<a id="observability-и-sre"></a>

# Observability and SRE

Main stage 3. [LFS162 and its award](../WORK_INTEGRATED_ROADMAP.md) · [Module map](README.md)

Prerequisites: understanding the request path and where the service runs. The goal is to notice a user’s problem and recover the system using a reproducible procedure.

<a id="порядок"></a>

## Order

LFS162 in syllabus order → [Google SRE: SLO](https://sre.google/sre-book/service-level-objectives/) → [OpenTelemetry concepts](https://opentelemetry.io/docs/concepts/) → [Prometheus](https://prometheus.io/docs/prometheus/latest/getting_started/) → [Grafana fundamentals](https://grafana.com/tutorials/grafana-fundamentals/).

Use the reference sections needed for one service. You do not need to deploy an entire observability stack for your first chart.

<a id="практика"></a>

## Practice

1. Choose a user scenario, such as completed document processing. Define a successful request, denominator, latency threshold, and measurement window.
2. Set a learning SLO and explain the choice. Do not declare it a contractual production commitment without agreement.
3. Connect the request to its log and processing stages using a correlation ID. Latency metrics do not require secrets or document contents.
4. Build an error/latency chart and an alert that leads to an action. Distinguish “no data” from “no errors.”
5. On dev, stop one dependency or introduce a controlled delay. Record detection time, symptoms, and recovery.
6. Repeat recovery using your runbook rather than memory.

<a id="runbook-должен-отвечать"></a>

## The runbook must answer

How do you detect the failure? How do you test the hypothesis? What action is allowed? When should you stop and escalate, and to whom? How do you verify that the user scenario has recovered?

For a stateful service, the recovery check includes reading known data. A successful process start does not yet establish data integrity.

<a id="выход"></a>

## Outcome

One metric, one alert, one completed recovery scenario, and an [experiment record](../templates/experiment.md). [SRE check](../exams/MASTER_EXAMS.md#sre-and-recovery).

The provider issues the LFS162 badge; the runbook earns a personal achievement. Next is the main [RAG stage](04-ml-llm-and-capstone.md), with QA supporting its measurements.
