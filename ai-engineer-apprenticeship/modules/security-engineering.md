<a id="security-engineering-границы-данных-и-доступа"></a>

# Security engineering: data and access boundaries

[Module map](README.md) · [CS50 Cybersecurity course](../WORK_INTEGRATED_ROADMAP.md)

The goal is to check specific boundaries in one of your services. Practice takes place on authorized dev/staging with synthetic data.

<a id="порядок"></a>

## Order

[OWASP Top 10](https://owasp.org/projects/top-ten) → [API Security](https://api-security.owasp.org/) → [LLM Top 10](https://genai.owasp.org/llm-top-10/) → [NIST SSDF](https://csrc.nist.gov/Projects/ssdf). Read categories relevant to the chosen flow; CS50 Cybersecurity provides a broad overview.

<a id="практика"></a>

## Practice

1. Draw browser → API → data store → model/tools → output. Mark users, documents, tokens, and permitted egress.
2. For each boundary, record who makes the access decision and what happens on failure.
3. Create two practice users and two document sets. Check direct requests for another user’s ID, search, export, and retrieval context.
4. Submit a learning document containing an instruction to violate the task. Check that document text does not grant new tool or egress permissions.
5. Check that secrets do not appear in the UI, logs, or pipeline artifacts. If the service accepts URLs, separately check allowed destinations within your environment.
6. Make a table: risk → check → observation → fix → repeat check.

An unavailable dependency should lead to predefined behavior. A model’s prompt-based decision does not replace server-side authorization.

<a id="выход"></a>

## Outcome

One boundary diagram, a reproducible negative scenario, and a list of open risks with an owner. [Security Review](../exams/MASTER_EXAMS.md#security-review).

The exercise earns a personal achievement; the CS50 certificate relates to its own program. This module is not a professional security audit or confirmation of compliance.
