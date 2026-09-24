<a id="qa-и-llm-evaluation"></a>

# QA and LLM evaluation

[Module map](README.md) · [Reference materials](../WORK_INTEGRATED_ROADMAP.md)

The goal is to replace a demo impression with a verifiable comparison. Open this when changing a model, prompt, rule, or user scenario.

<a id="читать"></a>

## Read

[pytest getting started](https://docs.pytest.org/en/stable/getting-started.html) → [Playwright](https://playwright.dev/docs/intro) for UI → [classification metrics](https://developers.google.com/machine-learning/crash-course/classification/accuracy-precision-recall). The TAU course is currently deferred according to the audit; it is not a dependency of this module.

<a id="практика"></a>

## Practice

1. Record the task, versions, and baseline. Write the regression criterion before making the change.
2. Assemble a small synthetic dataset: positive, negative, empty, and ambiguous cases. Describe labeling and example provenance.
3. Separate tuning data from the final evaluation. Do not tune the prompt on the final set.
4. For PII, calculate precision/recall by category, distinguishing exact span matches from partial ones. For retrieval, measure finding the relevant source separately from answer correctness.
5. Add deterministic unit/integration/UI tests only for suitable behavior. Do not present statistical LLM evaluations as deterministic unit tests.
6. Compare before/after, analyze errors, and record the decision. A small sample with no observed leaks does not prove absolute safety.
7. Define the CI gate: what blocks a release, what requires review, and what is simply monitored. The threshold must be justified by the task.

<a id="маленькая-расчётная-проверка"></a>

## Small calculation check

For a synthetic detector: TP=8, FP=2, FN=4. Independently calculate precision and recall, then explain why the costs of a missed detection and a false positive may differ. This is an exercise, not a measurement of a real product.

<a id="выход"></a>

## Outcome

A dataset version, baseline, comparison report, and at least one regression case. [QA and Evaluation](../exams/MASTER_EXAMS.md#qa-and-evaluation). Data under corporate access controls does not need to be copied into a public repo.

The reward for this practice is a personal achievement. CS50P from the roadmap provides pytest foundations and a separate certificate for the entire course; reading pytest docs does not promise a certificate.
