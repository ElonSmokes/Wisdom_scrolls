# Аудит roadmap и ссылок — 24.09.2026

## Объём и метод

- Исходная версия: commit `d678caa80a64e3b44a77df10762a4e3aacdf527b`.
- Прочитаны все **16 Markdown-файлов** репозитория; в них найдено **80 уникальных внешних Markdown-ссылок**, все находились в WORK_INTEGRATED_ROADMAP.md.
- Каждая исходная внешняя ссылка проверена через открытие страницы. Для динамических NVIDIA/GitLab использован браузер с загруженным содержимым; для открытого NVIDIA tutorial — GitHub API после ошибки текстового веб-просмотра.
- Отдельно проверен ранее убранный T-AC-01. Итого **9 карточек DLI** просмотрены в браузере.
- Проверены **29 новых адресов**, включая 8 конечных адресов вместо перенаправлений. Вместе с T-AC-01 реестр ниже содержит **110 уникальных внешних адресов**. Служебные ссылки внутри сайтов провайдеров не считаются автоматически проверенными.
- Для курсов отдельно смотрелись название/версия, предупреждения о закрытии, кнопка записи/покупки, программа, prerequisites, награда и условия доступа.
- У книг проверена страница издателя/автора; доступ ко всей платной книге не покупался.

**Граница проверки:** публичная карточка и действующий вход в регистрацию не доказывают оплату, доступность в конкретной стране, работоспособность labs или будущую выдачу сертификата в аккаунте. Регистрация, покупки, assessments и печать полученных наград не выполнялись. Чтение сайта не является прохождением курса. Дата важна: провайдеры могут изменить условия позднее.

## Что исправлено в маршруте

| Проблема | Решение |
|---|---|
| T-AC-01: запись отключена, баннер закрытия | Исключён; первый сертификационный курс — CUDA Python. Открытая CUDA-статья сохранена как материал без сертификата |
| S-FX-18 Sizing LLM Inference Systems: запись тоже отключена | Исключён. Sizing изучается на документации и собственном benchmark |
| C-FX-26 Adding New Knowledge: доступ истекает 31.12.2026 | Исключён из основной очереди, не планируется на отдалённый срок |
| S-AC-03 / S-AC-14 / S-FX-32: купить можно, сертификат не подтверждён | Только факультатив для содержания, без обещания награды |
| S-FX-19: карточка и обзорная NCP-страница расходятся по похожему курсу | Не обещать сертификат для этой конкретной версии |
| GitLab экзамен имеет короткое окно | Подготовка до покупки; явно указаны 14 дней и две попытки |
| LFS162 — badge, а не гарантированный PDF сертификат | Указаны точный тип награды, 90 дней доступа и 70% на финальном экзамене |
| HF старая выдача перенесена | В план внесён работающий unit_1_quiz; название награды ограничено Unit 1 |
| TAU pytest недоступен в браузере | Не включён в обязательный путь |
| 8 адресов ведут через перенаправление | Подставлены проверенные конечные страницы; SDPA закреплена на открывшейся документации PyTorch 2.14, для работы сверять свою версию |
| Старый syllabus ссылался на три отсутствующих exam-файла | Заменены на существующие разделы exams/MASTER_EXAMS.md |
| README предлагал параллельные треки, roadmap обесценивал сертификаты | Одна очередь из четырёх этапов; награда курса и рабочий результат учитываются отдельно |
| Исторические проценты и Phase 0 выглядели как текущий статус | Перенесены в явно отмеченный архив PROGRESS; текущая очередь без выдуманных завершений |

## Реестр исходных 80 ссылок

«Проверен материал» означает, что получена соответствующая страница, а не только HTTP-статус. Это не обещание бесплатного курса, лаборатории или сертификата.

