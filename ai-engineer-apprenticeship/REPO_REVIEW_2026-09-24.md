<a id="обзор-и-обновление-всего-wisdom_scrolls"></a>

# Review and update of the entire Wisdom_scrolls repository

Date: 24.09.2026. Starting commit: `39f1126870c6d58035c2c0f016851e36382c9a55`.

All 18 original Markdown files were reviewed. The repository contains learning documents; no application or service was run here. External addresses are checked against the [110-link audit](LINK_AUDIT_2026-09-24.md) performed earlier in this session.

<a id="что-найдено-и-исправлено"></a>

## Findings and fixes

| Observation | Change |
|---|---|
| The README described four stages while the syllabus retained a mandatory 32-week calendar | The active syllabus follows CUDA → Git/GitLab → SRE → RAG; the original is preserved in archive |
| Older modules began with a large manually coded Python project | Setup became a short readiness check; Python is added according to prerequisites |
| CUDA/GitLab/SRE had no dedicated practice | Corresponding modules were added with an order, assignment, and outcome |
| QA, frontend, security, and leadership were only paragraphs in the roadmap | Small exercises and checks were added for these disciplines |
| Backend/ML/containers required large projects regardless of the task | Scope is limited to one endpoint, experiment, or scenario; the capstone is optional |
| Exams specified an 80% pass without allocating points | A common 0–2 scale for each of five items; passing requires 8/10 and completed critical items |
| An unspecified broken project was proposed without source files | Checks now use your own reproducible learning artifacts |
| AI rules and the weekly review assumed mandatory manual coding | Work assistance, independent checks, and provider rules were separated |
| Aphorisms appeared to represent experience already earned | Current principles are labeled hypotheses; personal lessons require a case/evidence; older wording is preserved |
| The graveyard listed specific “mistakes” without their circumstances | Topics are labeled suggestions; no fictional incident history is created |
| Templates did not cover a course, experiment, and award | course-check, experiment, milestone, and achievement were added |
| The root README provided little navigation | Unified navigation and CONTRIBUTING update rules were added |

<a id="что-является-источником-правды"></a>

## Sources of truth

- Roadmap: courses and award conditions.
- Syllabus: sequence and prerequisites.
- Modules: practice; older numeric filenames do not determine the order.
- Progress: only actual attempts and achievements.
- Credentials: saving and printing.
- Link audit: source status on the check date.
- Archive: history; its old requirements do not automatically apply.

<a id="проверка-после-правок"></a>

## Verification after edits

Checks cover all relative Markdown links and anchors, the existence of referenced modules/templates, coverage of external addresses by the existing registry, and consistency of the main sequence. Knowledge checks link to actual modules.

This structural revision adds no new courses, award promises, or external addresses. It records no issued certificates, passed exams, new skill percentages, or completed labs.

Before publication, prepared content is compared against the diff; after publication, changed files are read again. The exact verification result and commit are available in GitHub history.

<a id="результат-локальной-проверки"></a>

## Local verification result

**34 Markdown files** were checked: all are reachable from the root README, with **0** missing internal targets or anchors. All **110 unique external addresses** are covered by the existing audit. All **11 internal checks** contain five scored items and explicitly marked critical conditions. No new external courses were added.

<a id="начать-после-обновления"></a>

## Starting after the update

Open the [roadmap](WORK_INTEGRATED_ROADMAP.md), continue the first course, and use the [CUDA module](modules/cuda-and-inference.md) for one small experiment. Open other modules as needed.
