# Backend и PostgreSQL

[Карта модулей](README.md) · [Курсы и книги](../WORK_INTEGRATED_ROADMAP.md)

Вход: читать Python-функции и понимать HTTP request/response. Выбрать один endpoint или два запроса, не переписывать весь сервис.

## Читать в таком порядке

[FastAPI tutorial](https://fastapi.tiangolo.com/tutorial/): validation, dependencies, testing → [Pydantic](https://pydantic.dev/docs/validation/latest/get-started/) → [PostgreSQL tutorial](https://www.postgresql.org/docs/current/tutorial.html) и [transactions](https://www.postgresql.org/docs/current/tutorial-transactions.html) → [SQLAlchemy](https://docs.sqlalchemy.org/en/20/tutorial/) → [Alembic](https://alembic.sqlalchemy.org/en/latest/tutorial.html).

Для SQL-основ можно выбрать CS50 SQL из roadmap. Для производительности: [EXPLAIN](https://www.postgresql.org/docs/current/using-explain.html) → [indexes](https://www.postgresql.org/docs/current/indexes.html) → [MVCC](https://www.postgresql.org/docs/current/mvcc.html). Разбирать план на реалистичном учебном размере данных.

## Практика A: контракт API

Учебный сценарий: создание задания обработки документа и получение статуса.

1. Записать запрос, ответ, валидацию, правила доступа и поведение повторного запроса.
2. Проследить путь transport → business logic → database transaction → response.
3. Проверить успех, неверный вход, чужой ресурс и повтор операции.
4. Смоделировать отказ до commit; убедиться, что нет частично записанного состояния.
5. Различить задачу в памяти процесса и устойчивую очередь; объяснить, что произойдёт при restart.

Не требуется создавать отдельный слой ради названия. Разделение кода должно помогать проверять поведение.

## Практика B: данные

Подготовить синтетические jobs/findings с владельцами. Написать join и запрос по статусу. Снять plan до/после обоснованного индекса, сравнить время и фактическое число строк. Учесть цену записи и размер индекса.

На dev применить миграцию, проверить данные и путь возврата. Downgrade не всегда восстанавливает удалённые данные; определить, где нужен backup или forward fix. Восстановить backup в отдельную пустую БД и проверить известные записи.

## Выход

Контракт и негативные тесты либо DB review с plan и результатом восстановления. [Backend and Data](../exams/MASTER_EXAMS.md#backend-and-data).

CS50P/SQL награды — по правилам провайдера; наш endpoint и DB review — личные ачивки. Далее по задаче [QA](quality-and-evaluation.md) и [Security](security-engineering.md).
