<a id="аудит-roadmap-и-ссылок--24092026"></a>

# Roadmap and link audit — September 24, 2026

<a id="объём-и-метод"></a>

## Scope and method

- Original version: commit `d678caa80a64e3b44a77df10762a4e3aacdf527b`.
- Read all **16 Markdown files** in the repository; found **80 unique external Markdown links**, all in WORK_INTEGRATED_ROADMAP.md.
- Checked every original external link by opening the page. For dynamic NVIDIA/GitLab pages, used a browser with loaded content; for the open NVIDIA tutorial, used the GitHub API after the text web view failed.
- Separately checked the previously removed T-AC-01. In total, **9 DLI listings** were viewed in the browser.
- Checked **29 new addresses**, including 8 final destinations replacing redirects. Together with T-AC-01, the registry below contains **110 unique external addresses**. Utility links within provider websites are not automatically counted as checked.
- For courses, separately examined the title/version, retirement warnings, enrollment/purchase button, syllabus, prerequisites, award, and access conditions.
- For books, checked the publisher/author page; access to the full paid book was not purchased.

**Verification limits:** a public listing and a working registration entry point do not demonstrate successful payment, availability in a specific country, working labs, or future certificate issuance in an account. Registration, purchases, assessments, and printing earned awards were not performed. Reading a website does not mean completing a course. The date matters: providers may change their terms later.

<a id="что-исправлено-в-маршруте"></a>

## What was corrected in the route

| Issue | Resolution |
|---|---|
| T-AC-01: enrollment disabled, retirement banner | Removed; the first certificate course is CUDA Python. The open CUDA article is retained as material without a certificate |
| S-FX-18 Sizing LLM Inference Systems: enrollment also disabled | Removed. Sizing is studied through documentation and your own benchmark |
| C-FX-26 Adding New Knowledge: access expires December 31, 2026 | Removed from the main queue; not scheduled for the distant future |
| S-AC-03 / S-AC-14 / S-FX-32: purchase available, certificate unconfirmed | Optional for their content only, with no promised award |
| S-FX-19: the listing and NCP overview differ on a similar course | Do not promise a certificate for this specific version |
| The GitLab exam has a short access window | Prepare before purchasing; 14 days and two attempts are stated explicitly |
| LFS162 awards a badge, not a guaranteed PDF certificate | The exact award type, 90 days of access, and 70% on the final exam are specified |
| The old HF award app moved | The working unit_1_quiz is included in the plan; the award name is limited to Unit 1 |
| TAU pytest unavailable in the browser | Excluded from the required path |
| 8 addresses lead through redirects | Replaced with verified final pages; SDPA is pinned to the PyTorch 2.14 documentation that opened—check your own version for work |
| The old syllabus linked to three missing exam files | Replaced with existing sections in exams/MASTER_EXAMS.md |
| README proposed parallel tracks; the roadmap devalued certificates | One four-stage queue; course awards and work results are recorded separately |
| Historical percentages and Phase 0 looked like current status | Moved into a clearly marked PROGRESS archive; the current queue has no invented completions |

<a id="реестр-исходных-80-ссылок"></a>

## Registry of the 80 original links

“Material checked” means the relevant page was retrieved, not just its HTTP status. This does not promise a free course, lab, or certificate.

