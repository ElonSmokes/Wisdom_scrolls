# 32-Week Syllabus

This curriculum is designed for 8–10 focused hours per week. Extend the schedule rather than skipping exercises.

## Phase 0 — Setup and baseline

### Week 1
Primary resources:
- Python official tutorial: sections 1–4
- GitHub Skills: Introduction to GitHub

Deliverables:
- install Python 3.12+, VS Code, Git and Docker;
- create a virtual environment;
- write a 50–100 line CLI that reads a text file and prints basic statistics;
- commit it without AI-generated implementation;
- complete the baseline questionnaire in `modules/00-setup-and-baseline.md`.

## Phase 1 — Python foundations

Primary course: **Harvard CS50P: Introduction to Programming with Python**.

### Week 2 — Variables, expressions and conditionals
Complete CS50P Week 0 and Week 1. Write three small programs from a blank file.

### Week 3 — Loops and collections
Complete CS50P Week 2. Build a log-line counter using lists, dictionaries and loops.

### Week 4 — Exceptions and libraries
Complete CS50P Week 3 and Week 4. Build a resilient file-processing CLI with useful errors.

### Week 5 — Unit tests
Complete CS50P Week 5. Add pytest tests before changing the CLI.

### Week 6 — Files and regular expressions
Complete CS50P Week 6 and Week 7. Build a deterministic PII candidate extractor for email, phone and IDs.

### Week 7 — Object-oriented programming
Complete CS50P Week 8. Refactor findings into typed objects with clear responsibilities.

### Week 8 — Final project
Complete the CS50P final project: a document inspection CLI. It must have tests, logging and a README.

### Week 9 — Python mastery gate
Complete `exams/python-exam.md` closed-book. Repeat the phase if the result is below 80% or you cannot explain your own code.

## Phase 2 — Professional Python

Primary resources:
- Python Packaging User Guide tutorials
- pytest documentation: Getting Started
- mypy Getting Started
- Ruff documentation

### Week 10 — Project structure and packaging
Create `src/` and `tests/` layout, `pyproject.toml`, editable install and console entry point.

### Week 11 — Types and data modelling
Learn type hints, protocols, dataclasses, enums and Pydantic fundamentals. Run mypy in strict-enough mode.

### Week 12 — Logging, configuration and debugging
Use `logging`, environment-based configuration and the debugger. Remove all diagnostic `print()` calls.

### Week 13 — Refactoring gate
Refactor the Week 8 project without changing externally visible behaviour. Demonstrate tests first, small commits and an ADR.

## Phase 3 — Linux, networking and Git

Primary resources:
- The Linux Command Line by William Shotts, selected chapters
- Pro Git, chapters 1–3
- MDN overview of HTTP

### Week 14 — Linux operating model
Files, permissions, processes, signals, services, logs, pipes, redirection, environment variables and SSH.

### Week 15 — Networking and HTTP
IP, routes, ports, DNS, TCP, TLS, HTTP methods and status codes. Diagnose a deliberately broken local service.

### Week 16 — Git as an engineering tool
Branches, merges, rebase, conflicts, revert, bisect and pull requests. Reconstruct a bug using Git history.

## Phase 4 — Docker and Compose

Primary resource: Docker official Get Started workshop and Dockerfile reference.

### Week 17 — Images and containers
Build an image manually. Explain every Dockerfile instruction, image layer, build context, CMD and ENTRYPOINT.

### Week 18 — Storage and networking
Volumes, bind mounts, user IDs, bridge networks, DNS, health checks and graceful shutdown.

### Week 19 — Compose boss fight
Run the CLI/API, PostgreSQL and a worker through Compose. Complete `exams/docker-exam.md` without agent implementation.

## Phase 5 — Backend engineering and databases

Primary resources:
- FastAPI official tutorial
- SQLBolt lessons
- PostgreSQL official tutorial
- Alembic tutorial

### Week 20 — HTTP API fundamentals
Build endpoints, request/response models, validation and error handling.

### Week 21 — Application architecture
Separate transport, service and repository layers. Learn dependency injection without creating abstraction theatre.

### Week 22 — SQL and PostgreSQL
Tables, constraints, joins, indexes, transactions and query plans. Use raw SQL before an ORM.

### Week 23 — SQLAlchemy and migrations
Persist document jobs and findings. Add migrations, rollback instructions and transaction tests.

### Week 24 — Backend mastery project
Build a tested document-analysis job API with PostgreSQL, background processing, authentication stub and Compose.

## Phase 6 — ML and LLM foundations

Primary resources:
- Google Machine Learning Crash Course
- Hugging Face NLP/LLM Course, chapters 1–5 and relevant inference sections
- The Illustrated Transformer

### Week 25 — ML foundations and evaluation
Train/validation/test splits, leakage, precision, recall, F1, confusion matrices, thresholds and baselines.

### Week 26 — Embeddings and retrieval
Tokenization, embedding vectors, similarity, chunking, retrieval metrics and reranking. Build retrieval without a framework first.

### Week 27 — Transformers and inference
Attention, transformer blocks, causal language modelling, context windows, batching and decoding parameters.

### Week 28 — Local serving
Study vLLM concepts: model loading, quantization, KV cache, continuous batching, tensor parallelism and OpenAI-compatible APIs. Complete `exams/llm-exam.md`.

## Phase 7 — Production AI capstone

### Week 29 — Architecture and threat model
Write requirements, data-flow diagram, ADRs, privacy boundary, failure modes and evaluation plan.

### Week 30 — Implementation
Build deterministic PII detection plus model-assisted review behind a typed service boundary. No whole-feature agent generation.

### Week 31 — Evaluation and operations
Create a labelled test set, precision/recall report, latency measurements, structured logs, health checks and backup/restore procedure.

### Week 32 — Final defence
Demonstrate the system, explain every component, reproduce deployment from a clean machine and document known limitations.

## Graduation standard

You graduate only when you can:

1. implement a non-trivial Python feature from a written requirement;
2. diagnose a failing Linux/Docker service methodically;
3. build and test a FastAPI/PostgreSQL service;
4. explain the LLM serving path from request to generated tokens;
5. measure product quality instead of judging by demos;
6. identify code you do not understand and refuse to ship it blindly.
