# Frontend и проверка пользовательского сценария

[Карта модулей](README.md) · [Курс Full Stack Open и награда](../WORK_INTEGRATED_ROADMAP.md)

Цель — понимать путь от действия пользователя до сохранённого результата. Агент может писать UI; человек проверяет поведение.

## Порядок чтения

[MDN](https://developer.mozilla.org/en-US/docs/Learn_web_development): HTML/CSS/HTTP → [TypeScript](https://www.typescriptlang.org/docs/handbook/intro.html) → [React](https://react.dev/learn): state/effects → [Next.js](https://nextjs.org/learn), если он в стеке → [WAI](https://www.w3.org/WAI/tutorials/) → [Playwright](https://playwright.dev/docs/intro).

Full Stack Open — длинный факультатив для системного обучения. Небольшой UX review можно сделать раньше.

## Практика: один review flow

Выбрать «открыть finding → изменить решение → сохранить → увидеть результат после reload».

- Описать API contract и единственный источник сохранённого состояния.
- Проверить loading, empty, success, validation error, server error и медленный ответ.
- Проверить двойной submit, повтор после ошибки и несохранённые изменения.
- Пройти сценарий клавиатурой: видимый focus, подписи полей, понятное сообщение об ошибке.
- На dev воспроизвести недоступность API; интерфейс не должен показывать ложный успех.
- Добавить один E2E-тест на критичный путь и один негативный сценарий, если они защищают значимый риск.

Скриншоты помогают review, но не заменяют проверку действия и сохранения данных. Не переносить секреты в browser bundle.

## Выход

Короткая карта состояний, замечания с воспроизводимыми шагами и проверка после исправления. [Frontend and UX](../exams/MASTER_EXAMS.md#frontend-and-ux).

За свой сценарий — личная ачивка. Сертификат Full Stack Open требует выполнения его упражнений; наш UI review не заменяет сдачу курса.