| No. | Original resource / URL | Observation and decision |
|---:|---|---|
| 1 | [An Even Easier Introduction to CUDA — updated NVIDIA article](https://developer.nvidia.com/blog/even-easier-introduction-cuda/) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 2 | [NVIDIA Accelerated Python Tutorial](https://github.com/NVIDIA/accelerated-computing-hub/tree/main/tutorials/accelerated-python) | GitHub API: retrieved the README and notebook list. Open tutorial; GPU exercises were not run; no certificate is advertised. |
| 3 | [Fundamentals of Accelerated Computing With CUDA Python](https://learn.nvidia.com/courses/course-detail?course_id=course-v1%3ADLI+S-AC-10+V1) | Browser: title, active Buy Now, $90 / 8 hours; the assessment awards a certificate. Main stage 1. |
| 4 | [Sizing LLM Inference Systems](https://learn.nvidia.com/courses/course-detail?course_id=course-v1%3ADLI+S-FX-18+V1) | Browser: retirement; enrollment until July 7, access until December 31 (no year stated in the banner); Buy Now/Redeem disabled. Removed. |
| 5 | [Optimizing CUDA Machine Learning Codes With NVIDIA Nsight Profiling Tools](https://learn.nvidia.com/courses/course-detail?course_id=course-v1%3ADLI+S-AC-03+V2) | Browser: Buy Now active, $30 / 2 hours; the listing does not confirm a certificate. Optional only. |
| 6 | [Find the Bottleneck: Optimize AI Pipelines With Nsight Systems](https://learn.nvidia.com/courses/course-detail?course_id=course-v1%3ADLI+S-AC-14+V1) | Browser: Buy Now active, $30 / 3 hours, advanced; certificate unconfirmed. Optional only. |
| 7 | [NVIDIA Learning Paths](https://www.nvidia.com/en-us/learn/learning-paths/) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 8 | [NVIDIA GPU Performance Background](https://docs.nvidia.com/deeplearning/performance/dl-performance-gpu-background/index.html) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 9 | [CUDA Programming Guide: Introduction / Programming Model](https://docs.nvidia.com/cuda/cuda-programming-guide/) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 10 | [NVIDIA CUDA samples](https://github.com/NVIDIA/cuda-samples) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 11 | [CUDA Best Practices Guide](https://docs.nvidia.com/cuda/cuda-c-best-practices-guide/) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 12 | [PyTorch Basics](https://docs.pytorch.org/tutorials/beginner/basics/) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 13 | [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 14 | [Hugging Face LLM Course](https://huggingface.co/learn/llm-course/chapter1/1) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 15 | [PyTorch scaled dot product attention](https://docs.pytorch.org/docs/stable/generated/torch.nn.functional.scaled_dot_product_attention.html) | The destination material was checked; the working link was updated: [open](https://docs.pytorch.org/docs/2.14/generated/torch.nn.functional.scaled_dot_product_attention.html). |
| 16 | [vLLM docs](https://docs.vllm.ai/en/latest/) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 17 | [SGLang docs](https://docs.sglang.ai/) | The destination material was checked; the working link was updated: [open](https://docs.sglang.io/). |
| 18 | [Nsight Systems](https://docs.nvidia.com/nsight-systems/UserGuide/) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 19 | [Nsight Compute](https://docs.nvidia.com/nsight-compute/) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 20 | [PyTorch Profiler](https://docs.pytorch.org/tutorials/beginner/profiler.html) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 21 | [Programming Massively Parallel Processors (Hwu, Kirk, El Hajj)](https://www.elsevier.com/books/programming-massively-parallel-processors/hwu/978-0-323-91231-0) | The destination material was checked; the working link was updated: [open](https://shop.elsevier.com/books/programming-massively-parallel-processors/hwu/978-0-323-91231-0). |
| 22 | [Pro Git](https://git-scm.com/book/en/v2) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 23 | [GitLab CI quick start](https://docs.gitlab.com/ci/quick_start/) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 24 | [YAML reference](https://docs.gitlab.com/ci/yaml/) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 25 | [Runner](https://docs.gitlab.com/runner/) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 26 | [Environments](https://docs.gitlab.com/ci/environments/) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 27 | [deployment safety](https://docs.gitlab.com/ci/environments/deployment_safety/) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 28 | [Google SRE Book: SLI/SLO](https://sre.google/sre-book/service-level-objectives/) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 29 | [OpenTelemetry concepts](https://opentelemetry.io/docs/concepts/) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 30 | [Prometheus getting started](https://prometheus.io/docs/prometheus/latest/getting_started/) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 31 | [Grafana fundamentals](https://grafana.com/tutorials/grafana-fundamentals/) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 32 | [pytest getting started](https://docs.pytest.org/en/stable/getting-started.html) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 33 | [Playwright](https://playwright.dev/docs/intro) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 34 | [Google ML Crash Course: classification](https://developers.google.com/machine-learning/crash-course/classification/accuracy-precision-recall) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 35 | [NIST AI RMF](https://www.nist.gov/itl/ai-risk-management-framework) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 36 | [Python tutorial](https://docs.python.org/3/tutorial/) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 37 | [typing](https://docs.python.org/3/library/typing.html) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 38 | [asyncio](https://docs.python.org/3/library/asyncio.html) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 39 | [FastAPI tutorial](https://fastapi.tiangolo.com/tutorial/) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 40 | [Pydantic docs](https://docs.pydantic.dev/latest/) | The destination material was checked; the working link was updated: [open](https://pydantic.dev/docs/validation/latest/get-started/). |
| 41 | [SQLAlchemy 2.0 tutorial](https://docs.sqlalchemy.org/en/20/tutorial/) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 42 | [Alembic](https://alembic.sqlalchemy.org/en/latest/tutorial.html) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 43 | [Architecture Patterns with Python](https://www.cosmicpython.com/book/preface.html) | The destination material was checked; the working link was updated: [open](https://www.cosmicpython.com/book/preface). |
| 44 | [PostgreSQL tutorial](https://www.postgresql.org/docs/current/tutorial.html) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 45 | [Transactions](https://www.postgresql.org/docs/current/tutorial-transactions.html) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 46 | [EXPLAIN](https://www.postgresql.org/docs/current/using-explain.html) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 47 | [Indexes](https://www.postgresql.org/docs/current/indexes.html) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 48 | [MVCC](https://www.postgresql.org/docs/current/mvcc.html) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 49 | [The Art of PostgreSQL](https://theartofpostgresql.com/) | The book/publisher page is available; this does not confirm access to the full paid book. No learning award is advertised. |
| 50 | [The Linux Command Line](https://linuxcommand.org/tlcl.php) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 51 | [systemd docs](https://systemd.io/) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 52 | [Docker overview](https://docs.docker.com/get-started/docker-overview/) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 53 | [Compose](https://docs.docker.com/compose/) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 54 | [Podman docs](https://docs.podman.io/en/latest/) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 55 | [NVIDIA Container Toolkit](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 56 | [MDN Learn web development](https://developer.mozilla.org/en-US/docs/Learn_web_development) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 57 | [TypeScript Handbook](https://www.typescriptlang.org/docs/handbook/intro.html) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 58 | [React Learn](https://react.dev/learn) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 59 | [Next.js Learn](https://nextjs.org/learn) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 60 | [WAI accessibility tutorials](https://www.w3.org/WAI/tutorials/) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 61 | [OWASP Top 10](https://owasp.org/www-project-top-ten/) | The destination material was checked; the working link was updated: [open](https://owasp.org/projects/top-ten). |
| 62 | [OWASP API Security Top 10](https://owasp.org/API-Security/) | The destination material was checked; the working link was updated: [open](https://api-security.owasp.org/). |
| 63 | [OWASP LLM Top 10](https://genai.owasp.org/llm-top-10/) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 64 | [NIST SSDF](https://csrc.nist.gov/Projects/ssdf) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 65 | [OAuth 2.0 Security BCP](https://www.rfc-editor.org/rfc/rfc9700) | The destination material was checked; the working link was updated: [open](https://www.rfc-editor.org/info/rfc9700/). |
| 66 | [Google ML Crash Course](https://developers.google.com/machine-learning/crash-course) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 67 | [Hugging Face PEFT](https://huggingface.co/docs/peft/index) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 68 | [Hugging Face TRL](https://huggingface.co/docs/trl/index) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 69 | [Stanford IR book](https://nlp.stanford.edu/IR-book/) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 70 | [Qdrant docs](https://qdrant.tech/documentation/) | The page content and purpose were checked. Qdrant documentation; no certificate is advertised here. |
| 71 | [Build a Large Language Model (From Scratch)](https://www.manning.com/books/build-a-large-language-model-from-scratch) | The book/publisher page is available; this does not confirm access to the full paid book. No learning award is advertised. |
| 72 | [Building RAG Agents With LLMs](https://learn.nvidia.com/courses/course-detail?course_id=course-v1%3ADLI+S-FX-15+V1) | Browser: Buy Now active, $90 / 8 hours; assessment/certification in the syllabus. The NCP page also lists a course certificate. Main stage 4. |
| 73 | [Evaluating RAG and Semantic Search Systems](https://learn.nvidia.com/courses/course-detail?course_id=course-v1%3ADLI+S-FX-32+V1) | Browser: Buy Now active, $30 / 3 hours; certificate unconfirmed. Optional only. |
| 74 | [Introduction to Deploying RAG Pipelines for Production at Scale](https://learn.nvidia.com/courses/course-detail?course_id=course-v1%3ADLI+S-FX-19+V1) | Browser: Buy Now active, $90 / 4 hours. The NCP overview describes a similar course differently; the certificate for this version is unconfirmed. Optional only. |
| 75 | [Adding New Knowledge to LLMs](https://learn.nvidia.com/courses/course-detail?course_id=course-v1%3ADLI+C-FX-26+V1) | Browser: title [Access Expires: 2026/12/31], instructor-led; self-enrollment unconfirmed. Removed from the queue. |
| 76 | [NCA-GENL certification](https://www.nvidia.com/en-us/learn/certification/generative-ai-llm-associate/) | Exam page: Register for Exam, badge, and optional certificate are present. Enrollment in the account/region was not checked; optional. |
| 77 | [NCP-GENL](https://www.nvidia.com/en-us/learn/certification/generative-ai-llm-professional/) | Browser: Register for Exam is present; a badge/optional certificate is advertised. The external exam account was not checked; optional. |
| 78 | [AI Engineering (Chip Huyen)](https://www.oreilly.com/library/view/ai-engineering/9781098166298/) | The book/publisher page is available; this does not confirm access to the full paid book. No learning award is advertised. |
| 79 | [Google engineering practices: code review](https://google.github.io/eng-practices/review/) | The page content and purpose were checked. Reference / learning material; award issuance is not confirmed by this audit. |
| 80 | [The Manager's Path](https://www.oreilly.com/library/view/the-managers-path/9781491973882/) | The book/publisher page is available; this does not confirm access to the full paid book. No learning award is advertised. |

<a id="ранее-исключённый-курс"></a>

## Previously excluded course

| Resource | Observation |
|---|---|
| [T-AC-01: An Even Easier Introduction to CUDA](https://learn.nvidia.com/courses/course-detail?course_id=course-v1%3ADLI+T-AC-01+V1) | Browser: retirement, enrollment until July 7, access until December 31; the year is not stated in this banner. Enroll Now is disabled. Not restored to the main path |

<a id="реестр-29-новых-адресов"></a>

## Registry of 29 new addresses

All checked on September 24, 2026. Access to private assignments still requires an account.

| No. | Resource / URL | Check |
|---:|---|---|
| 1 | [GitLab CI/CD Associate Learning Path](https://university.gitlab.com/learning-paths/gitlab-certified-cicd-associate-learning-path) | Browser: five learning blocks and links to them. The certification exam is purchased separately. |
| 2 | [exam](https://university.gitlab.com/courses/gitlab-certified-cicd-associate) | Browser: active Enroll Now; $150 non-member / $120 member, 14 days, two attempts. |
| 3 | [Linux Foundation: Introduction to DevOps and Site Reliability Engineering — LFS162](https://training.linuxfoundation.org/training/introduction-to-devops-and-site-reliability-engineering-lfs162/) | Listing: free, 10–12 hours, 90 days of access, digital badge; Enroll Today link. |
| 4 | [access conditions and country list](https://www.nvidia.com/en-us/learn/training/support/) | Read the restrictions concerning countries, access, certificates, and MyLearning. |
| 5 | [GitLab rules and award issuance](https://university.gitlab.com/learn/article/gitlab-certification-candidate-handbook) | Browser: requirements, 75% pass, certificate + Credly, AI prohibited during the exam. |
| 6 | [Course entry point](https://trainingportal.linuxfoundation.org/courses/introduction-to-devops-and-site-reliability-engineering-lfs162) | Browser: course listing and Register Now. Completion/exam within the account were not tested. |
| 7 | [badge issuance criterion](https://www.credly.com/org/the-linux-foundation/badge/lfs162-introduction-to-devops-and-site-reliability-) | Issuer's badge: Cost Free, final exam criterion 70%. |
| 8 | [CS50P](https://cs50.harvard.edu/python/) | Opened the syllabus and assignments; enrollment/submission through a personal account were not performed. |
| 9 | [Free CS50 Certificate](https://cs50.harvard.edu/python/certificate/) | Official free CS50 Certificate requirements: ≥70% on every problem/assignment and the project. |
| 10 | [CS50 SQL](https://cs50.harvard.edu/sql/) | Opened the syllabus and assignments; enrollment/submission through a personal account were not performed. |
| 11 | [Free certificate](https://cs50.harvard.edu/sql/certificate/) | Official free CS50 Certificate requirements: ≥70% on every problem/assignment and the project. |
| 12 | [Full Stack Open](https://fullstackopen.com/en/) | Opened the syllabus. A long, free web track; study as needed. |
| 13 | [Certificate rules](https://fullstackopen.com/en/part0/general_info) | Checked prerequisites, exercises, and certificate download; credits/exam are a separate path. |
| 14 | [CS50 Cybersecurity](https://cs50.harvard.edu/cybersecurity/) | Opened the syllabus and assignments; enrollment/submission through a personal account were not performed. |
| 15 | [Free certificate](https://cs50.harvard.edu/cybersecurity/certificate/) | Official free CS50 Certificate requirements: ≥70% on every problem/assignment and the project. |
| 16 | [Hugging Face Agents, Unit 1](https://huggingface.co/learn/agents-course/unit1/introduction) | Unit 1 materials are open; this is only the Fundamentals certificate. |
| 17 | [current quiz app](https://huggingface.co/spaces/agents-course/unit_1_quiz) | Browser: the app is Running on CPU, login/start are visible; issuance after the quiz was not tested. |
| 18 | [Certificate of Fundamentals](https://huggingface.co/learn/agents-course/unit1/get-your-certificate) | Read the ≥80% requirements; the old app reports a move. The new unit_1_quiz is used. |
| 19 | [TAU Introduction to pytest](https://testautomationu.applitools.com/pytest-tutorial/) | Search retrieves the syllabus; browser twice: Site Unavailable. Deferred, not a required course. |
| 20 | [PyTorch scaled dot product attention](https://docs.pytorch.org/docs/2.14/generated/torch.nn.functional.scaled_dot_product_attention.html) | The destination page was checked after following the redirect; it replaces the old address. |
| 21 | [SGLang docs](https://docs.sglang.io/) | The destination page was checked after following the redirect; it replaces the old address. |
| 22 | [Programming Massively Parallel Processors (Hwu, Kirk, El Hajj)](https://shop.elsevier.com/books/programming-massively-parallel-processors/hwu/978-0-323-91231-0) | The destination page was checked after following the redirect; it replaces the old address. |
| 23 | [Pydantic docs](https://pydantic.dev/docs/validation/latest/get-started/) | The destination page was checked after following the redirect; it replaces the old address. |
| 24 | [Architecture Patterns with Python](https://www.cosmicpython.com/book/preface) | The destination page was checked after following the redirect; it replaces the old address. |
| 25 | [OWASP Top 10](https://owasp.org/projects/top-ten) | The destination page was checked after following the redirect; it replaces the old address. |
| 26 | [OWASP API Security Top 10](https://api-security.owasp.org/) | The destination page was checked after following the redirect; it replaces the old address. |
| 27 | [OAuth 2.0 Security BCP](https://www.rfc-editor.org/info/rfc9700/) | The destination page was checked after following the redirect; it replaces the old address. |
| 28 | [Image download instructions](https://support.credly.com/hc/en-us/articles/360020965172-Can-I-download-my-badge-image) | Official instructions for downloading an issued badge image. |
| 29 | [Certificate PDF](https://support.credly.com/hc/en-us/articles/360026639872-Can-I-download-and-print-my-badge-certificate) | Read the PDF conditions: depends on the issuer; a public profile and badge are required. |

<a id="проверка-содержания-плана"></a>

## Plan content check

- All 11 disciplines, reading order, and specific work outputs are preserved. They have not become 11 simultaneously required programs.
- Main route: CUDA Python → Git/CI/CD → SRE → RAG. Python/NumPy are checked before CUDA; Python/OOP and deep learning fundamentals before RAG.
- CUDA Python's Numba focus is stated; the course is not presented as a complete course on LLM inference architecture.
- The KV formula is limited to standard attention. MLA, sliding window, hybrid models, and distribution across GPUs require checking the implementation.
- Internal mastery exams have no external accreditation or provider certificate.
- There are no claims of actual completion, new skill percentages, or awards already issued.
- AI rules for work projects are separated from graded-assessment restrictions.
- The free CS50 Certificate is distinguished from paid verified edX. A badge is distinguished from a PDF. A professional exam is distinguished from a course certificate.

<a id="как-обновлять-этот-аудит"></a>

## How to update this audit

Before the next start, open the specific listing and check enrollment, expiry, and the award. If a new retirement notice, unavailability, or change in award issuance appears, remove the resource from the active queue and record the reason and date. An automated HTTP check helps find 404s, but does not prove that a course can be completed.

[Return to the roadmap](WORK_INTEGRATED_ROADMAP.md) · [Saving and printing awards](CREDENTIALS.md)

<a id="дополнение-согласование-всего-репозитория"></a>

## Addendum: repository-wide alignment

After the audit, the syllabus, modules, internal checks, AI rules, templates, and navigation were updated. The original syllabus was moved into a clearly marked archive. Details: [REPO_REVIEW_2026-09-24.md](REPO_REVIEW_2026-09-24.md).

The modules reuse addresses from this registry. The original 16/80 counts above describe the state before the first edit, not the current repository size. This structural revision is not a new check of labs, payment, or award issuance.
