# AI Engineer Apprenticeship

> **Текущий маршрут (с 23.09.2026):** [рабочий roadmap с CUDA и Git в начале](WORK_INTEGRATED_ROADMAP.md). Он даёт точные ссылки, порядок чтения, практику на H200/GitLab и результаты по каждому направлению. 32-недельный план ниже сохраняется как углублённый самостоятельный трек; он больше не задаёт обязательный порядок для рабочих задач.

A practical 32-week path from Windows/system-administration experience and rusty Python basics to independently building, testing, containerizing, deploying, and evaluating local-AI systems.

## Target capability

By the end, you should be able to:

- read and modify Python applications without relying on blind agent generation;
- design and test FastAPI services;
- understand Linux processes, networking, permissions, Git, Docker and Compose;
- use PostgreSQL and migrations safely;
- explain embeddings, transformers, quantization, KV cache and inference serving;
- deploy and evaluate a small local document-analysis service;
- use AI as a reviewer and tutor rather than as a slot machine.

## Pace

- **Duration:** 32 weeks
- **Normal workload:** 8–10 hours per week
- **Minimum sustainable workload:** 5 hours per week; extend the calendar rather than skipping exercises
- **Protected workday block:** 60–90 minutes before production agent work

## Non-negotiable rules

1. Write the first working version of every mandatory exercise yourself.
2. AI may explain, question, review, generate extra tests and help interpret errors.
3. AI may not solve a mastery check before you submit your attempt.
4. Commit every meaningful increment.
5. Watching a course is not completion. Passing the module exit check is completion.
6. Keep learning projects small enough to understand completely.
7. Maintain one active production priority; park the rest visibly.

## Roadmap

| Phase | Weeks | Outcome |
|---|---:|---|
| 0. Setup and baseline | 1 | Reproducible environment and honest diagnostic |
| 1. Python foundations | 2–9 | Independently write tested command-line programs |
| 2. Professional Python | 10–13 | Packages, typing, logging, configuration and debugging |
| 3. Linux, networking and Git | 14–16 | Diagnose services without cargo-cult commands |
| 4. Docker and Compose | 17–19 | Build and debug reproducible containers |
| 5. Backend and databases | 20–24 | Tested FastAPI/PostgreSQL application |
| 6. ML and LLM foundations | 25–28 | Embeddings, transformers, inference and evaluation |
| 7. Production AI capstone | 29–32 | Local document-analysis system, end to end |

## Repository map

- [`WORK_INTEGRATED_ROADMAP.md`](WORK_INTEGRATED_ROADMAP.md) — актуальный порядок, ресурсы и рабочие milestones
- [`SYLLABUS.md`](SYLLABUS.md) — прежний 32-недельный самостоятельный трек
- [`PROGRESS.md`](PROGRESS.md) — current status and evidence log
- [`modules/`](modules/) — assignments and exit criteria for each phase
- [`templates/weekly-review.md`](templates/weekly-review.md) — weekly reflection
- [`templates/adr.md`](templates/adr.md) — architecture decision record
- [`AI_USAGE_RULES.md`](AI_USAGE_RULES.md) — operating rules for coding agents

## Begin

1. Read [`WORK_INTEGRATED_ROADMAP.md`](WORK_INTEGRATED_ROADMAP.md) and choose the CUDA/GPU inference milestone.
2. Study Git/GitLab in parallel on a training branch and one real pipeline.
3. Record evidence and the next blind spot in [`PROGRESS.md`](PROGRESS.md).
4. Use [`modules/00-setup-and-baseline.md`](modules/00-setup-and-baseline.md) when you want an independent coding baseline; it is no longer a prerequisite for working milestones.
