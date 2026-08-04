# Phase 5 — Backend Engineering and Databases

## Mission

Build a service whose behaviour is explicit, tested and understandable from HTTP request to database transaction.

## Primary resources

- FastAPI official tutorial
- SQLBolt
- PostgreSQL official tutorial
- SQLAlchemy 2.0 Unified Tutorial
- Alembic tutorial

## Project: Document Job API

Build an API that can:

- create a document-analysis job;
- retrieve job status;
- list findings;
- mark a finding reviewed;
- retry failed processing safely;
- reject invalid input clearly;
- preserve idempotency for duplicate requests.

## Required architecture

Use three clear layers:

1. HTTP transport: parsing, status codes and response models.
2. Service layer: business rules and orchestration.
3. Repository layer: persistence and transactions.

Do not add abstractions unless they solve an observed problem.

## Database requirements

- PostgreSQL, not SQLite, for the final project;
- foreign keys and meaningful constraints;
- indexes justified by a query;
- migrations with upgrade and downgrade paths;
- transaction boundaries documented;
- test for concurrent or duplicate job creation;
- seed data only for development.

## Testing requirements

- unit tests for business rules;
- integration tests against PostgreSQL;
- API tests for success and failure paths;
- one test that proves rollback;
- one test that proves idempotency;
- no tests that merely mirror implementation details.

## Boss fight

Implement a new requirement without AI implementation:

> A user may restore a masked value only if the finding belongs to a matter they can access. Every restoration must be audit logged, and duplicate restore requests must not create duplicate audit events.

Before coding, write:

- acceptance criteria;
- data model change;
- transaction boundary;
- tests;
- failure cases.

## Exit criteria

- can explain HTTP semantics and status choices;
- can trace a request through all layers;
- can write joins and transactions in raw SQL;
- can create and reverse a migration;
- can explain an index with `EXPLAIN` evidence;
- can diagnose a failing integration test without asking an agent to rewrite the service.
