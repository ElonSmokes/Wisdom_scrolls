<a id="работа-с-ai-во-время-обучения-и-разработки"></a>

# Working with AI during learning and development

[Syllabus](SYLLABUS.md) · [Knowledge checks](exams/MASTER_EXAMS.md)

The goal is to retain understanding and the ability to verify results while continuing to use agents in daily work.

<a id="три-режима"></a>

## Three modes

| Mode | What the agent does | What you verify |
|---|---|---|
| Work implementation and labs | May write code, configuration, and tests, and help with diagnosis | The requirement, scope of change, diff, verification data, failure behavior, and rollback |
| Independent internal check | After the first attempt: review and explain gaps | Your own answers and decisions before hints; then another attempt at the weak point |
| Graded assessment of an external course/exam | Only what the provider permits | The current rules for that assignment; permission to use AI at work does not automatically carry over |

In particular, GitLab’s exam prohibition on AI is recorded in the [roadmap](WORK_INTEGRATED_ROADMAP.md). Do not copy actual exam questions into public notes. The repository’s internal exercises do not replace external assessment.

<a id="один-цикл-работы"></a>

## One work cycle

1. Define the expected behavior and how to verify it.
2. Record the starting commit/configuration and limit the task.
3. Receive the change; inspect the diff and affected dependencies.
4. Verify the normal case and a significant failure; inspect raw data for measurements.
5. Decide whether to accept the change and record the remaining question.

You do not need to reproduce an entire framework by hand. You need to understand the changed area, its contract, risks, and how to diagnose it.

<a id="если-диагностика-застряла"></a>

## If diagnosis gets stuck

Reproduce the error, collect the traceback/log, state a hypothesis, and choose an observation that distinguishes possible causes. If several iterations yield no new data, reduce the problem.

There is no mandatory “30 minutes without help” wait. During an incident, restore the service first using an available, verified method, then review the lesson. Returning to an older version must not destroy uncommitted changes or needed data.

<a id="короткая-запись-вклада-ai"></a>

## Short record of AI contribution

```text
Task and expected result:
What the agent did:
What I checked:
Evidence: diff / test / log / measurement
What I do not understand yet:
Next step or rollback:
```

Every small action does not need a separate report. A record is useful for a significant change or a learning insight. Templates: [milestone](templates/milestone.md) and [weekly review](templates/weekly-review.md).

<a id="что-считать-освоенным"></a>

## What counts as understood

You can explain the mechanism, predict at least one failure, and verify the result. Copying a successful output without running and checking it does not count as completed practice. Using a hint is a normal part of learning; simply record it in an independent check.
