<a id="учебная-программа"></a>

# Syllabus

[Roadmap and courses](WORK_INTEGRATED_ROADMAP.md) · [Modules](modules/README.md) · [Progress](PROGRESS.md)

Sequence: **CUDA → Git/GitLab → SRE → RAG**. One active course, 3–5 hours per week. The numbered filenames of older modules are preserved for links; they do not determine the sequence.

<a id="три-вида-завершения"></a>

## Three kinds of completion

- **Course:** the provider’s requirements have been met and the award issued.
- **Practical module:** a small result has been produced that you can explain and substantiate.
- **Internal check:** the criteria in [MASTER_EXAMS](exams/MASTER_EXAMS.md) have been met.

These events have separate dates. A course certificate does not have to wait for a large project to be finished.

<a id="основная-последовательность"></a>

## Main sequence

| Stage | Before starting | Order | Practical finish |
|---|---|---|---|
| Setup as needed | Access to the chosen course | [Setup](modules/00-setup-and-baseline.md): account, Python/NumPy, a place for notes | You know where to work through the next section |
| 1. CUDA | Python functions, loops, arrays, and NumPy ndarray | NVIDIA CUDA Python → assessment; [practice](modules/cuda-and-inference.md): data → kernel → measurement → inference | An explained benchmark and, when a profiler is available, a profile |
| 2. Git/GitLab | Files and the command line | [Git module](modules/git-and-gitlab.md): commits/index → history → jobs → artifacts → rollback; then the GitLab exam | Recovery of practice history and a pipeline map |
| 3. DevOps/SRE | Request path through a service, a basic pipeline | LFS162 → award; [SRE module](modules/observability-and-sre.md): metric → SLO → alert → runbook | A detected practice failure and recovery |
| 4. RAG | Python/OOP, introductory deep learning; the course recommends PyTorch | NVIDIA Building RAG Agents → assessment; [ML/RAG module](modules/04-ml-llm-and-capstone.md): baseline → retrieval → evaluation → access | A reproducible quality comparison |

Course schedules, prices, and conditions are in the roadmap. Check access and expiry before purchasing. A GPU is needed for independent GPU execution; the course’s cloud lab has its own conditions.

<a id="остальные-дисциплины--по-потребности"></a>

## Other disciplines — as needed

| If the obstacle is… | Open | Smallest useful action |
|---|---|---|
| Reading Python code or NumPy | [Python](modules/01-python-foundations.md) | Understand a function and array shape; choose CS50P for a broader gap |
| A package, process, container, or GPU | [Runtime/Linux/containers](modules/02-professional-python-and-systems.md) | Trace startup and one failure on dev |
| An endpoint, transaction, migration, or query | [Backend/PostgreSQL](modules/03-backend-and-databases.md) | A contract, negative test, or query plan |
| “It got better” without data | [QA/evaluation](modules/quality-and-evaluation.md) | A baseline and separate examples for the final evaluation |
| An interface and review flow | [Frontend/UX](modules/frontend-and-ux.md) | One scenario covering every state and keyboard use |
| Data and access boundaries | [Security](modules/security-engineering.md) | A negative scenario using synthetic data |
| Decisions and agent work | [Technical leadership](modules/technical-leadership.md) | An ADR with an outcome criterion and risk owner |

These are exercises to use as needed. Completing the whole reference section is not required before the next course.

<a id="ритм-недели"></a>

## Weekly rhythm

1. One or two 45–60-minute sessions: course theory and exercises.
2. A practice block of up to two hours: one testable hypothesis.
3. Five minutes for a [weekly review](templates/weekly-review.md): a win, an obstacle, and the next section.

If an incident takes up the week, a single note with a lesson is enough. A low score does not require repeating an entire phase.

<a id="общий-проект"></a>

## Shared project

The modules can be applied to a learning system that processes synthetic documents. It does not have to copy production. The [capstone](modules/04-ml-llm-and-capstone.md) is limited to one scenario; deployment and a demo do not establish readiness for real work data.

<a id="архив"></a>

## Archive

The [previous 32-week syllabus](archive/LEGACY_32_WEEK_SYLLABUS.md) is preserved with corrected relative links. It is a historical version.
