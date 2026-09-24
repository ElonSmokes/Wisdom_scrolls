<a id="applied-ai-и-техническое-лидерство"></a>

# Applied AI and technical leadership

[Module map](README.md) · [Books and reference materials](../WORK_INTEGRATED_ROADMAP.md)

The goal is to make verifiable decisions and organize people and agents so the result can be maintained.

<a id="читать-по-текущему-вопросу"></a>

## Read for the current question

AI Engineering (Chip Huyen): evaluation/deployment/agents → [Google code review practices](https://google.github.io/eng-practices/review/) → The Manager’s Path as management tasks arise. Exact book links are in roadmap section 11. These materials are for application, not a required additional queue.

<a id="практика-одно-реальное-решение"></a>

## Practice: one real decision

1. Name the user, problem, baseline, and observable success criterion.
2. Consider at least two alternatives, including a simple solution without a new model if appropriate.
3. Record operating cost, data constraints, risks, owner, and the trigger for reconsideration.
4. Split agent work into reviewable changes: task definition → diff → verification → acceptance decision.
5. Describe failure behavior and a rollback/stop plan.
6. Hand over a short procedure that the next person can repeat. If you are working alone, repeat it yourself after a break.

Write an [ADR](../templates/adr.md). Distinguish fact, assumption, and an untested hypothesis. Do not judge system quality solely from an attractive demo or a speed benchmark.

<a id="выход"></a>

## Outcome

A decision with evidence, an owner, and a bounded next step. [Technical Leadership](../exams/MASTER_EXAMS.md#technical-leadership).

A completed decision earns a personal achievement. LFS162 in the main queue helps with the delivery/SRE overview; this module does not promise a separate management certificate.
