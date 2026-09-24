<a id="backend-и-postgresql"></a>

# Backend and PostgreSQL

[Module map](README.md) · [Courses and books](../WORK_INTEGRATED_ROADMAP.md)

Prerequisites: reading Python functions and understanding HTTP request/response. Choose one endpoint or two queries; do not rewrite the entire service.

<a id="читать-в-таком-порядке"></a>

## Read in this order

[FastAPI tutorial](https://fastapi.tiangolo.com/tutorial/): validation, dependencies, testing → [Pydantic](https://pydantic.dev/docs/validation/latest/get-started/) → [PostgreSQL tutorial](https://www.postgresql.org/docs/current/tutorial.html) and [transactions](https://www.postgresql.org/docs/current/tutorial-transactions.html) → [SQLAlchemy](https://docs.sqlalchemy.org/en/20/tutorial/) → [Alembic](https://alembic.sqlalchemy.org/en/latest/tutorial.html).

For SQL foundations, you can choose CS50 SQL from the roadmap. For performance: [EXPLAIN](https://www.postgresql.org/docs/current/using-explain.html) → [indexes](https://www.postgresql.org/docs/current/indexes.html) → [MVCC](https://www.postgresql.org/docs/current/mvcc.html). Analyze the plan using a realistic learning dataset size.

<a id="практика-a-контракт-api"></a>

## Exercise A: API contract

Learning scenario: create a document-processing job and retrieve its status.

1. Specify the request, response, validation, access rules, and behavior of a repeated request.
2. Trace transport → business logic → database transaction → response.
3. Check success, invalid input, another user’s resource, and a repeated operation.
4. Simulate a failure before commit; verify that no partially written state remains.
5. Distinguish an in-process task from a durable queue; explain what happens on restart.

You do not need a separate layer just for its name. Code separation should help verify behavior.

<a id="практика-b-данные"></a>

## Exercise B: data

Prepare synthetic jobs/findings with owners. Write a join and a status query. Capture the plan before/after a justified index, comparing time and actual row counts. Account for write cost and index size.

On dev, apply a migration, check the data, and test the return path. A downgrade does not always restore deleted data; identify where a backup or forward fix is needed. Restore a backup into a separate empty database and verify known records.

<a id="выход"></a>

## Outcome

A contract and negative tests, or a DB review with a plan and restore result. [Backend and Data](../exams/MASTER_EXAMS.md#backend-and-data).

CS50P/SQL awards follow the provider’s rules; our endpoint and DB review earn personal achievements. Next, as needed: [QA](quality-and-evaluation.md) and [Security](security-engineering.md).
