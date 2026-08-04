# Phase 6–7 — ML, LLM Inference and Production Capstone

## Mission

Replace demo-driven judgement with measurable quality, then build a local document-analysis system you can explain and operate.

## ML foundations

Complete the relevant Google ML Crash Course sections on:

- datasets and splits;
- classification;
- precision, recall and thresholds;
- overfitting and generalization;
- embeddings;
- fairness and data quality.

For ClearGate-style work, create a labelled evaluation set with separate development and held-out test portions. Never tune prompts, rules or thresholds on the held-out set.

## Retrieval lab

Build a small retrieval system without LangChain or an agent framework:

1. parse documents;
2. split them into chunks;
3. compute embeddings;
4. store vectors and metadata;
5. retrieve by similarity;
6. calculate recall@k on labelled questions;
7. add reranking and compare results.

Document chunking failures and citation-boundary problems.

## Transformer and inference study

You must be able to explain:

- tokenization and vocabulary;
- embeddings and positional information;
- self-attention at a conceptual and tensor-shape level;
- causal masking;
- transformer blocks;
- prefill versus decode;
- KV cache;
- batching and continuous batching;
- quantization trade-offs;
- tensor parallelism;
- TTFT, inter-token latency and throughput.

## vLLM lab

Serve a model locally and measure:

- cold and warm model load;
- TTFT;
- decode tokens per second;
- concurrency at 1, 2, 4 and 8 requests;
- memory use;
- failures at excessive context length;
- quality differences across decoding settings.

Do not report one tokens-per-second number without workload definition.

# Capstone: ClearGate Lite

Build a local-first service that accepts text documents and returns reviewable PII findings.

## Required pipeline

1. ingestion and text normalization;
2. deterministic detectors for structured identifiers;
3. model-assisted candidate classification or review;
4. span merge with source offsets preserved;
5. policy decision: `PROTECTED`, `PUBLIC`, or `REVIEW`;
6. placeholder rendering;
7. leakage verification;
8. audit event generation;
9. reviewer API;
10. export of masked text and evaluation report.

## Required quality work

- labelled corpus with documented annotation rules;
- precision, recall and F1 by label and document type;
- false-positive and false-negative taxonomy;
- held-out test set;
- ablation comparing deterministic-only, model-only and combined systems;
- latency distribution, not only average;
- regression suite for every discovered serious failure;
- explicit known limitations.

## Operational requirements

- Compose-based deployment;
- non-root containers;
- no required outbound internet;
- health and readiness checks;
- structured logs with correlation IDs;
- backup and restore instructions;
- threat model and privacy boundary;
- reproducible deployment from a clean host;
- failure-safe behaviour when the model is unavailable.

## Final defence

In a recorded or live 60-minute session:

1. deploy from a clean clone;
2. process a test document;
3. trace one finding through the system;
4. explain one false positive and one false negative;
5. change a business rule and add its regression test;
6. diagnose a deliberately broken container;
7. explain what you would redesign for production scale.

Graduation requires understanding, not perfection.
