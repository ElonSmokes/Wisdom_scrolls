<a id="frontend-и-проверка-пользовательского-сценария"></a>

# Frontend and user scenario verification

[Module map](README.md) · [Full Stack Open course and award](../WORK_INTEGRATED_ROADMAP.md)

The goal is to understand the path from a user action to a saved result. An agent may write the UI; the human checks its behavior.

<a id="порядок-чтения"></a>

## Reading order

[MDN](https://developer.mozilla.org/en-US/docs/Learn_web_development): HTML/CSS/HTTP → [TypeScript](https://www.typescriptlang.org/docs/handbook/intro.html) → [React](https://react.dev/learn): state/effects → [Next.js](https://nextjs.org/learn) if it is in the stack → [WAI](https://www.w3.org/WAI/tutorials/) → [Playwright](https://playwright.dev/docs/intro).

Full Stack Open is a long elective for systematic learning. A small UX review can be done earlier.

<a id="практика-один-review-flow"></a>

## Practice: one review flow

Choose “open a finding → change the decision → save → see the result after reload.”

- Describe the API contract and single source of saved state.
- Check loading, empty, success, validation error, server error, and a slow response.
- Check double submit, retry after error, and unsaved changes.
- Complete the scenario using the keyboard: visible focus, field labels, and an understandable error message.
- On dev, reproduce API unavailability; the interface must not show false success.
- Add one E2E test for the critical path and one negative scenario if they protect against a significant risk.

Screenshots help with review but do not replace checking the action and data persistence. Do not put secrets in the browser bundle.

<a id="выход"></a>

## Outcome

A short state map, findings with reproduction steps, and a check after the fix. [Frontend and UX](../exams/MASTER_EXAMS.md#frontend-and-ux).

Your scenario earns a personal achievement. The Full Stack Open certificate requires its exercises to be completed; our UI review does not replace course submissions.
