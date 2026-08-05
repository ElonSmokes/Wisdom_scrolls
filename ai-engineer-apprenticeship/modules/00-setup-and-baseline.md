# Phase 0 — Setup and Baseline

## Mission

Establish a reproducible learning environment and measure what you can do today without shame, performance, or AI implementation.

## Setup checklist

- [ ] Python 3.12 or newer installed
- [ ] `python --version` and `pip --version` understood
- [ ] Git installed and identity configured
- [ ] VS Code with Python extension installed
- [ ] Docker installed and `docker run hello-world` completed
- [ ] Repository cloned locally
- [ ] `.venv` created and activated
- [ ] `pytest`, `ruff` and `mypy` installed

## Baseline assignment

Create `projects/baseline-text-inspector/` containing a program that:

1. accepts a UTF-8 text file path;
2. reports line, word and character counts;
3. reports the ten most common words;
4. handles missing files and decoding errors;
5. returns a non-zero exit code on failure;
6. has at least five tests;
7. contains a README with run instructions.

Restrictions:

- no AI-written implementation;
- official Python documentation is allowed;
- AI may explain a concept after you have written a specific question;
- commit at least three meaningful increments.

## Baseline questionnaire

Answer in `notes/baseline.md`:

1. What happens between running `python app.py` and seeing output?
2. What is the difference between a list, tuple, set and dictionary?
3. What is an exception?
4. What is a process? What is a port?
5. What problem does Git solve that file copies do not?
6. What is the difference between a Docker image and container?
7. What makes an HTTP request valid?
8. What is a database transaction?
9. What is a model checkpoint?
10. How would you measure whether a PII detector is good?

Write "I do not know" where appropriate. The document is a diagnostic, not a performance.

## Exit criteria

- program runs on a clean clone;
- tests pass;
- you can explain every line;
- no secrets or machine-specific paths are committed;
- `PROGRESS.md` contains the evidence link and actual hours spent.
