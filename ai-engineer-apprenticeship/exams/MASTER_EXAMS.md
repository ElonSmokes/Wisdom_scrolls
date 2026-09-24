<a id="внутренние-проверки-знаний"></a>

# Internal knowledge checks

[Syllabus](../SYLLABUS.md) · [Modules](../modules/README.md) · [Progress](../PROGRESS.md)

These checks assess your own understanding. They do not award an external certificate or affect a course award you have already earned. Choose one check after the corresponding practice, using your own learning artifacts.

<a id="единая-шкала"></a>

## Shared scoring scale

Each check has five items, each scored **0–2**:

| Score | Basis |
|---:|---|
| 0 | No answer/result, a substantial error, or a result that is only assumed |
| 1 | Partially correct: a substantive hint is needed, evidence is incomplete, or a limitation is unexplained |
| 2 | Completed and explained in your own words; practical items include a reproducible observation |

**Pass:** at least 8/10, with 2 points on every explicitly marked critical item. If you only need theory, record it as such—it does not complete the practical part. Scores assess this attempt, not the percentage of a profession you have mastered.

Documentation and your own code are allowed. On the first attempt, provide explanations and solutions independently; an agent may then review them, ask questions, and help address a gap. Do not record a hinted answer as independent until you check it again. External assessments have their own rules.

Allow 45–90 minutes; split longer practical work into sessions. You do not need to retake every module because of one gap. Record: date → item → score → evidence → what to revisit. Do not store questions from confidential certification exams here.

## CUDA and Inference

[Practice](../modules/cuda-and-inference.md).

1. Explain thread/block/grid, host/device, and the data path using your own example.
2. Predict when data copying may outweigh kernel speed gains.
3. **Critical:** demonstrate result correctness and distinguish kernel-only from end-to-end measurements with warmup/synchronization.
4. Explain prefill/decode, weights/KV, and the limits of the memory estimate.
5. Show raw results from one comparison and explain the bottleneck or clearly justified uncertainty.

## Git and GitLab

[Practice](../modules/git-and-gitlab.md).

1. Draw HEAD, branch, commits, index, and working tree before/after your change.
2. Explain your choice of merge/rebase/revert/reset in two scenarios of your own.
3. **Critical:** recover a practice history and show that the required result is preserved.
4. Trace job/rules/runner to a specific artifact or image digest; distinguish cache from artifact.
5. **Critical:** demonstrate a practice/staging rollback and verify the result, including data compatibility if a database is involved.

## SRE and Recovery

[Practice](../modules/observability-and-sre.md).

1. Define a user-facing SLI, its denominator, window, and proposed SLO.
2. Explain why a green healthcheck can coexist with a user problem.
3. Demonstrate detection of a controlled failure and the alert's action.
4. **Critical:** recover a practice scenario using the runbook and verify the result.
5. Name a monitoring limitation and the next useful signal; distinguish no errors from no data.

## Python Exam

[Practice](../modules/01-python-foundations.md).

1. Explain mutable/immutable, scope, and an exception using your own function.
2. Predict normal and boundary results before running the code.
3. **Critical:** demonstrate correct behavior for normal/empty input and a read error or another declared failure.
4. Change a small requirement and add a behavior test that catches the corresponding error.
5. Reproduce the run from the instructions and explain the traceback without rewriting the whole program.

## Docker Exam

[Practice](../modules/02-professional-python-and-systems.md).

1. Explain image/container, build context, startup, and runtime user.
2. Trace port/network/volume; explain localhost inside a container.
3. Identify the cause of one reproducible failure from evidence, rather than a series of random rebuilds.
4. Demonstrate service shutdown and restart with a clear state.
5. **Critical:** verify persistence and recovery of a practice stateful component into a separate environment. Switching to privileged to bypass an unexplained error does not count.

## Backend and Data

[Practice](../modules/03-backend-and-databases.md).

1. Explain the endpoint contract, validation, and server-side access decision.
2. Trace the transaction boundary and repeated-request behavior.
3. **Critical:** show a negative failure/rollback test confirming that no partial state remains.
4. Explain a join and an actual query plan; justify having or not having an index.
5. **Critical:** show data checks after a migration and practice recovery; name the rollback limitations.

## QA and Evaluation

[Practice](../modules/quality-and-evaluation.md).

1. Define the behavior, baseline, metric, and regression criterion before making a change.
2. For TP=8, FP=2, FN=4, calculate precision/recall and explain the denominators.
3. **Critical:** show how tuning and final evaluation are separated; the examples' provenance and labels are known.
4. Show a regression case and explain exactly what it proves.
5. Compare results accounting for sample size, errors, and uncertainty; state the decision on accepting the change.

## Frontend and UX

[Practice](../modules/frontend-and-ux.md).

1. Explain the path from a user action to saved data.
2. Show loading/empty/error/success states and a clear way to recover from an error.
3. **Critical:** confirm persistence after reload and the absence of false success when the API fails.
4. Complete the main scenario using the keyboard and find/fix one issue, if present.
5. Show one justified E2E test or reproducible manual scenario and its limitations.

## Security Review

[Practice](../modules/security-engineering.md).

1. Draw trust boundaries and the path of sensitive data.
2. Explain where permissions are checked and why a prompt does not replace authorization.
3. **Critical:** confirm with practice users that other users' data is not returned through the API/retrieval/export paths being checked.
4. Show one authorized negative injection/egress/secrets scenario and its result.
5. Name the remaining risks, owner, and limits of the check; do not present a small set of tests as a full audit.

## LLM Systems Exam

[Practice](../modules/04-ml-llm-and-capstone.md).

1. Explain tokenization, attention, and the path from a question to context and an answer.
2. Distinguish retrieval quality, generation quality, and latency.
3. **Critical:** show a reproducible comparison of a baseline and one change on separate data.
4. **Critical:** show an unanswerable case and access control for context across different practice users.
5. Justify the next step—data, retrieval, prompt, model, or fine-tune—using results rather than an assumption.

## Technical Leadership

[Practice](../modules/technical-leadership.md).

1. Name the user, problem, baseline, and success criterion.
2. Compare alternatives accounting for cost, data, and maintenance.
3. **Critical:** show a decision with result verification, an owner, and a clear next step.
4. Explain how agent changes were verified and how scope was limited.
5. Name a condition for reconsidering the decision and a way to roll back/stop; hand over the procedure so it can be repeated.

<a id="после-проверки"></a>

## After the check

Record the result in [PROGRESS](../PROGRESS.md). If there is a gap, choose just one item for the next attempt. After successful completion, create a [personal achievement](../templates/achievement.md). Course grading and certificate issuance remain the provider's responsibility.