| № | Исходный ресурс / URL | Наблюдение и решение |
|---:|---|---|
| 1 | [An Even Easier Introduction to CUDA — обновлённая статья NVIDIA](https://developer.nvidia.com/blog/even-easier-introduction-cuda/) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 2 | [NVIDIA Accelerated Python Tutorial](https://github.com/NVIDIA/accelerated-computing-hub/tree/main/tutorials/accelerated-python) | GitHub API: получен README и перечень notebooks. Открытый tutorial, GPU-упражнения не запускались; сертификат не заявлен. |
| 3 | [Fundamentals of Accelerated Computing With CUDA Python](https://learn.nvidia.com/courses/course-detail?course_id=course-v1%3ADLI+S-AC-10+V1) | Браузер: название, активная Buy Now, $90 / 8 ч; assessment даёт сертификат. Основной этап 1. |
| 4 | [Sizing LLM Inference Systems](https://learn.nvidia.com/courses/course-detail?course_id=course-v1%3ADLI+S-FX-18+V1) | Браузер: retirement; запись до 7 июля, доступ до 31 декабря (год в баннере не указан); Buy Now/Redeem отключены. Исключён. |
| 5 | [Optimizing CUDA Machine Learning Codes With NVIDIA Nsight Profiling Tools](https://learn.nvidia.com/courses/course-detail?course_id=course-v1%3ADLI+S-AC-03+V2) | Браузер: Buy Now активна, $30 / 2 ч; сертификат на карточке не подтверждён. Только факультатив. |
| 6 | [Find the Bottleneck: Optimize AI Pipelines With Nsight Systems](https://learn.nvidia.com/courses/course-detail?course_id=course-v1%3ADLI+S-AC-14+V1) | Браузер: Buy Now активна, $30 / 3 ч, advanced; сертификат не подтверждён. Только факультатив. |
| 7 | [NVIDIA Learning Paths](https://www.nvidia.com/en-us/learn/learning-paths/) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 8 | [NVIDIA GPU Performance Background](https://docs.nvidia.com/deeplearning/performance/dl-performance-gpu-background/index.html) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 9 | [CUDA Programming Guide: Introduction / Programming Model](https://docs.nvidia.com/cuda/cuda-programming-guide/) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 10 | [NVIDIA CUDA samples](https://github.com/NVIDIA/cuda-samples) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 11 | [CUDA Best Practices Guide](https://docs.nvidia.com/cuda/cuda-c-best-practices-guide/) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 12 | [PyTorch Basics](https://docs.pytorch.org/tutorials/beginner/basics/) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 13 | [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 14 | [Hugging Face LLM Course](https://huggingface.co/learn/llm-course/chapter1/1) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 15 | [PyTorch scaled dot product attention](https://docs.pytorch.org/docs/stable/generated/torch.nn.functional.scaled_dot_product_attention.html) | Проверен конечный материал; рабочая ссылка обновлена: [открыть](https://docs.pytorch.org/docs/2.14/generated/torch.nn.functional.scaled_dot_product_attention.html). |
| 16 | [vLLM docs](https://docs.vllm.ai/en/latest/) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 17 | [SGLang docs](https://docs.sglang.ai/) | Проверен конечный материал; рабочая ссылка обновлена: [открыть](https://docs.sglang.io/). |
| 18 | [Nsight Systems](https://docs.nvidia.com/nsight-systems/UserGuide/) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 19 | [Nsight Compute](https://docs.nvidia.com/nsight-compute/) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 20 | [PyTorch Profiler](https://docs.pytorch.org/tutorials/beginner/profiler.html) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 21 | [Programming Massively Parallel Processors (Hwu, Kirk, El Hajj)](https://www.elsevier.com/books/programming-massively-parallel-processors/hwu/978-0-323-91231-0) | Проверен конечный материал; рабочая ссылка обновлена: [открыть](https://shop.elsevier.com/books/programming-massively-parallel-processors/hwu/978-0-323-91231-0). |
| 22 | [Pro Git](https://git-scm.com/book/en/v2) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 23 | [GitLab CI quick start](https://docs.gitlab.com/ci/quick_start/) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 24 | [YAML reference](https://docs.gitlab.com/ci/yaml/) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 25 | [Runner](https://docs.gitlab.com/runner/) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 26 | [Environments](https://docs.gitlab.com/ci/environments/) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 27 | [deployment safety](https://docs.gitlab.com/ci/environments/deployment_safety/) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 28 | [Google SRE Book: SLI/SLO](https://sre.google/sre-book/service-level-objectives/) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 29 | [OpenTelemetry concepts](https://opentelemetry.io/docs/concepts/) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 30 | [Prometheus getting started](https://prometheus.io/docs/prometheus/latest/getting_started/) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 31 | [Grafana fundamentals](https://grafana.com/tutorials/grafana-fundamentals/) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 32 | [pytest getting started](https://docs.pytest.org/en/stable/getting-started.html) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 33 | [Playwright](https://playwright.dev/docs/intro) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 34 | [Google ML Crash Course: classification](https://developers.google.com/machine-learning/crash-course/classification/accuracy-precision-recall) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 35 | [NIST AI RMF](https://www.nist.gov/itl/ai-risk-management-framework) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 36 | [Python tutorial](https://docs.python.org/3/tutorial/) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 37 | [typing](https://docs.python.org/3/library/typing.html) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 38 | [asyncio](https://docs.python.org/3/library/asyncio.html) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 39 | [FastAPI tutorial](https://fastapi.tiangolo.com/tutorial/) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 40 | [Pydantic docs](https://docs.pydantic.dev/latest/) | Проверен конечный материал; рабочая ссылка обновлена: [открыть](https://pydantic.dev/docs/validation/latest/get-started/). |
| 41 | [SQLAlchemy 2.0 tutorial](https://docs.sqlalchemy.org/en/20/tutorial/) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 42 | [Alembic](https://alembic.sqlalchemy.org/en/latest/tutorial.html) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 43 | [Architecture Patterns with Python](https://www.cosmicpython.com/book/preface.html) | Проверен конечный материал; рабочая ссылка обновлена: [открыть](https://www.cosmicpython.com/book/preface). |
| 44 | [PostgreSQL tutorial](https://www.postgresql.org/docs/current/tutorial.html) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 45 | [Transactions](https://www.postgresql.org/docs/current/tutorial-transactions.html) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 46 | [EXPLAIN](https://www.postgresql.org/docs/current/using-explain.html) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 47 | [Indexes](https://www.postgresql.org/docs/current/indexes.html) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 48 | [MVCC](https://www.postgresql.org/docs/current/mvcc.html) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 49 | [The Art of PostgreSQL](https://theartofpostgresql.com/) | Доступна страница книги/издателя; это не подтверждение доступа к полной платной книге. Учебная награда не заявлена. |
| 50 | [The Linux Command Line](https://linuxcommand.org/tlcl.php) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 51 | [systemd docs](https://systemd.io/) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 52 | [Docker overview](https://docs.docker.com/get-started/docker-overview/) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 53 | [Compose](https://docs.docker.com/compose/) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 54 | [Podman docs](https://docs.podman.io/en/latest/) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 55 | [NVIDIA Container Toolkit](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 56 | [MDN Learn web development](https://developer.mozilla.org/en-US/docs/Learn_web_development) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 57 | [TypeScript Handbook](https://www.typescriptlang.org/docs/handbook/intro.html) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 58 | [React Learn](https://react.dev/learn) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 59 | [Next.js Learn](https://nextjs.org/learn) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 60 | [WAI accessibility tutorials](https://www.w3.org/WAI/tutorials/) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 61 | [OWASP Top 10](https://owasp.org/www-project-top-ten/) | Проверен конечный материал; рабочая ссылка обновлена: [открыть](https://owasp.org/projects/top-ten). |
| 62 | [OWASP API Security Top 10](https://owasp.org/API-Security/) | Проверен конечный материал; рабочая ссылка обновлена: [открыть](https://api-security.owasp.org/). |
| 63 | [OWASP LLM Top 10](https://genai.owasp.org/llm-top-10/) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 64 | [NIST SSDF](https://csrc.nist.gov/Projects/ssdf) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 65 | [OAuth 2.0 Security BCP](https://www.rfc-editor.org/rfc/rfc9700) | Проверен конечный материал; рабочая ссылка обновлена: [открыть](https://www.rfc-editor.org/info/rfc9700/). |
| 66 | [Google ML Crash Course](https://developers.google.com/machine-learning/crash-course) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 67 | [Hugging Face PEFT](https://huggingface.co/docs/peft/index) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 68 | [Hugging Face TRL](https://huggingface.co/docs/trl/index) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 69 | [Stanford IR book](https://nlp.stanford.edu/IR-book/) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 70 | [Qdrant docs](https://qdrant.tech/documentation/) | Проверены содержимое и назначение страницы. Документация Qdrant; сертификат здесь не заявлен. |
| 71 | [Build a Large Language Model (From Scratch)](https://www.manning.com/books/build-a-large-language-model-from-scratch) | Доступна страница книги/издателя; это не подтверждение доступа к полной платной книге. Учебная награда не заявлена. |
| 72 | [Building RAG Agents With LLMs](https://learn.nvidia.com/courses/course-detail?course_id=course-v1%3ADLI+S-FX-15+V1) | Браузер: Buy Now активна, $90 / 8 ч; assessment/certification в программе. NCP-страница также указывает course certificate. Основной этап 4. |
| 73 | [Evaluating RAG and Semantic Search Systems](https://learn.nvidia.com/courses/course-detail?course_id=course-v1%3ADLI+S-FX-32+V1) | Браузер: Buy Now активна, $30 / 3 ч; сертификат не подтверждён. Только факультатив. |
| 74 | [Introduction to Deploying RAG Pipelines for Production at Scale](https://learn.nvidia.com/courses/course-detail?course_id=course-v1%3ADLI+S-FX-19+V1) | Браузер: Buy Now активна, $90 / 4 ч. Обзор NCP иначе описывает похожий курс; сертификат этой версии не подтверждён. Только факультатив. |
| 75 | [Adding New Knowledge to LLMs](https://learn.nvidia.com/courses/course-detail?course_id=course-v1%3ADLI+C-FX-26+V1) | Браузер: заголовок [Access Expires: 2026/12/31], instructor-led; самостоятельная запись не подтверждена. Исключён из очереди. |
| 76 | [Сертификация NCA-GENL](https://www.nvidia.com/en-us/learn/certification/generative-ai-llm-associate/) | Страница экзамена: есть Register for Exam, badge и optional certificate. Запись в аккаунте/регионе не проверена; факультатив. |
| 77 | [NCP-GENL](https://www.nvidia.com/en-us/learn/certification/generative-ai-llm-professional/) | Браузер: Register for Exam присутствует, badge/optional certificate заявлены. Внешний экзаменационный кабинет не проверен; факультатив. |
| 78 | [AI Engineering (Chip Huyen)](https://www.oreilly.com/library/view/ai-engineering/9781098166298/) | Доступна страница книги/издателя; это не подтверждение доступа к полной платной книге. Учебная награда не заявлена. |
| 79 | [Google engineering practices: code review](https://google.github.io/eng-practices/review/) | Проверены содержимое и назначение страницы. Справочник / учебный материал; выдача наград в этом аудите не подтверждается. |
| 80 | [The Manager's Path](https://www.oreilly.com/library/view/the-managers-path/9781491973882/) | Доступна страница книги/издателя; это не подтверждение доступа к полной платной книге. Учебная награда не заявлена. |

## Ранее исключённый курс

| Ресурс | Наблюдение |
|---|---|
| [T-AC-01: An Even Easier Introduction to CUDA](https://learn.nvidia.com/courses/course-detail?course_id=course-v1%3ADLI+T-AC-01+V1) | Браузер: retirement, запись до 7 июля, доступ до 31 декабря; год в этом баннере не указан. Enroll Now отключена. В основной путь не возвращён |

## Реестр 29 новых адресов

Все проверены 24.09.2026. Для входа в закрытые задания по-прежнему нужен аккаунт.

| № | Ресурс / URL | Проверка |
|---:|---|---|
| 1 | [GitLab CI/CD Associate Learning Path](https://university.gitlab.com/learning-paths/gitlab-certified-cicd-associate-learning-path) | Браузер: пять учебных блоков и ссылки на них. Сертификационный экзамен оплачивается отдельно. |
| 2 | [экзамен](https://university.gitlab.com/courses/gitlab-certified-cicd-associate) | Браузер: активная Enroll Now; $150 non-member / $120 member, 14 дней, две попытки. |
| 3 | [Linux Foundation: Introduction to DevOps and Site Reliability Engineering — LFS162](https://training.linuxfoundation.org/training/introduction-to-devops-and-site-reliability-engineering-lfs162/) | Карточка: бесплатно, 10–12 ч, доступ 90 дней, digital badge; ссылка Enroll Today. |
| 4 | [условия доступа и список стран](https://www.nvidia.com/en-us/learn/training/support/) | Прочитаны ограничения по странам, доступу, сертификатам и MyLearning. |
| 5 | [Правила и выдача наград GitLab](https://university.gitlab.com/learn/article/gitlab-certification-candidate-handbook) | Браузер: требования, 75% pass, сертификат + Credly, запрет AI на экзамене. |
| 6 | [Вход в курс](https://trainingportal.linuxfoundation.org/courses/introduction-to-devops-and-site-reliability-engineering-lfs162) | Браузер: карточка курса и Register Now. Завершение/экзамен внутри аккаунта не тестировались. |
| 7 | [критерий выдачи badge](https://www.credly.com/org/the-linux-foundation/badge/lfs162-introduction-to-devops-and-site-reliability-) | Badge издателя: Cost Free, критерий финального экзамена 70%. |
| 8 | [CS50P](https://cs50.harvard.edu/python/) | Открыты программа и задания; запись/отправка работ через личный аккаунт не выполнялась. |
| 9 | [Бесплатный CS50 Certificate](https://cs50.harvard.edu/python/certificate/) | Официальные условия бесплатного CS50 Certificate: ≥70% на каждой задаче и проекте. |
| 10 | [CS50 SQL](https://cs50.harvard.edu/sql/) | Открыты программа и задания; запись/отправка работ через личный аккаунт не выполнялась. |
| 11 | [Бесплатный сертификат](https://cs50.harvard.edu/sql/certificate/) | Официальные условия бесплатного CS50 Certificate: ≥70% на каждой задаче и проекте. |
| 12 | [Full Stack Open](https://fullstackopen.com/en/) | Открыта программа. Бесплатный длинный web-трек; изучать по потребности. |
| 13 | [Правила сертификата](https://fullstackopen.com/en/part0/general_info) | Проверены prerequisites, упражнения, скачивание сертификата; credits/exam — отдельный путь. |
| 14 | [CS50 Cybersecurity](https://cs50.harvard.edu/cybersecurity/) | Открыты программа и задания; запись/отправка работ через личный аккаунт не выполнялась. |
| 15 | [Бесплатный сертификат](https://cs50.harvard.edu/cybersecurity/certificate/) | Официальные условия бесплатного CS50 Certificate: ≥70% на каждой задаче и проекте. |
| 16 | [Hugging Face Agents, Unit 1](https://huggingface.co/learn/agents-course/unit1/introduction) | Материалы Unit 1 открыты; это только Fundamentals certificate. |
| 17 | [актуальное приложение quiz](https://huggingface.co/spaces/agents-course/unit_1_quiz) | Браузер: приложение Running on CPU, видны login/start; выдача после quiz не тестировалась. |
| 18 | [Certificate of Fundamentals](https://huggingface.co/learn/agents-course/unit1/get-your-certificate) | Прочитаны условия ≥80%; старое приложение сообщает о переносе. Использован новый unit_1_quiz. |
| 19 | [TAU Introduction to pytest](https://testautomationu.applitools.com/pytest-tutorial/) | Поиск читает программу; браузер дважды: Site Unavailable. Отложен, не обязательный курс. |
| 20 | [PyTorch scaled dot product attention](https://docs.pytorch.org/docs/2.14/generated/torch.nn.functional.scaled_dot_product_attention.html) | Конечная страница проверена после перехода; заменяет старый адрес. |
| 21 | [SGLang docs](https://docs.sglang.io/) | Конечная страница проверена после перехода; заменяет старый адрес. |
| 22 | [Programming Massively Parallel Processors (Hwu, Kirk, El Hajj)](https://shop.elsevier.com/books/programming-massively-parallel-processors/hwu/978-0-323-91231-0) | Конечная страница проверена после перехода; заменяет старый адрес. |
| 23 | [Pydantic docs](https://pydantic.dev/docs/validation/latest/get-started/) | Конечная страница проверена после перехода; заменяет старый адрес. |
| 24 | [Architecture Patterns with Python](https://www.cosmicpython.com/book/preface) | Конечная страница проверена после перехода; заменяет старый адрес. |
| 25 | [OWASP Top 10](https://owasp.org/projects/top-ten) | Конечная страница проверена после перехода; заменяет старый адрес. |
| 26 | [OWASP API Security Top 10](https://api-security.owasp.org/) | Конечная страница проверена после перехода; заменяет старый адрес. |
| 27 | [OAuth 2.0 Security BCP](https://www.rfc-editor.org/info/rfc9700/) | Конечная страница проверена после перехода; заменяет старый адрес. |
| 28 | [Инструкция скачивания изображения](https://support.credly.com/hc/en-us/articles/360020965172-Can-I-download-my-badge-image) | Официальная инструкция скачивания выданного badge image. |
| 29 | [PDF сертификата](https://support.credly.com/hc/en-us/articles/360026639872-Can-I-download-and-print-my-badge-certificate) | Прочитаны условия PDF: зависит от издателя; требуются публичные профиль и badge. |

## Проверка содержания плана

- Сохранены все 11 дисциплин, порядок чтения и конкретные рабочие результаты. Они не превращены в 11 одновременно обязательных программ.
- Основной маршрут: CUDA Python → Git/CI/CD → SRE → RAG. Python/NumPy проверяются перед CUDA; Python/OOP и основы deep learning — перед RAG.
- Для CUDA Python указана Numba-ориентация; курс не выдаётся за полный курс архитектуры LLM inference.
- Формула KV ограничена обычным attention. Для MLA, sliding window, гибридных моделей и распределения по GPU требуется проверка реализации.
- У internal mastery exams нет внешней аккредитации или провайдерского сертификата.
- Нет отметок о фактическом прохождении, новых процентах навыков или уже выданных наградах.
- Правила AI для рабочих проектов отделены от ограничений graded assessments.
- Бесплатный CS50 Certificate отделён от платного verified edX. Badge отделён от PDF. Профессиональный экзамен отделён от course certificate.

## Как обновлять этот аудит

Перед следующим стартом открыть конкретную карточку и проверить запись, expiry и награду. При новом retirement, недоступности или изменении выдачи награды убрать ресурс из активной очереди и сохранить причину с датой. Автоматический HTTP-check полезен для 404, но не доказывает возможность пройти курс.

[Вернуться к маршруту](WORK_INTEGRATED_ROADMAP.md) · [Сохранение и печать наград](CREDENTIALS.md)
