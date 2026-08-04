# Mastery Exams

All exams are closed-AI. Documentation is allowed unless the section says otherwise. Record start time, end time, mistakes and corrections.

# Python Exam

Time: 180 minutes. Pass: 80% plus successful explanation.

## Part A — Concepts

Explain in your own words:

1. mutable versus immutable values;
2. scope and name resolution;
3. exception propagation;
4. iterator versus iterable;
5. class composition versus inheritance;
6. dependency injection without a framework;
7. why tests should assert behaviour rather than implementation;
8. text encoding and why UTF-8 decoding can fail.

## Part B — Implementation

Build a CLI that:

- scans `.txt` files recursively;
- computes SHA-256 hashes;
- detects duplicate content;
- extracts email candidates;
- emits JSON;
- processes unreadable files without terminating the entire run;
- has at least eight meaningful tests.

No copied project code. Standard library and pytest are allowed.

## Part C — Debugging

Take a previously unseen broken Python program. Produce:

- minimal reproduction;
- root-cause explanation;
- failing regression test;
- smallest justified fix.

# Docker Exam

Time: 150 minutes. Pass: all critical tasks.

1. Write a Dockerfile for a Python API from a blank file.
2. Run as a non-root user.
3. Explain build context, layers and cache invalidation.
4. Add Compose with API and PostgreSQL.
5. Add health checks and persistent storage.
6. Diagnose a DNS failure between services.
7. Diagnose a permission failure on a mounted directory.
8. Demonstrate graceful shutdown.
9. Explain why `localhost` inside a container does not refer to the host or another service.
10. Reduce an intentionally bloated image and justify each change.

Automatic failure:

- solving by repeated blind rebuilds;
- copying an unexplained Dockerfile;
- running everything privileged or as root to bypass the problem.

# LLM Systems Exam

Time: 180 minutes. Pass: 80% and valid benchmark design.

## Explain

1. tokenization;
2. attention;
3. prefill and decode;
4. KV cache;
5. context-length memory pressure;
6. quantization;
7. tensor parallelism;
8. TTFT versus throughput;
9. continuous batching;
10. why a fast model can still produce a bad product.

## Design

Design a benchmark comparing two local models for legal-document analysis. Specify:

- hardware and serving configuration;
- dataset and held-out split;
- tasks and scoring rubric;
- concurrency levels;
- latency metrics;
- quality metrics;
- failure taxonomy;
- reproducibility controls.

## Evaluation task

Given labelled PII spans and model predictions, calculate precision, recall and F1; inspect boundary errors; choose a threshold; and explain the cost of false positives versus false negatives for the actual product policy.

# Grading rule

An answer is not correct merely because the code runs. You must be able to explain:

- what assumptions it makes;
- how it fails;
- how it is tested;
- what evidence supports the design.
