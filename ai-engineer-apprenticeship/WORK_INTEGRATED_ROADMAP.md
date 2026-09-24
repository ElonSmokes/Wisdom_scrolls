<a id="рабочий-roadmap-ai-systems-engineering"></a>

# Work-integrated roadmap: AI systems engineering

Checked **September 24, 2026**. Development direction: **AI systems engineer / technical AI lead**—understand the computation, delivery, and quality of the systems you already manage. This is a skills target, not a level conferred by courses.

**Open only the first course in the table for now.** The queue has four stages. The 11 discipline sections below are a reference to consult for a specific task. The [previous 32-week syllabus](archive/LEGACY_32_WEEK_SYLLABUS.md) is archived; the [current syllabus](SYLLABUS.md) follows this queue.

<a id="основная-очередь-закончить-получить-награду-применить"></a>

## Main queue: finish, earn an award, apply the knowledge

| Order | Course / preparation | What you will earn | Price and pace |
|---|---|---|---|
| **1. CUDA** | [NVIDIA: Fundamentals of Accelerated Computing with CUDA Python](https://learn.nvidia.com/courses/course-detail?course_id=course-v1%3ADLI+S-AC-10+V1) | Course certificate after the assessment; then a small GPU benchmark | The listing shows **$90, 8 hours**. Allow 3–5 weeks for learning with exercises |
| **2. Git → GitLab CI/CD** | [Pro Git](https://git-scm.com/book/en/v2) → [GitLab CI/CD Associate Learning Path](https://university.gitlab.com/learning-paths/gitlab-certified-cicd-associate-learning-path) → [exam](https://university.gitlab.com/courses/gitlab-certified-cicd-associate) | After passing the exam: a GitLab certificate and Credly badge | Preparation is free; the regular exam price is **$150**, and the listing also shows a $120 member price. Plan 4–6 weeks of preparation |
| **3. DevOps / SRE** | [Linux Foundation: Introduction to DevOps and Site Reliability Engineering — LFS162](https://training.linuxfoundation.org/training/introduction-to-devops-and-site-reliability-engineering-lfs162/) | **Digital badge**, final exam ≥70%; after the course—a dashboard and runbook | **Free**, 10–12 hours of material; **90 days** of access. Plan 3–5 weeks |
| **4. RAG** | [NVIDIA: Building RAG Agents with LLMs](https://learn.nvidia.com/courses/course-detail?course_id=course-v1%3ADLI+S-FX-15+V1) | Course certificate after the final assessment; then a retrieval baseline with evaluation | The listing shows **$90, 8 hours**. Plan 4–6 weeks with practice |

The durations in weeks are our estimates at **3–5 hours per week**, not promises; the hours in course listings do not include all revision and work on your own project. Prices are a snapshot as of the check date; the final amount depends on your account and purchase terms. For the main-queue courses, public pages, registration/purchase entry points, and award descriptions were checked. Payment, private lab launches, and award issuance in your account were not performed.

<a id="этап-1-как-начать-cuda"></a>

### Stage 1: how to start CUDA

**Prerequisites:** Python—functions, loops, arrays; NumPy—ndarray and array operations. If you cannot yet explain simple code using these, first cover the relevant Python/NumPy topics in the course materials. The full CS50P course below is an option for systematically filling the gap, not a mandatory barrier lasting several months.

1. Complete the CUDA Python introduction: CPU/GPU, data transfers, Numba.
2. Complete custom kernels: thread/block/grid; predict which array element a thread processes.
3. Complete multidimensional grids and shared memory. Check correctness, then measure after warmup and synchronization.
4. Complete the assessment independently under the course rules. You can save and print the certificate as soon as it is issued.
5. As a separate next step, apply the knowledge to the H200: a fixed workload, TTFT/ITL/VRAM, then one Nsight profile. **The certificate is already earned; the work experiment is another win.**

The course uses Numba. It teaches CUDA fundamentals, but does not by itself explain all of vLLM inference, attention, or the KV cache—reference section 1 below covers those.

NVIDIA purchases are supported only in the countries listed by the provider: [access conditions and country list](https://www.nvidia.com/en-us/learn/training/support/). The general DLI policy gives access to materials for **up to 6 months** from the start, with separate limits for GPU labs; an individual course retirement date takes precedence over the general period. Do not buy several courses in advance.

If enrollment or purchasing is unavailable for your account, continue with the open materials in section 1. **They do not award an NVIDIA certificate.** There is a separate verified Hugging Face option below for a short, free award; it covers agents and does not replace CUDA.

<a id="этап-2-gitlab--сначала-подготовка-потом-экзамен"></a>

### Stage 2: GitLab—prepare first, then take the exam

Start with Pro Git and the history exercises in section 2. Then complete the five learning-path blocks in order: Introduction to CI/CD → Understanding GitLab Runners → Maintain Pipelines with Efficiency → Solving Complex Problems with Pipelines → Introduction to GitLab Registries. Compare your preparation against the current exam topics: its scope is broader than the short videos.

Exam: 50 questions, 75 minutes, a 75% passing score; **14 days of access after registration and two attempts**. Buy it when preparation is complete. AI and unauthorized assistance are prohibited during the exam. [GitLab rules and award issuance](https://university.gitlab.com/learn/article/gitlab-certification-candidate-handbook). Completing the preparation videos alone does not earn this certification.

<a id="этапы-34-эксплуатация-затем-rag"></a>

### Stages 3–4: operations, then RAG

Follow the LFS162 chapter order: DevOps/SRE → cloud → containers → IaC → CI/CD → observability → SRE. This is an introductory overview, not full Kubernetes administrator training. [Course entry point](https://trainingportal.linuxfoundation.org/courses/introduction-to-devops-and-site-reliability-engineering-lfs162); [badge issuance criterion](https://www.credly.com/org/the-linux-foundation/badge/lfs162-introduction-to-devops-and-site-reliability-).

Before RAG, you need confident Python/OOP skills and introductory deep learning knowledge; PyTorch/transfer learning are recommended. If these are missing, use sections 5 and 10. After RAG, build a question set with reference answers, a retrieval baseline, and checks for document access and answer errors. A course certificate and the professional NCA/NCP exams are different awards.

<a id="практика-и-проверки"></a>

## Practice and checks

Each main stage has a small assignment: [CUDA/inference](modules/cuda-and-inference.md) → [Git/GitLab](modules/git-and-gitlab.md) → [SRE](modules/observability-and-sre.md) → [ML/RAG](modules/04-ml-llm-and-capstone.md).

The [module map](modules/README.md) connects the other disciplines to work tasks. [Internal checks](exams/MASTER_EXAMS.md) help identify gaps; they do not replace a provider's assessment or invalidate an earned certificate. One [milestone](templates/milestone.md) or [experiment](templates/experiment.md) is enough to record the work.

<a id="награды-по-остальным-дисциплинам--выбрать-одну-когда-понадобится"></a>

## Awards in other disciplines—choose one when needed

| Need | Course and sequence | Award requirements / limits |
|---|---|---|
| Python, backend, testing fundamentals | [CS50P](https://cs50.harvard.edu/python/): Weeks 0–9 → final project; then FastAPI from section 5 | [Free CS50 Certificate](https://cs50.harvard.edu/python/certificate/): ≥70% on **every** problem and the final project. This is not the paid verified edX certificate. At our pace, allow months for the whole course |
| SQL and databases | [CS50 SQL](https://cs50.harvard.edu/sql/): Querying → Relating → Designing → Writing → Viewing → Optimizing → Scaling → project; then PostgreSQL from section 6 | [Free certificate](https://cs50.harvard.edu/sql/certificate/): ≥70% on every problem and the project. The course does not replace PostgreSQL operations practice |
| Frontend and web backend | [Full Stack Open](https://fullstackopen.com/en/): Parts 0–5, then 6–7 as needed; JS → React → Node → tests | [Certificate rules](https://fullstackopen.com/en/part0/general_info): submit enough exercises for a passing grade; the current table for 0–5 requires at least 72. Download the certificate from the submission system; no exam is needed for the certificate. Confident programming is a prerequisite; this is a long elective |
| Security | [CS50 Cybersecurity](https://cs50.harvard.edu/cybersecurity/): Accounts → Data → Systems → Software → Privacy → project | [Free certificate](https://cs50.harvard.edu/cybersecurity/certificate/): ≥70% on every assignment and the project. Also use section 9 for AppSec/LLM security |
| A short finish in AI agents | [Hugging Face Agents, Unit 1](https://huggingface.co/learn/agents-course/unit1/introduction) → [current quiz app](https://huggingface.co/spaces/agents-course/unit_1_quiz) | [Certificate of Fundamentals](https://huggingface.co/learn/agents-course/unit1/get-your-certificate): Unit 1 + quiz ≥80%, free. The app launches, then requires an HF login. This certifies the **first unit**, not the entire course |
| QA, Linux/containers, observability, leadership | QA—CS50P tests and section 4 practice; infrastructure/SRE—LFS162 and sections 3/7; leadership—section 11 | Create a personal achievement for a separate work exercise, with a result and evidence. It is not a training-provider certificate |

[TAU Introduction to pytest](https://testautomationu.applitools.com/pytest-tutorial/) is **deferred for now**: public text is available through search, but the browser showed Site Unavailable twice. It is not a condition for progress, and no award is promised.

<a id="как-сохранять-мотивацию"></a>

## How to stay motivated

One active course. For completion—an award on the wall; for application—a short result entry. You can finish a course and celebrate before completing a large work project. [CREDENTIALS.md](CREDENTIALS.md) covers saving, printing, and the personal achievement template; [PROGRESS.md](PROGRESS.md) contains the queue and log.

Work agents can continue writing code. Assignments submitted for a certificate follow the rules of the **specific provider**: an independent assessment cannot automatically be treated as ordinary agent-assisted work.

<a id="что-проверено-и-что-убрано"></a>

## What was checked and removed

[Full audit of all 80 original links and new resources](LINK_AUDIT_2026-09-24.md). T-AC-01 and S-FX-18 were removed from the required path: their listings show enrollment closing, with disabled buttons. C-FX-26 is marked with access ending on December 31, 2026, and was also removed. Some other DLI courses are available for purchase, but certificates for those specific courses are unconfirmed—they are supplementary materials only.

The check records the state on **September 24, 2026**, not a guarantee of permanent availability. Before starting each next course, check three fields on its page: **enrollment, access period, award**. A new retirement notice means pausing the purchase and choosing a verified replacement.

---

<a id="справочник-по-дисциплинам"></a>

# Discipline reference

These are not eleven additional mandatory courses. Read selected sections to answer one work question. For a work result, keep the hypothesis, measurement, conclusion, and rollback method. Only put anonymized learning examples in the public repository.

<a id="1-cuda-устройство-gpu-и-llm-inference"></a>

## 1. CUDA, GPU architecture, and LLM inference

<a id="открытые-материалы-и-запасной-путь-без-оплаты"></a>

### Open materials and a fallback without payment

[An Even Easier Introduction to CUDA — NVIDIA article](https://developer.nvidia.com/blog/even-easier-introduction-cuda/) → [NVIDIA Accelerated Python Tutorial](https://github.com/NVIDIA/accelerated-computing-hub/tree/main/tutorials/accelerated-python). In the Python tutorial: Fundamentals 01 → 03 → 05 → 06 → 07 → Kernels 40. Start with data transfers and memory, then asynchrony and one kernel. These are open learning materials **without a promised certificate**; GPU execution requires a compatible environment and was not tested here.

Optional after the foundational course, only if you need the relevant practice:

- [Optimizing CUDA Machine Learning Codes With Nsight Profiling Tools](https://learn.nvidia.com/courses/course-detail?course_id=course-v1%3ADLI+S-AC-03+V2): $30, 2 hours, intermediate; CUDA familiarity. Buy Now is available; the listing does not confirm a certificate.
- [Find the Bottleneck: Optimize AI Pipelines With Nsight Systems](https://learn.nvidia.com/courses/course-detail?course_id=course-v1%3ADLI+S-AC-14+V1): $30, 3 hours, advanced; Python and PyTorch. Buy Now is available; the listing does not confirm a certificate.

Use the [general NVIDIA Learning Paths](https://www.nvidia.com/en-us/learn/learning-paths/) as a topic catalog; check the specific listing for current availability.

**Study order:**

1. **Computation map.** [NVIDIA GPU Performance Background](https://docs.nvidia.com/deeplearning/performance/dl-performance-gpu-background/index.html) → [CUDA Programming Guide: Introduction / Programming Model](https://docs.nvidia.com/cuda/cuda-programming-guide/). Understand SMs, warps, blocks, HBM/L2/shared/register memory, kernel launch, PCIe/NVLink, latency versus bandwidth. Read selected sections, not the entire reference.
2. **One small kernel.** [NVIDIA CUDA samples](https://github.com/NVIDIA/cuda-samples) (`vectorAdd`, then matrix multiplication) → [CUDA Best Practices Guide](https://docs.nvidia.com/cuda/cuda-c-best-practices-guide/) (memory, occupancy, profiling). Compare CPU, naive GPU, and library implementations; check correctness and timing after warmup. If C++ is holding you back, start with [PyTorch Basics](https://docs.pytorch.org/tutorials/beginner/basics/) on a remote GPU, then return to one kernel. This is a learning experiment, not a vLLM rewrite.
3. **Transformer as workload.** [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/) → [Hugging Face LLM Course](https://huggingface.co/learn/llm-course/chapter1/1) (tokenizer/model/generation) → [PyTorch scaled dot product attention](https://docs.pytorch.org/docs/2.14/generated/torch.nn.functional.scaled_dot_product_attention.html). Write down Q/K/V dimensions, the causal mask, and why prefill and decode differ. Then estimate the KV cache from the specific model's config: `2 × layers × KV-heads × head-dim × bytes × tokens × concurrent sequences`; check GQA/MQA, dtype, block waste, and runtime overhead. This estimate applies to standard attention with K/V at every layer and full context; for MLA, sliding-window, hybrid architectures, and tensor parallelism, check the specific engine's layout. For MoE, distinguish total model weights, active parameters, and KV.
4. **Serving.** [vLLM docs](https://docs.vllm.ai/en/latest/) (serving, scheduler, KV cache, benchmarking/metrics) → [SGLang docs](https://docs.sglang.io/) (serving, benchmarking). Understand request → queue → prefill → allocation → decode → stream, batching, prefix reuse, and tensor parallelism. Do not assume one engine's behavior applies to another without checking the version.
5. **Profiling.** [Nsight Systems](https://docs.nvidia.com/nsight-systems/UserGuide/) for the timeline → [Nsight Compute](https://docs.nvidia.com/nsight-compute/) for a specific kernel → [PyTorch Profiler](https://docs.pytorch.org/tutorials/beginner/profiler.html) for a PyTorch workload. Start with a bottleneck hypothesis, then profile; otherwise the chart is useless.

**H200 practice:** repeat a controlled benchmark of one model with a fixed engine version, quantization, prompt/output tokens, concurrency 1/4/8, and GPU count. Save raw measurements, TTFT p50/p95, ITL, output tok/s, GPU memory, queue/CPU, and settings. Do not treat `curl` wall time as pure decode speed; account for reasoning tokens and warmup. Compare predicted KV with actual VRAM and explain the difference. Profile work models during an agreed window.

**Output:** an internal table of supported load profiles and a procedure for choosing the H200 configuration; publicly—only a synthetic, reproducible `llm-inference-lab`, if publishing the methodology is allowed. **What I stop taking on trust:** “The model fits, so it can handle N users.”

**Book for deeper study:** [Programming Massively Parallel Processors (Hwu, Kirk, El Hajj)](https://shop.elsevier.com/books/programming-massively-parallel-processors/hwu/978-0-323-91231-0), chapters on GPU architecture, threads, and memory after your first hands-on experience; buying it is optional.

<a id="2-git-и-gitlab-cicd--после-первого-cuda-финиша"></a>

## 2. Git and GitLab CI/CD—after the first CUDA finish

1. [Pro Git](https://git-scm.com/book/en/v2): chapters 1–3 (objects, staging, commits, branches/merges), then selected sections 7.5–7.7 (search, rewriting, reset), 7.10 (debugging), and 10.2–10.3 (objects/references). Draw `HEAD`, the branch pointer, index, and working tree; explain `reset` versus `revert`.
2. In a separate practice branch, reproduce a conflict, `revert`, `reflog`, `bisect`, a merge request, and a safe rollback. Do not practice force pushes on a shared branch. Record the base commit before an agent task; afterward, check `git status`, `git diff --stat`, `git diff`, tests, and review.
3. [GitLab CI quick start](https://docs.gitlab.com/ci/quick_start/) → [YAML reference](https://docs.gitlab.com/ci/yaml/) (`stages`, `needs`, `rules`, `artifacts`, `cache`) → [Runner](https://docs.gitlab.com/runner/) → [Environments](https://docs.gitlab.com/ci/environments/) and [deployment safety](https://docs.gitlab.com/ci/environments/deployment_safety/). On corporate GitLab, check the version and availability of specific features.
4. Trace **one real pipeline**: commit → runner → build → artifact/image digest → tests/evals → staging → approval → prod → rollback. Understand whose token and permissions the job receives, where secrets are stored, and where the image comes from.

**Output:** a one-page map of the existing GitLab pipeline, mandatory diff/review for agent changes, and a verified version rollback scenario on staging. **What I stop taking on trust:** “The pipeline is green, so the release is safe to deploy.”

<a id="3-observability-и-sre"></a>

## 3. Observability and SRE

[Google SRE Book: SLI/SLO](https://sre.google/sre-book/service-level-objectives/) → [OpenTelemetry concepts](https://opentelemetry.io/docs/concepts/) → [Prometheus getting started](https://prometheus.io/docs/prometheus/latest/getting_started/) → [Grafana fundamentals](https://grafana.com/tutorials/grafana-fundamentals/). For ClearGate, record deterministic/NER/LLM/verify timing, p50/p95, errors, and correlation ID; for inference—TTFT/ITL, queue, KV usage, and GPU. Test one service failure and the alert's action. **Output:** a dashboard and runbook with a threshold and owner. **What I stop believing:** “The healthcheck is green, so users can work.”

<a id="4-qa-и-llm-evaluation"></a>

## 4. QA and LLM evaluation

[pytest getting started](https://docs.pytest.org/en/stable/getting-started.html) → [Playwright docs](https://playwright.dev/docs/intro) → [Google ML Crash Course: classification](https://developers.google.com/machine-learning/crash-course/classification/accuracy-precision-recall) → [NIST AI RMF](https://www.nist.gov/itl/ai-risk-management-framework) for a risk framework. For ClearGate, create a labeled dataset by document type, a separate held-out split, and negative cases for public legal entities, addresses, surnames, and leaks. Measure false negatives for critical fields, precision, and latency separately; do not claim an absolute guarantee from zero errors in a finite sample. **Output:** a CI regression gate and a before/after report with the raw sample under corporate access controls. **What I stop believing:** “The new prompt seems better.”

<a id="5-backend-и-рабочий-python"></a>

## 5. Backend and production Python

[Python tutorial](https://docs.python.org/3/tutorial/) (only gaps) → [typing](https://docs.python.org/3/library/typing.html) and [asyncio](https://docs.python.org/3/library/asyncio.html) → [FastAPI tutorial](https://fastapi.tiangolo.com/tutorial/) (dependencies, testing, background tasks) → [Pydantic docs](https://pydantic.dev/docs/validation/latest/get-started/) → [SQLAlchemy 2.0 tutorial](https://docs.sqlalchemy.org/en/20/tutorial/) and [Alembic](https://alembic.sqlalchemy.org/en/latest/tutorial.html). Examine one work endpoint: input, auth, dependency lifetime, transaction, retry/idempotency, failure, response. AI may change the code; you check the boundary and a negative test. **Book:** [Architecture Patterns with Python](https://www.cosmicpython.com/book/preface), chapters on repository/service/unit of work as real problems arise. **Output:** a review checklist for a FastAPI/Django service. **What I stop believing:** “Async makes CPU-bound code faster.”

<a id="6-postgresql-и-data-engineering"></a>

## 6. PostgreSQL and data engineering

[PostgreSQL tutorial](https://www.postgresql.org/docs/current/tutorial.html) → [Transactions](https://www.postgresql.org/docs/current/tutorial-transactions.html) → [EXPLAIN](https://www.postgresql.org/docs/current/using-explain.html) → [Indexes](https://www.postgresql.org/docs/current/indexes.html) → [MVCC](https://www.postgresql.org/docs/current/mvcc.html). In the ERP, choose two slow queries, record plans before/after adding an index, and check actual rows, locks, backup/restore, and a migration on staging. **Book:** [The Art of PostgreSQL](https://theartofpostgresql.com/) for deeper SQL study. **Output:** a database review with measurements and a reversible migration. **What I stop believing:** “An index always makes a query faster.”

<a id="7-linux-containers-и-инфраструктура"></a>

## 7. Linux, containers, and infrastructure

[The Linux Command Line](https://linuxcommand.org/tlcl.php) (permissions, processes, I/O) → [systemd docs](https://systemd.io/) → [Docker overview](https://docs.docker.com/get-started/docker-overview/) and [Compose](https://docs.docker.com/compose/) → [Podman docs](https://docs.podman.io/en/latest/) → [NVIDIA Container Toolkit](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/). On your dev VM, trace service → container user → volume → network → GPU device → log; rehearse a restart that preserves state. Maintain the dev/prod boundary and the no-outbound-access rule for prod under the agreed architecture. **Output:** a runtime diagram, dependency list, and recovery procedure. **What I stop believing:** “The container started, so the data and GPU are available.”

<a id="8-frontend-и-ux-контроль-агента"></a>

## 8. Frontend and UX review of agent work

[MDN Learn web development](https://developer.mozilla.org/en-US/docs/Learn_web_development) (HTML/CSS/HTTP) → [TypeScript Handbook](https://www.typescriptlang.org/docs/handbook/intro.html) → [React Learn](https://react.dev/learn) (state/effects) → [Next.js Learn](https://nextjs.org/learn) (server/client boundary) → [WAI accessibility tutorials](https://www.w3.org/WAI/tutorials/) → [Playwright](https://playwright.dev/docs/intro). In ClearGate, walk through one review flow: loading/error/empty states, keyboard use, preserving unsubmitted edits, and the API contract. **Output:** a verified user scenario and test. **What I stop believing:** “The screenshot looks good, so the process works.”

## 9. Security engineering

[OWASP Top 10](https://owasp.org/projects/top-ten) → [OWASP API Security Top 10](https://api-security.owasp.org/) → [OWASP LLM Top 10](https://genai.owasp.org/llm-top-10/) → [NIST SSDF](https://csrc.nist.gov/Projects/ssdf) → [OAuth 2.0 Security BCP](https://www.rfc-editor.org/info/rfc9700/). Draw trust boundaries: lawyer → browser → ClearGate → local model → permitted cloud egress → restore. On staging, test cross-user/matter access, SSRF, injection, runner secrets, and failure when the model is unavailable; coordinate with information security. **Output:** a threat model and a list of specific pre-release checks. **What I stop believing:** “The agent will respect boundaries because of the prompt.”

<a id="10-ml-engineering-rag-и-модели"></a>

## 10. ML engineering, RAG, and models

[Google ML Crash Course](https://developers.google.com/machine-learning/crash-course) → [PyTorch Basics](https://docs.pytorch.org/tutorials/beginner/basics/) → [Hugging Face LLM Course](https://huggingface.co/learn/llm-course/chapter1/1) → [Hugging Face PEFT](https://huggingface.co/docs/peft/index) → [Hugging Face TRL](https://huggingface.co/docs/trl/index). For RAG—[Stanford IR book](https://nlp.stanford.edu/IR-book/) (evaluation/retrieval) and [Qdrant docs](https://qdrant.tech/documentation/) for ACL-aware retrieval and filters. Start with a ClearGate/document-search baseline, then labeled data, a train/dev/held-out split, fine-tuning only when the need is demonstrated, ablation, and drift monitoring. **Book:** [Build a Large Language Model (From Scratch)](https://www.manning.com/books/build-a-large-language-model-from-scratch), selected chapters on attention/training; deeper reading after a working baseline. **Output:** a model decision with a reproducible quality/latency/cost comparison. **What I stop believing:** “Fine-tuning will fix the lack of an eval dataset.”

<a id="дополнительные-dli-и-профессиональные-экзамены"></a>

### Additional DLI courses and professional exams

[Evaluating RAG and Semantic Search Systems](https://learn.nvidia.com/courses/course-detail?course_id=course-v1%3ADLI+S-FX-32+V1): $30 / 3 hours; purchasing is open, but certificate issuance is unconfirmed. Take it for a retrieval/evaluation task.

[Introduction to Deploying RAG Pipelines for Production at Scale](https://learn.nvidia.com/courses/course-detail?course_id=course-v1%3ADLI+S-FX-19+V1): the listing shows $90 / 4 hours, Kubernetes/Helm/NIM. A similarly named course is described differently on a certification overview page; the award for this exact version is unconfirmed. Do not buy it for a certificate without clarification.

[NCA-GENL](https://www.nvidia.com/en-us/learn/certification/generative-ai-llm-associate/) and [NCP-GENL](https://www.nvidia.com/en-us/learn/certification/generative-ai-llm-professional/) are optional, separate exams, not the next required course. Registration pages exist; a badge and optional certificate are advertised after passing. Exam availability in your country and the terms in your exam-provider account were not checked. NCA tests fundamentals; NCP requires deeper preparation in training/distributed systems. Preparation links within the NVIDIA page can also become outdated.

<a id="11-applied-ai-продукт-и-лидерство--постоянно"></a>

## 11. Applied AI, product, and leadership—ongoing

Read [AI Engineering (Chip Huyen)](https://www.oreilly.com/library/view/ai-engineering/9781098166298/) for your current bottleneck (evaluation, deployment, agents) → [Google engineering practices: code review](https://google.github.io/eng-practices/review/) → project and team management chapters of [The Manager's Path](https://www.oreilly.com/library/view/the-managers-path/9781491973882/) as needed. At every work milestone: one ADR decision, a risk owner, a result metric, a clear Definition of Done, and a short standard for future people/agents. **Output:** a repeatable system delivery process and clear achievements worth celebrating. Books and code review do not themselves award certificates.

<a id="шаблон-одного-milestone"></a>

## One-milestone template

```text
Work problem:
My hypothesis and expected measurement:
Resource (exact section):
What the agent did:
What I checked myself (command/log/metric/user scenario):
Access boundary and failure scenario:
Result before → after:
How to roll back:
What I no longer delegate to an agent on blind trust:
The next most costly gap:
```

<a id="ближайшие-три-занятия"></a>

## The next three sessions

1. **45–60 minutes:** check the Python/NumPy prerequisites, open CUDA Python, and complete the introduction. If enrollment is restricted, use the open article and tutorial.
2. **45–60 minutes:** kernel launch, thread/block/grid; write one explanation in your own words and one question.
3. **90–120 minutes:** reproduce a small example, check the result and measurement. Continue the course through the assessment. GitLab starts as the next stage; an urgent work question can be handled separately.

Save the certificate as soon as it is issued. Create a second, personal achievement for the completed work benchmark.
