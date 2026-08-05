# Phase 2–4 — Professional Python, Linux, Git and Docker

## Mission

Turn working scripts into maintainable software and understand the operating environment beneath them.

## Professional Python deliverable

Refactor the document inspection CLI into a package with:

- `src/` and `tests/` layout;
- `pyproject.toml`;
- typed public functions;
- dataclasses or Pydantic models where useful;
- environment-based configuration;
- structured logging;
- pytest, Ruff and mypy checks;
- a console entry point.

Write one ADR explaining a real design choice, such as regex registry design or error-handling policy.

## Linux lab

Create a disposable Linux VM or container and demonstrate:

- users, groups and permissions;
- process inspection and signals;
- environment variables;
- stdout/stderr and pipes;
- filesystem and disk inspection;
- listening ports and active connections;
- DNS lookup and route inspection;
- logs for a failed service;
- SSH keys and host verification.

For each command, write what evidence it provides. Do not maintain a magic-command list.

## Git lab

Use a training repository to perform:

- feature branches and pull requests;
- merge conflict resolution;
- interactive rebase;
- revert of a bad commit;
- `git bisect` to locate an introduced defect;
- recovery of a lost commit through reflog.

## Docker project

Containerize the packaged application.

Required:

- small, reproducible Dockerfile;
- non-root runtime user;
- `.dockerignore`;
- explicit dependency installation;
- graceful signal handling;
- persistent input/output mount;
- health check when an HTTP service is introduced;
- Compose file with at least two services;
- written explanation of layers, build cache, CMD, ENTRYPOINT and networking.

## Boss fight

You receive a Compose stack where:

- the API cannot resolve the database;
- the volume is owned by the wrong UID;
- the container exits on SIGTERM incorrectly;
- a dependency is missing from the final image;
- the health check targets the wrong interface.

Diagnose each fault from evidence and write a short incident report.

## Exit criteria

- can create a package without a template generator;
- can explain a traceback and use a debugger;
- can diagnose a service using processes, ports, DNS and logs;
- can write a Dockerfile and Compose file without agent generation;
- passes the Docker exam.
