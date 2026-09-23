# Рабочий roadmap: AI systems engineering

Обновлено: 23 сентября 2026. Приоритет: **CUDA/GPU inference → Git/GitLab → ближайший производственный риск**. Этот план заменяет календарный порядок `SYLLABUS.md`; старый 32-недельный syllabus остаётся как самостоятельный углублённый трек. Текущие отметки в `PROGRESS.md` не означают, что перечисленные ниже этапы уже пройдены.

## Как проходить при полной загрузке

- 3–5 часов в неделю: 2 коротких занятия по 45–60 минут и один практический блок 90–120 минут. В аврал оставить один блок на критичный рабочий вопрос; даты сдвигаются.
- На каждый блок: **понять механизм → предсказать результат → поручить агенту реализацию или измерение → проверить исходные данные → записать решение**. Продукционный код агент продолжает писать.
- Раз в неделю выбрать ровно один вертикальный срез рабочей задачи. Для него оставить: схему потока, дифф, наблюдаемое подтверждение, отказной сценарий и способ отката. Секреты, клиентские документы и внутренние адреса в публичный репозиторий не переносить.
- Критерий завершения: ты можешь объяснить решение и опровергнуть неверное утверждение агента на данных. Просмотр видео, сертификат и число написанных вручную строк сами по себе не считаются.
- После первых двух блоков выбирай следующий по тому, что больше мешает работе. Последовательность далее — предпочтительный порядок, а не фиксированные месяцы. Сертификаты NVIDIA, ШАД, статьи и конференции — отдельная надстройка, без обязательного дедлайна в рабочем треке.

## 1. CUDA, устройство GPU и LLM inference — начать сейчас (4–6 недель)

**Порядок изучения:**

