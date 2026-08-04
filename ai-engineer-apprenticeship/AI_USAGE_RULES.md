# AI Usage Rules

The purpose of these rules is not purity. It is to prevent speed from silently replacing competence.

## The traffic-light system

### Green — always allowed

- explain a concept using examples;
- ask Socratic questions;
- review code you already wrote;
- explain an error after you have attempted diagnosis;
- propose additional tests after you wrote the first tests;
- critique an ADR, threat model or evaluation plan;
- check documentation wording and spelling.

### Yellow — allowed with an evidence note

- generate repetitive fixtures or boilerplate;
- suggest refactoring alternatives;
- draft configuration after you write and understand the first version;
- produce a patch for a production emergency.

For yellow use, add to the commit or weekly review:

```text
AI contribution:
What it generated:
What I verified:
What I could reproduce without it:
```

### Red — prohibited during learning work

- solving mandatory exercises before your attempt;
- generating the entire feature or project;
- replacing an exam or boss fight;
- accepting code you cannot explain line by line;
- retrying prompts until tests happen to pass;
- asking the agent to "fix everything" without a failing test and diagnosis.

## The 30-minute rule

Before asking AI to fix a bug:

1. reproduce it;
2. reduce it;
3. read the traceback and relevant logs;
4. state one or more hypotheses;
5. perform at least one discriminating test.

Then ask a narrow question containing evidence.

## Required prompt shape

Bad:

> Dude, fix it properly and make no mistakes.

Good:

> Test `test_duplicate_job_is_idempotent` fails with this traceback. I traced the request through the service layer and suspect the repository commits before checking the idempotency key. Ask me diagnostic questions first; do not write a patch yet.

## Stop condition

Stop an agent loop when any of these is true:

- three prompts have not improved the same failing test;
- you stopped reading the full response;
- you cannot state the current hypothesis;
- changes span unrelated files;
- you feel the urge to deploy merely to see whether it works.

Return to the last known-good commit, write down the failure, and reduce scope.

## Module restrictions

| Phase | AI role |
|---|---|
| Setup and Python foundations | Tutor and reviewer only |
| Professional Python | Reviewer; limited boilerplate after first implementation |
| Linux, Git and Docker | Explain evidence; no blind command sequences |
| Backend and databases | Architecture critique and code review |
| ML/LLM foundations | Explain mathematics, review experiments, generate extra cases |
| Capstone | Review and adversarial testing; no whole-feature generation |

## Ownership test

Before merging, answer yes to all:

- Can I explain why this design was chosen?
- Can I trace one request through the code?
- Can I identify its failure modes?
- Can I change it safely tomorrow?
- Are tests proving behaviour rather than merely increasing coverage?

If not, the work is not owned yet.
