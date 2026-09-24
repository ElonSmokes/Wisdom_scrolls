<a id="git-и-gitlab-cicd"></a>

# Git and GitLab CI/CD

Main stage 2. [Course and exam](../WORK_INTEGRATED_ROADMAP.md) · [Module map](README.md)

The goal is to understand change history and the path from a commit to a running artifact.

<a id="по-порядку"></a>

## In order

1. [Pro Git](https://git-scm.com/book/en/v2): chapters 1–3; then searching, rewriting history, reset/debugging; selected objects/references sections.
2. Explain the working tree, index, commit, HEAD, and branch pointer using your own learning example.
3. Complete the GitLab learning path from the roadmap.
4. [CI quick start](https://docs.gitlab.com/ci/quick_start/) → [YAML](https://docs.gitlab.com/ci/yaml/) → [Runner](https://docs.gitlab.com/runner/). Check features against your GitLab version.

<a id="практика-a-история-в-отдельном-репозитории"></a>

## Exercise A: history in a separate repository

Create a text file and three small commits. Make two branches that change the same line; produce and deliberately resolve a conflict. Undo one published practice commit with revert. In a separate branch, recover a lost reference using reflog.

For bisect, create a known good commit, several changes, and a commit with a reproducible error. Write down the good/bad criterion before searching. The goal is to find the change and explain why it caused the problem.

Before changing history, always understand which commits are available to others. The exercise does not require force-pushing to a shared branch.

<a id="практика-b-pipeline"></a>

## Exercise B: pipeline

In a learning project or authorized staging environment, trace:

`commit → job/rules → runner → build → artifact/image digest → test → deploy → smoke check → rollback`.

Distinguish artifacts from cache; identify where the image, token, and variables come from. Create or fix one job with a verifiable result. Rehearse returning to a previous artifact; consider database schema compatibility beforehand.

If no runner is available, finish part A and the YAML review; leave pipeline execution marked “not verified.” You cannot record a green status from reading the configuration alone.

<a id="выход"></a>

## Outcome

A pipeline diagram, an explained diff, and evidence of recovery on a learning environment. [Git check](../exams/MASTER_EXAMS.md#git-and-gitlab).

Purchase the GitLab exam after preparation: the access window and conditions are in the roadmap. A personal practice achievement does not replace GitLab certification. The next main stage is [SRE](observability-and-sre.md).