1. **Карта вычислений.** [NVIDIA GPU Performance Background](https://docs.nvidia.com/deeplearning/performance/dl-performance-gpu-background/index.html) → [CUDA Programming Guide: Introduction / Programming Model](https://docs.nvidia.com/cuda/cuda-programming-guide/). Разобрать SM, warps, blocks, память HBM/L2/shared/registers, kernel launch, PCIe/NVLink, latency versus bandwidth. Читать выбранные разделы, не весь справочник.
2. **Один маленький kernel.** [NVIDIA CUDA samples](https://github.com/NVIDIA/cuda-samples) (`vectorAdd`, затем matrix multiplication) → [CUDA Best Practices Guide](https://docs.nvidia.com/cuda/cuda-c-best-practices-guide/) (memory, occupancy, profiling). Сравнить CPU, наивный GPU и библиотечную реализацию; проверить корректность и время после warmup. Если C++ пока тормозит, сначала [PyTorch Basics](https://docs.pytorch.org/tutorials/beginner/basics/) на remote GPU, затем вернуться к одному kernel. Это учебный эксперимент, не переписывание vLLM.
3. **Transformer as workload.** [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/) → [Hugging Face LLM Course](https://huggingface.co/learn/llm-course/chapter1/1) (tokenizer/model/generation) → [PyTorch scaled dot product attention](https://docs.pytorch.org/docs/stable/generated/torch.nn.functional.scaled_dot_product_attention.html). Выписать размерности Q/K/V, causal mask, почему prefill и decode отличаются. Затем оценить KV cache из config конкретной модели: `2 × layers × KV-heads × head-dim × bytes × tokens × concurrent sequences`; проверить GQA/MQA, dtype, block waste и runtime overhead. Для MoE отдельно различать общие веса модели, активные параметры и KV.
4. **Serving.** [vLLM docs](https://docs.vllm.ai/en/latest/) (serving, scheduler, KV cache, benchmarking/metrics) → [SGLang docs](https://docs.sglang.ai/) (serving, benchmarking). Разобрать request → queue → prefill → allocation → decode → stream, batching, prefix reuse, tensor parallelism. Не переносить особенности одного engine на другой без проверки версии.
5. **Профиль.** [Nsight Systems](https://docs.nvidia.com/nsight-systems/UserGuide/) для timeline → [Nsight Compute](https://docs.nvidia.com/nsight-compute/) для конкретного kernel → [PyTorch Profiler](https://docs.pytorch.org/tutorials/beginner/profiler.html) при PyTorch workload. Сначала гипотеза о bottleneck; затем профиль, иначе график бесполезен.

**Практика на H200:** повторить контролируемый benchmark одной модели при фиксированных версии движка, quantization, prompt/output tokens, concurrency 1/4/8 и числе GPU. Сохранять raw measurements, TTFT p50/p95, ITL, output tok/s, GPU memory, queue/CPU и настройки. Не считать wall time `curl` чистой скоростью decode; учитывать reasoning tokens и warmup. Сопоставить предсказанный KV и фактический VRAM, объяснить расхождение. На рабочих моделях профилировать в согласованном окне.

**Выход:** внутренняя таблица допустимых профилей нагрузки и процедура выбора конфигурации H200; публично — только синтетический воспроизводимый `llm-inference-lab`, если разрешена публикация методики. **Что перестаю принимать на веру:** «модель помещается, значит выдержит N пользователей».

**Книга на углубление:** [Programming Massively Parallel Processors (Hwu, Kirk, El Hajj)](https://www.elsevier.com/books/programming-massively-parallel-processors/hwu/978-0-323-91231-0), главы о GPU architecture, threads и memory после первого опыта; покупать необязательно.

## 2. Git и GitLab CI/CD — параллельно с CUDA (2–3 недели)

1. [Pro Git](https://git-scm.com/book/en/v2): главы 1–3 (объекты, stage, commits, branches/merges), затем 7.5–7.7 (search, rewriting, reset), 7.10 (debugging), 10.2–10.3 (objects/references) выборочно. Нарисовать `HEAD`, branch pointer, index, working tree; объяснить `reset` versus `revert`.
2. В отдельной учебной ветке воспроизвести conflict, `revert`, `reflog`, `bisect`, merge request и безопасный откат. Не упражняться с force push на общей ветке. Перед агентной задачей зафиксировать base commit; после — `git status`, `git diff --stat`, `git diff`, tests и review.
3. [GitLab CI quick start](https://docs.gitlab.com/ci/quick_start/) → [YAML reference](https://docs.gitlab.com/ci/yaml/) (`stages`, `needs`, `rules`, `artifacts`, `cache`) → [Runner](https://docs.gitlab.com/runner/) → [Environments](https://docs.gitlab.com/ci/environments/) и [deployment safety](https://docs.gitlab.com/ci/environments/deployment_safety/). На корпоративном GitLab проверить версию и доступность конкретных функций.
4. Проследить **один настоящий pipeline**: commit → runner → build → artifact/image digest → tests/evals → staging → approval → prod → rollback. Понять, чей token и права получает job, где секреты и откуда образ.

**Выход:** одностраничная карта существующего GitLab pipeline, обязательный diff/review для агентных изменений и проверенный сценарий возврата версии на staging. **Что перестаю принимать на веру:** «пайплайн зелёный, значит релиз можно безопасно развернуть».

## 3. Observability и SRE (2–4 недели)

[Google SRE Book: SLI/SLO](https://sre.google/sre-book/service-level-objectives/) → [OpenTelemetry concepts](https://opentelemetry.io/docs/concepts/) → [Prometheus getting started](https://prometheus.io/docs/prometheus/latest/getting_started/) → [Grafana fundamentals](https://grafana.com/tutorials/grafana-fundamentals/). Для ClearGate отметить время deterministic/NER/LLM/verify, p50/p95, ошибки и correlation ID; для inference — TTFT/ITL, queue, KV usage и GPU. Проверить один отказ сервиса и действие alert. **Выход:** dashboard и runbook с порогом и ответственным. **Не верю:** «healthcheck зелёный, значит пользователи работают».

## 4. QA и LLM evaluation (2–4 недели)

[pytest getting started](https://docs.pytest.org/en/stable/getting-started.html) → [Playwright docs](https://playwright.dev/docs/intro) → [Google ML Crash Course: classification](https://developers.google.com/machine-learning/crash-course/classification/accuracy-precision-recall) → [NIST AI RMF](https://www.nist.gov/itl/ai-risk-management-framework) для рамки рисков. На ClearGate создать размеченный набор по типам документов, отдельный held-out split и отрицательные кейсы для публичных юрлиц, адресов, фамилий и утечек. Отдельно измерять false negatives критичных полей, precision, latency; не заявлять абсолютную гарантию по нулю ошибок в конечной выборке. **Выход:** CI gate по регрессиям и отчёт «до/после» с сырой выборкой под корпоративным доступом. **Не верю:** «новый prompt кажется лучше».

## 5. Backend и рабочий Python (3–5 недель)

[Python tutorial](https://docs.python.org/3/tutorial/) (только пробелы) → [typing](https://docs.python.org/3/library/typing.html) и [asyncio](https://docs.python.org/3/library/asyncio.html) → [FastAPI tutorial](https://fastapi.tiangolo.com/tutorial/) (dependencies, testing, background tasks) → [Pydantic docs](https://docs.pydantic.dev/latest/) → [SQLAlchemy 2.0 tutorial](https://docs.sqlalchemy.org/en/20/tutorial/) и [Alembic](https://alembic.sqlalchemy.org/en/latest/tutorial.html). Разобрать один рабочий endpoint: вход, auth, lifetime dependency, transaction, retry/idempotency, failure, response. AI может менять код, ты проверяешь boundary и негативный тест. **Книга:** [Architecture Patterns with Python](https://www.cosmicpython.com/book/preface.html), главы repository/service/unit of work по мере появления реальной проблемы. **Выход:** review checklist для FastAPI/Django сервиса. **Не верю:** «async делает CPU-bound код быстрее».

## 6. PostgreSQL и data engineering (2–4 недели)

[PostgreSQL tutorial](https://www.postgresql.org/docs/current/tutorial.html) → [Transactions](https://www.postgresql.org/docs/current/tutorial-transactions.html) → [EXPLAIN](https://www.postgresql.org/docs/current/using-explain.html) → [Indexes](https://www.postgresql.org/docs/current/indexes.html) → [MVCC](https://www.postgresql.org/docs/current/mvcc.html). На ERP выбрать два медленных запроса, записать план до/после индекса, проверить реальные строки, блокировки, backup/restore и миграцию на staging. **Книга:** [The Art of PostgreSQL](https://theartofpostgresql.com/) как углубление SQL. **Выход:** DB review с измерениями и обратимой миграцией. **Не верю:** «индекс всегда ускорит запрос».

## 7. Linux, containers и инфраструктура (3–5 недель)

[The Linux Command Line](https://linuxcommand.org/tlcl.php) (permissions, processes, I/O) → [systemd docs](https://systemd.io/) → [Docker overview](https://docs.docker.com/get-started/docker-overview/) и [Compose](https://docs.docker.com/compose/) → [Podman docs](https://docs.podman.io/en/latest/) → [NVIDIA Container Toolkit](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/). На своей dev VM проследить service → container user → volume → network → GPU device → log; отрепетировать перезапуск с сохранением state. Сохранять dev/prod границу и принцип prod без исходящего доступа по принятой архитектуре. **Выход:** схема runtime, список зависимостей и процедура восстановления. **Не верю:** «контейнер запустился, значит данные и GPU доступны».

## 8. Frontend и UX контроль агента (2–4 недели)

[MDN Learn web development](https://developer.mozilla.org/en-US/docs/Learn_web_development) (HTML/CSS/HTTP) → [TypeScript Handbook](https://www.typescriptlang.org/docs/handbook/intro.html) → [React Learn](https://react.dev/learn) (state/effects) → [Next.js Learn](https://nextjs.org/learn) (server/client boundary) → [WAI accessibility tutorials](https://www.w3.org/WAI/tutorials/) → [Playwright](https://playwright.dev/docs/intro). В ClearGate пройти один review flow: loading/error/empty states, keyboard use, сохранение несданных правок, API contract. **Выход:** проверенный пользовательский сценарий и тест. **Не верю:** «скриншот красивый, значит процесс работает».

## 9. Security engineering (3–5 недель)

[OWASP Top 10](https://owasp.org/www-project-top-ten/) → [OWASP API Security Top 10](https://owasp.org/API-Security/) → [OWASP LLM Top 10](https://genai.owasp.org/llm-top-10/) → [NIST SSDF](https://csrc.nist.gov/Projects/ssdf) → [OAuth 2.0 Security BCP](https://www.rfc-editor.org/rfc/rfc9700). Нарисовать trust boundaries lawyer → browser → ClearGate → локальная модель → разрешённый cloud egress → restore. Проверить на staging cross-user/matter access, SSRF, injection, секреты runner, отказ при недоступности модели; согласовать с ИБ. **Выход:** threat model и перечень конкретных проверок перед релизом. **Не верю:** «агент соблюдёт границы по prompt».

## 10. ML engineering, RAG и модели (4–8 недель после измерений)

[Google ML Crash Course](https://developers.google.com/machine-learning/crash-course) → [PyTorch Basics](https://docs.pytorch.org/tutorials/beginner/basics/) → [Hugging Face LLM Course](https://huggingface.co/learn/llm-course/chapter1/1) → [Hugging Face PEFT](https://huggingface.co/docs/peft/index) → [Hugging Face TRL](https://huggingface.co/docs/trl/index). Для RAG — [Stanford IR book](https://nlp.stanford.edu/IR-book/) (evaluation/retrieval) и [Qdrant docs](https://qdrant.tech/documentation/) для ACL-aware retrieval и фильтров. Сначала baseline на ClearGate/документном поиске, затем размеченные данные, train/dev/held-out split, fine-tune только при доказанной потребности, абляция и мониторинг дрейфа. **Книга:** [Build a Large Language Model (From Scratch)](https://www.manning.com/books/build-a-large-language-model-from-scratch), избранные главы об attention/training; глубокое чтение после рабочего baseline. **Выход:** решение о модели с воспроизводимым quality/latency/cost сравнением. **Не верю:** «fine-tune исправит отсутствие eval dataset».

## 11. Applied AI, продукт и лидерство — постоянно

[AI Engineering (Chip Huyen)](https://www.oreilly.com/library/view/ai-engineering/9781098166298/) читать по текущему узкому месту (evaluation, deployment, agents) → [Google engineering practices: code review](https://google.github.io/eng-practices/review/) → [The Manager's Path](https://www.oreilly.com/library/view/the-managers-path/9781491973882/) главы про управление проектом и командой по необходимости. На каждом рабочем milestone: одно решение ADR, владелец риска, метрика результата, понятный Definition of Done, короткий стандарт для будущих людей/агентов. **Выход:** повторяемый процесс поставки системы, а не коллекция сертификатов.

## Шаблон одного milestone

```text
Рабочая проблема:
Моя гипотеза и ожидаемое измерение:
Ресурс (точный раздел):
Что сделал агент:
Что я проверил сам (команда/лог/метрика/пользовательский сценарий):
Граница доступа и отказной сценарий:
Результат до → после:
Как откатить:
Что теперь не отдаю агенту на слепое доверие:
Следующий самый дорогой пробел:
```

## Первые две недели

1. Создать в приватных рабочих заметках baseline H200: модель, engine/version, token counts, TTFT, ITL, VRAM, 1/4/8 concurrency. Прочитать раздел GPU Background, объяснить prefill/decode и оценить KV на реальном config.
2. Проследить один запрос через сервер, проверить расчёт profiler/metrics и записать расхождения; параллельно прочитать Pro Git 1–3 и разобрать историю одного merge request.
3. На отдельной ветке потренировать `revert`/`reflog`/`bisect`. Нарисовать один GitLab pipeline, найти artifact и проверить staging rollback.
4. На ревью записать: какое решение о H200 стало точнее и какую ошибку в изменениях/релизе удалось поймать до production.
