# Engineering Graveyard

This directory stores failed experiments, abandoned architectures and expensive mistakes.

A graveyard entry is not shame. It prevents the same failure from being paid for twice.

## Entry template

Create one Markdown file per meaningful failure:

```text
YYYY-MM-DD-short-name.md
```

Include:

1. **Goal** — what was being attempted.
2. **Context** — constraints and assumptions.
3. **What happened** — observable failure, without drama.
4. **Evidence** — logs, tests, metrics or commits.
5. **Root cause** — known, suspected or explicitly unknown.
6. **What was tried** — including agent loops and why they failed.
7. **Lesson** — reusable engineering principle.
8. **Revisit condition** — what would need to change before trying again.
9. **Salvageable assets** — tests, utilities, datasets or design ideas worth keeping.

## Suggested first entries

- ClearGate spaCy `LOC -> CITY` hallucination failure;
- fragmented public legal-entity names bypassing the keep policy;
- any deployment loop where repeated agent patches produced regressions;
- an architecture that became too complex to evaluate reliably.
