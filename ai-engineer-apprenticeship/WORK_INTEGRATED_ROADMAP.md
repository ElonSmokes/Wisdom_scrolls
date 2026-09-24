# Рабочий roadmap: AI systems engineering

Проверено **24 сентября 2026**. Направление развития: **AI systems engineer / технический AI lead** — понимать вычисления, поставку и качество систем, которыми ты уже управляешь. Это ориентир навыков, а не присвоенный курсами уровень.

**Сейчас открыть только первый курс из таблицы.** В очереди четыре этапа. Разделы по 11 дисциплинам ниже — справочник, к которому обращаемся по задаче. [Прежний 32-недельный syllabus](archive/LEGACY_32_WEEK_SYLLABUS.md) сохранён в архиве; [текущая программа](SYLLABUS.md) следует этой очереди.

## Основная очередь: закончить, получить награду, применить

| Порядок | Курс / подготовка | Что получишь | Цена и темп |
|---|---|---|---|
| **1. CUDA** | [NVIDIA: Fundamentals of Accelerated Computing with CUDA Python](https://learn.nvidia.com/courses/course-detail?course_id=course-v1%3ADLI+S-AC-10+V1) | Сертификат курса после assessment; затем небольшой GPU benchmark | В карточке **$90, 8 часов**. На освоение с упражнениями заложить 3–5 недель |
| **2. Git → GitLab CI/CD** | [Pro Git](https://git-scm.com/book/en/v2) → [GitLab CI/CD Associate Learning Path](https://university.gitlab.com/learning-paths/gitlab-certified-cicd-associate-learning-path) → [экзамен](https://university.gitlab.com/courses/gitlab-certified-cicd-associate) | После сдачи экзамена: сертификат GitLab и Credly badge | Подготовка бесплатная; обычная цена экзамена **$150**, карточка также показывает $120 member price. Планировать 4–6 недель подготовки |
| **3. DevOps / SRE** | [Linux Foundation: Introduction to DevOps and Site Reliability Engineering — LFS162](https://training.linuxfoundation.org/training/introduction-to-devops-and-site-reliability-engineering-lfs162/) | **Digital badge**, финальный экзамен ≥70%; после курса — dashboard и runbook | **Бесплатно**, 10–12 часов материала; доступ **90 дней**. Планировать 3–5 недель |
| **4. RAG** | [NVIDIA: Building RAG Agents with LLMs](https://learn.nvidia.com/courses/course-detail?course_id=course-v1%3ADLI+S-FX-15+V1) | Сертификат курса после итоговой оценки; затем retrieval baseline с eval | В карточке **$90, 8 часов**. Планировать 4–6 недель с практикой |

Сроки в неделях — наша оценка при **3–5 часах в неделю**, без обещания уложиться; часы из карточек не включают все повторения и работу над своим проектом. Цены — снимок на дату проверки, окончательная сумма зависит от аккаунта и условий покупки. У курсов в основной очереди проверены публичные страницы, вход в регистрацию/покупку и описание награды. Оплата, запуск закрытых лабораторий и выдача награды в твоём аккаунте не выполнялись.

### Этап 1: как начать CUDA

**Входной порог:** Python — функции, циклы, массивы; NumPy — ndarray и операции над массивами. Если пока не можешь объяснить простой такой код, сначала пройди нужные темы Python/NumPy из материалов курса. Полный CS50P ниже — вариант для системного закрытия пробела, а не обязательный многомесячный барьер.

1. Пройти вводный раздел CUDA Python: CPU/GPU, перенос данных, Numba.
2. Пройти custom kernels: thread/block/grid; предсказать, какой элемент массива обрабатывает поток.
3. Пройти multidimensional grids и shared memory. Проверять корректность, затем измерять после warmup и синхронизации.
4. Самостоятельно выполнить assessment по правилам курса. Полученный сертификат можно сразу сохранить и распечатать.
5. Отдельным следующим шагом применить знания к H200: фиксированный workload, TTFT/ITL/VRAM, затем один профиль Nsight. **Сертификат уже заслужен; рабочий эксперимент — ещё одна победа.**

Курс использует Numba. Он даёт основы CUDA, но сам по себе не объясняет весь inference vLLM, attention или KV cache — для них предназначен раздел 1 справочника ниже.

У NVIDIA покупка поддерживается только в перечисленных провайдером странах: [условия доступа и список стран](https://www.nvidia.com/en-us/learn/training/support/). Общая политика DLI — доступ к материалам **до 6 месяцев** от старта, у GPU labs отдельные лимиты; индивидуальная дата закрытия курса важнее общего срока. Не покупать несколько курсов заранее.

Если запись или покупка недоступна для твоего аккаунта, продолжай по открытым материалам в разделе 1. **Они не выдают сертификат NVIDIA.** Для бесплатной короткой награды есть отдельный проверенный вариант Hugging Face ниже; он изучает агентов и не заменяет CUDA.

### Этап 2: GitLab — сначала подготовка, потом экзамен

Сначала Pro Git и упражнения с историей в разделе 2. Затем пройти пять блоков learning path по порядку: Introduction to CI/CD → Understanding GitLab Runners → Maintain Pipelines with Efficiency → Solving Complex Problems with Pipelines → Introduction to GitLab Registries. Сверить подготовку с текущими темами экзамена: его программа шире коротких видео.

Экзамен: 50 вопросов, 75 минут, проходной результат 75%; **14 дней доступа после регистрации и две попытки**. Покупать, когда подготовка закончена. На экзамене нельзя пользоваться AI или неразрешённой помощью. [Правила и выдача наград GitLab](https://university.gitlab.com/learn/article/gitlab-certification-candidate-handbook). Прохождение подготовительных видео само по себе не даёт эту сертификацию.

### Этапы 3–4: эксплуатация, затем RAG

LFS162 проходить в порядке его глав: DevOps/SRE → cloud → containers → IaC → CI/CD → observability → SRE. Это вводный обзор, не полноценная подготовка Kubernetes-администратора. [Вход в курс](https://trainingportal.linuxfoundation.org/courses/introduction-to-devops-and-site-reliability-engineering-lfs162); [критерий выдачи badge](https://www.credly.com/org/the-linux-foundation/badge/lfs162-introduction-to-devops-and-site-reliability-).

Перед RAG нужны уверенный Python/OOP и вводные знания deep learning; PyTorch/transfer learning рекомендованы. Если их не хватает, использовать разделы 5 и 10. После RAG — набор вопросов с эталонами, baseline retrieval, проверка доступа к документам и ошибок ответа. Сертификат курса и профессиональные экзамены NCA/NCP — разные награды.

## Практика и проверки

Для каждого основного этапа есть небольшое задание: [CUDA/inference](modules/cuda-and-inference.md) → [Git/GitLab](modules/git-and-gitlab.md) → [SRE](modules/observability-and-sre.md) → [ML/RAG](modules/04-ml-llm-and-capstone.md).

[Карта всех модулей](modules/README.md) связывает остальные дисциплины с рабочими задачами. [Внутренние проверки](exams/MASTER_EXAMS.md) помогают увидеть пробелы; они не заменяют assessment провайдера и не отменяют полученный сертификат. Для записи достаточно одного [milestone](templates/milestone.md) или [эксперимента](templates/experiment.md).

## Награды по остальным дисциплинам — выбрать одну, когда понадобится

| Потребность | Курс и порядок | Условие награды / границы |
|---|---|---|
| Python, backend, основы тестирования | [CS50P](https://cs50.harvard.edu/python/): Weeks 0–9 → final project; затем FastAPI из раздела 5 | [Бесплатный CS50 Certificate](https://cs50.harvard.edu/python/certificate/): ≥70% **на каждой** задаче и итоговом проекте. Это не платный verified edX certificate. На весь курс планировать месяцы при нашем темпе |
| SQL и базы данных | [CS50 SQL](https://cs50.harvard.edu/sql/): Querying → Relating → Designing → Writing → Viewing → Optimizing → Scaling → project; затем PostgreSQL из раздела 6 | [Бесплатный сертификат](https://cs50.harvard.edu/sql/certificate/): ≥70% на каждой задаче и проекте. Курс не заменяет эксплуатацию PostgreSQL |
| Frontend и web backend | [Full Stack Open](https://fullstackopen.com/en/): Parts 0–5, затем 6–7 по необходимости; JS → React → Node → tests | [Правила сертификата](https://fullstackopen.com/en/part0/general_info): сдавать упражнения до проходного уровня; текущая таблица для 0–5 — минимум 72. Сертификат скачивается в submission system; экзамен для сертификата не нужен. Уверенное программирование — prerequisite; это длинный факультатив |
| Security | [CS50 Cybersecurity](https://cs50.harvard.edu/cybersecurity/): Accounts → Data → Systems → Software → Privacy → project | [Бесплатный сертификат](https://cs50.harvard.edu/cybersecurity/certificate/): ≥70% на каждой задаче и проекте. Для AppSec/LLM security дополнительно раздел 9 |
| Короткий финиш по AI agents | [Hugging Face Agents, Unit 1](https://huggingface.co/learn/agents-course/unit1/introduction) → [актуальное приложение quiz](https://huggingface.co/spaces/agents-course/unit_1_quiz) | [Certificate of Fundamentals](https://huggingface.co/learn/agents-course/unit1/get-your-certificate): Unit 1 + quiz ≥80%, бесплатно. Приложение запускается, далее нужен HF login. Это сертификат **первого раздела**, не всего курса |
| QA, Linux/containers, observability, лидерство | QA — тесты CS50P и практика раздела 4; инфраструктура/SRE — LFS162 и разделы 3/7; лидерство — раздел 11 | За отдельную рабочую практику оформлять личную ачивку с результатом и доказательством. Она не является сертификатом учебного провайдера |

[TAU Introduction to pytest](https://testautomationu.applitools.com/pytest-tutorial/) **пока отложен**: публичный текст доступен через поиск, но браузер дважды показал Site Unavailable. Не ставим его условием продвижения и не обещаем получение награды.

## Как сохранять мотивацию

Один активный курс. За завершение — награда на стену; за применение — короткая запись результата. Можно закончить курс и отпраздновать это до завершения большого рабочего проекта. В [CREDENTIALS.md](CREDENTIALS.md) — сохранение, печать и шаблон личной ачивки; в [PROGRESS.md](PROGRESS.md) — очередь и журнал.

Рабочие агенты могут продолжать писать код. Для заданий, которые сдаются на сертификат, действуют правила **конкретного провайдера**: самостоятельный assessment нельзя автоматически приравнивать к обычной агентной работе.

## Что проверено и что убрано

[Полный аудит всех 80 исходных ссылок и новых ресурсов](LINK_AUDIT_2026-09-24.md). Из обязательного пути исключены T-AC-01 и S-FX-18: карточки показывают закрытие записи, кнопки отключены. C-FX-26 помечен окончанием доступа 31.12.2026 и тоже исключён. Некоторые другие DLI-курсы доступны к покупке, но сертификат именно для них не подтверждён — они только дополнительные материалы.

Проверка фиксирует состояние на **24.09.2026**, не гарантирует вечную доступность. Перед началом каждого следующего курса достаточно проверить на его странице три поля: **запись, срок доступа, награда**. Новое предупреждение о закрытии означает паузу покупки и выбор проверенной замены.

---

# Справочник по дисциплинам

Это не дополнительные одиннадцать обязательных курсов. Читать выбранные разделы под один рабочий вопрос. Для рабочего результата сохранять гипотезу, измерение, вывод и способ отката. В публичный репозиторий переносить только обезличенные учебные примеры.

## 1. CUDA, устройство GPU и LLM inference

### Открытые материалы и запасной путь без оплаты

[An Even Easier Introduction to CUDA — статья NVIDIA](https://developer.nvidia.com/blog/even-easier-introduction-cuda/) → [NVIDIA Accelerated Python Tutorial](https://github.com/NVIDIA/accelerated-computing-hub/tree/main/tutorials/accelerated-python). В Python tutorial: Fundamentals 01 → 03 → 05 → 06 → 07 → Kernels 40. Сначала перенос данных и память, затем асинхронность и один kernel. Это открытые учебные материалы **без обещанного сертификата**; GPU-запуск требует совместимого окружения и здесь не проверялся.

Дополнительно после базового курса, только если нужна соответствующая практика:

- [Optimizing CUDA Machine Learning Codes With Nsight Profiling Tools](https://learn.nvidia.com/courses/course-detail?course_id=course-v1%3ADLI+S-AC-03+V2): $30, 2 часа, intermediate; CUDA familiarity. Buy Now доступна, сертификат не подтверждён карточкой.
- [Find the Bottleneck: Optimize AI Pipelines With Nsight Systems](https://learn.nvidia.com/courses/course-detail?course_id=course-v1%3ADLI+S-AC-14+V1): $30, 3 часа, advanced; Python и PyTorch. Buy Now доступна, сертификат не подтверждён карточкой.

[Общие NVIDIA Learning Paths](https://www.nvidia.com/en-us/learn/learning-paths/) использовать как каталог тем; актуальность конкретной записи проверяется в карточке.

**Порядок изучения:**

1. **Карта вычислений.** [NVIDIA GPU Performance Background](https://docs.nvidia.com/deeplearning/performance/dl-performance-gpu-background/index.html) → [CUDA Programming Guide: Introduction / Programming Model](https://docs.nvidia.com/cuda/cuda-programming-guide/). Разобрать SM, warps, blocks, память HBM/L2/shared/registers, kernel launch, PCIe/NVLink, latency versus bandwidth. Читать выбранные разделы, не весь справочник.
2. **Один маленький kernel.** [NVIDIA CUDA samples](https://github.com/NVIDIA/cuda-samples) (`vectorAdd`, затем matrix multiplication) → [CUDA Best Practices Guide](https://docs.nvidia.com/cuda/cuda-c-best-practices-guide/) (memory, occupancy, profiling). Сравнить CPU, наивный GPU и библиотечную реализацию; проверить корректность и время после warmup. Если C++ пока тормозит, сначала [PyTorch Basics](https://docs.pytorch.org/tutorials/beginner/basics/) на remote GPU, затем вернуться к одному kernel. Это учебный эксперимент, не переписывание vLLM.
3. **Transformer as workload.** [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/) → [Hugging Face LLM Course](https://huggingface.co/learn/llm-course/chapter1/1) (tokenizer/model/generation) → [PyTorch scaled dot product attention](https://docs.pytorch.org/docs/2.14/generated/torch.nn.functional.scaled_dot_product_attention.html). Выписать размерности Q/K/V, causal mask, почему prefill и decode отличаются. Затем оценить KV cache из config конкретной модели: `2 × layers × KV-heads × head-dim × bytes × tokens × concurrent sequences`; проверить GQA/MQA, dtype, block waste и runtime overhead. Эта оценка относится к обычному attention с K/V на каждом слое и полным контекстом; для MLA, sliding-window, гибридных архитектур и tensor parallelism проверять раскладку конкретного engine. Для MoE отдельно различать общие веса модели, активные параметры и KV.
4. **Serving.** [vLLM docs](https://docs.vllm.ai/en/latest/) (serving, scheduler, KV cache, benchmarking/metrics) → [SGLang docs](https://docs.sglang.io/) (serving, benchmarking). Разобрать request → queue → prefill → allocation → decode → stream, batching, prefix reuse, tensor parallelism. Не переносить особенности одного engine на другой без проверки версии.
5. **Профиль.** [Nsight Systems](https://docs.nvidia.com/nsight-systems/UserGuide/) для timeline → [Nsight Compute](https://docs.nvidia.com/nsight-compute/) для конкретного kernel → [PyTorch Profiler](https://docs.pytorch.org/tutorials/beginner/profiler.html) при PyTorch workload. Сначала гипотеза о bottleneck; затем профиль, иначе график бесполезен.

**Практика на H200:** повторить контролируемый benchmark одной модели при фиксированных версии движка, quantization, prompt/output tokens, concurrency 1/4/8 и числе GPU. Сохранять raw measurements, TTFT p50/p95, ITL, output tok/s, GPU memory, queue/CPU и настройки. Не считать wall time `curl` чистой скоростью decode; учитывать reasoning tokens и warmup. Сопоставить предсказанный KV и фактический VRAM, объяснить расхождение. На рабочих моделях профилировать в согласованном окне.

**Выход:** внутренняя таблица допустимых профилей нагрузки и процедура выбора конфигурации H200; публично — только синтетический воспроизводимый `llm-inference-lab`, если разрешена публикация методики. **Что перестаю принимать на веру:** «модель помещается, значит выдержит N пользователей».

**Книга на углубление:** [Programming Massively Parallel Processors (Hwu, Kirk, El Hajj)](https://shop.elsevier.com/books/programming-massively-parallel-processors/hwu/978-0-323-91231-0), главы о GPU architecture, threads и memory после первого опыта; покупать необязательно.

## 2. Git и GitLab CI/CD — после первого CUDA-финиша

1. [Pro Git](https://git-scm.com/book/en/v2): главы 1–3 (объекты, stage, commits, branches/merges), затем 7.5–7.7 (search, rewriting, reset), 7.10 (debugging), 10.2–10.3 (objects/references) выборочно. Нарисовать `HEAD`, branch pointer, index, working tree; объяснить `reset` versus `revert`.
2. В отдельной учебной ветке воспроизвести conflict, `revert`, `reflog`, `bisect`, merge request и безопасный откат. Не упражняться с force push на общей ветке. Перед агентной задачей зафиксировать base commit; после — `git status`, `git diff --stat`, `git diff`, tests и review.
3. [GitLab CI quick start](https://docs.gitlab.com/ci/quick_start/) → [YAML reference](https://docs.gitlab.com/ci/yaml/) (`stages`, `needs`, `rules`, `artifacts`, `cache`) → [Runner](https://docs.gitlab.com/runner/) → [Environments](https://docs.gitlab.com/ci/environments/) и [deployment safety](https://docs.gitlab.com/ci/environments/deployment_safety/). На корпоративном GitLab проверить версию и доступность конкретных функций.
4. Проследить **один настоящий pipeline**: commit → runner → build → artifact/image digest → tests/evals → staging → approval → prod → rollback. Понять, чей token и права получает job, где секреты и откуда образ.

**Выход:** одностраничная карта существующего GitLab pipeline, обязательный diff/review для агентных изменений и проверенный сценарий возврата версии на staging. **Что перестаю принимать на веру:** «пайплайн зелёный, значит релиз можно безопасно развернуть».

## 3. Observability и SRE

[Google SRE Book: SLI/SLO](https://sre.google/sre-book/service-level-objectives/) → [OpenTelemetry concepts](https://opentelemetry.io/docs/concepts/) → [Prometheus getting started](https://prometheus.io/docs/prometheus/latest/getting_started/) → [Grafana fundamentals](https://grafana.com/tutorials/grafana-fundamentals/). Для ClearGate отметить время deterministic/NER/LLM/verify, p50/p95, ошибки и correlation ID; для inference — TTFT/ITL, queue, KV usage и GPU. Проверить один отказ сервиса и действие alert. **Выход:** dashboard и runbook с порогом и ответственным. **Не верю:** «healthcheck зелёный, значит пользователи работают».

## 4. QA и LLM evaluation

[pytest getting started](https://docs.pytest.org/en/stable/getting-started.html) → [Playwright docs](https://playwright.dev/docs/intro) → [Google ML Crash Course: classification](https://developers.google.com/machine-learning/crash-course/classification/accuracy-precision-recall) → [NIST AI RMF](https://www.nist.gov/itl/ai-risk-management-framework) для рамки рисков. На ClearGate создать размеченный набор по типам документов, отдельный held-out split и отрицательные кейсы для публичных юрлиц, адресов, фамилий и утечек. Отдельно измерять false negatives критичных полей, precision, latency; не заявлять абсолютную гарантию по нулю ошибок в конечной выборке. **Выход:** CI gate по регрессиям и отчёт «до/после» с сырой выборкой под корпоративным доступом. **Не верю:** «новый prompt кажется лучше».

## 5. Backend и рабочий Python

[Python tutorial](https://docs.python.org/3/tutorial/) (только пробелы) → [typing](https://docs.python.org/3/library/typing.html) и [asyncio](https://docs.python.org/3/library/asyncio.html) → [FastAPI tutorial](https://fastapi.tiangolo.com/tutorial/) (dependencies, testing, background tasks) → [Pydantic docs](https://pydantic.dev/docs/validation/latest/get-started/) → [SQLAlchemy 2.0 tutorial](https://docs.sqlalchemy.org/en/20/tutorial/) и [Alembic](https://alembic.sqlalchemy.org/en/latest/tutorial.html). Разобрать один рабочий endpoint: вход, auth, lifetime dependency, transaction, retry/idempotency, failure, response. AI может менять код, ты проверяешь boundary и негативный тест. **Книга:** [Architecture Patterns with Python](https://www.cosmicpython.com/book/preface), главы repository/service/unit of work по мере появления реальной проблемы. **Выход:** review checklist для FastAPI/Django сервиса. **Не верю:** «async делает CPU-bound код быстрее».

## 6. PostgreSQL и data engineering

[PostgreSQL tutorial](https://www.postgresql.org/docs/current/tutorial.html) → [Transactions](https://www.postgresql.org/docs/current/tutorial-transactions.html) → [EXPLAIN](https://www.postgresql.org/docs/current/using-explain.html) → [Indexes](https://www.postgresql.org/docs/current/indexes.html) → [MVCC](https://www.postgresql.org/docs/current/mvcc.html). На ERP выбрать два медленных запроса, записать план до/после индекса, проверить реальные строки, блокировки, backup/restore и миграцию на staging. **Книга:** [The Art of PostgreSQL](https://theartofpostgresql.com/) как углубление SQL. **Выход:** DB review с измерениями и обратимой миграцией. **Не верю:** «индекс всегда ускорит запрос».

## 7. Linux, containers и инфраструктура

[The Linux Command Line](https://linuxcommand.org/tlcl.php) (permissions, processes, I/O) → [systemd docs](https://systemd.io/) → [Docker overview](https://docs.docker.com/get-started/docker-overview/) и [Compose](https://docs.docker.com/compose/) → [Podman docs](https://docs.podman.io/en/latest/) → [NVIDIA Container Toolkit](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/). На своей dev VM проследить service → container user → volume → network → GPU device → log; отрепетировать перезапуск с сохранением state. Сохранять dev/prod границу и принцип prod без исходящего доступа по принятой архитектуре. **Выход:** схема runtime, список зависимостей и процедура восстановления. **Не верю:** «контейнер запустился, значит данные и GPU доступны».

## 8. Frontend и UX контроль агента

[MDN Learn web development](https://developer.mozilla.org/en-US/docs/Learn_web_development) (HTML/CSS/HTTP) → [TypeScript Handbook](https://www.typescriptlang.org/docs/handbook/intro.html) → [React Learn](https://react.dev/learn) (state/effects) → [Next.js Learn](https://nextjs.org/learn) (server/client boundary) → [WAI accessibility tutorials](https://www.w3.org/WAI/tutorials/) → [Playwright](https://playwright.dev/docs/intro). В ClearGate пройти один review flow: loading/error/empty states, keyboard use, сохранение несданных правок, API contract. **Выход:** проверенный пользовательский сценарий и тест. **Не верю:** «скриншот красивый, значит процесс работает».

## 9. Security engineering

[OWASP Top 10](https://owasp.org/projects/top-ten) → [OWASP API Security Top 10](https://api-security.owasp.org/) → [OWASP LLM Top 10](https://genai.owasp.org/llm-top-10/) → [NIST SSDF](https://csrc.nist.gov/Projects/ssdf) → [OAuth 2.0 Security BCP](https://www.rfc-editor.org/info/rfc9700/). Нарисовать trust boundaries lawyer → browser → ClearGate → локальная модель → разрешённый cloud egress → restore. Проверить на staging cross-user/matter access, SSRF, injection, секреты runner, отказ при недоступности модели; согласовать с ИБ. **Выход:** threat model и перечень конкретных проверок перед релизом. **Не верю:** «агент соблюдёт границы по prompt».

## 10. ML engineering, RAG и модели

[Google ML Crash Course](https://developers.google.com/machine-learning/crash-course) → [PyTorch Basics](https://docs.pytorch.org/tutorials/beginner/basics/) → [Hugging Face LLM Course](https://huggingface.co/learn/llm-course/chapter1/1) → [Hugging Face PEFT](https://huggingface.co/docs/peft/index) → [Hugging Face TRL](https://huggingface.co/docs/trl/index). Для RAG — [Stanford IR book](https://nlp.stanford.edu/IR-book/) (evaluation/retrieval) и [Qdrant docs](https://qdrant.tech/documentation/) для ACL-aware retrieval и фильтров. Сначала baseline на ClearGate/документном поиске, затем размеченные данные, train/dev/held-out split, fine-tune только при доказанной потребности, абляция и мониторинг дрейфа. **Книга:** [Build a Large Language Model (From Scratch)](https://www.manning.com/books/build-a-large-language-model-from-scratch), избранные главы об attention/training; глубокое чтение после рабочего baseline. **Выход:** решение о модели с воспроизводимым quality/latency/cost сравнением. **Не верю:** «fine-tune исправит отсутствие eval dataset».

### Дополнительные DLI и профессиональные экзамены

[Evaluating RAG and Semantic Search Systems](https://learn.nvidia.com/courses/course-detail?course_id=course-v1%3ADLI+S-FX-32+V1): $30 / 3 часа; открыта покупка, но выдача сертификата не подтверждена. Брать при задаче на retrieval/evaluation.

[Introduction to Deploying RAG Pipelines for Production at Scale](https://learn.nvidia.com/courses/course-detail?course_id=course-v1%3ADLI+S-FX-19+V1): карточка показывает $90 / 4 часа, Kubernetes/Helm/NIM. В обзорной сертификационной странице похожий курс указан иначе; награда для именно этой версии не подтверждена. Не покупать ради сертификата без уточнения.

[NCA-GENL](https://www.nvidia.com/en-us/learn/certification/generative-ai-llm-associate/) и [NCP-GENL](https://www.nvidia.com/en-us/learn/certification/generative-ai-llm-professional/) — факультативные отдельные экзамены, не следующий обязательный курс. Страницы регистрации существуют, после сдачи заявлены badge и optional certificate. Возможность экзамена в твоей стране и условия в аккаунте экзаменационного провайдера не проверены. NCA проверяет основы, NCP требует более глубокой подготовки по training/distributed systems. Подготовительные ссылки внутри страницы NVIDIA тоже могут устаревать.

## 11. Applied AI, продукт и лидерство — постоянно

[AI Engineering (Chip Huyen)](https://www.oreilly.com/library/view/ai-engineering/9781098166298/) читать по текущему узкому месту (evaluation, deployment, agents) → [Google engineering practices: code review](https://google.github.io/eng-practices/review/) → [The Manager's Path](https://www.oreilly.com/library/view/the-managers-path/9781491973882/) главы про управление проектом и командой по необходимости. На каждом рабочем milestone: одно решение ADR, владелец риска, метрика результата, понятный Definition of Done, короткий стандарт для будущих людей/агентов. **Выход:** повторяемый процесс поставки системы и понятные достижения, которые можно отмечать. Книги и code review сами по себе сертификатов не выдают.

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

## Ближайшие три занятия

1. **45–60 минут:** проверить prerequisite Python/NumPy, открыть CUDA Python и пройти вводный раздел. При ограничении записи использовать открытую статью и tutorial.
2. **45–60 минут:** kernel launch, thread/block/grid; записать одно объяснение своими словами и один вопрос.
3. **90–120 минут:** воспроизвести небольшой пример, проверить результат и замер. Продолжать курс до assessment. GitLab начнётся следующим этапом; срочный рабочий вопрос можно решить отдельно.

Сертификат сохранить сразу после выдачи. За полный рабочий benchmark оформить вторую, личную ачивку.
