# ML, RAG и небольшой capstone

Основной этап 4. [NVIDIA RAG и prerequisites](../WORK_INTEGRATED_ROADMAP.md) · [Карта модулей](README.md)

Вход: Python/OOP, основы deep learning; для курса рекомендована работа с PyTorch. Начинать с задачи и измеримого baseline.

## По порядку

1. [Google ML Crash Course](https://developers.google.com/machine-learning/crash-course): splits, overfitting, classification/evaluation.
2. [PyTorch Basics](https://docs.pytorch.org/tutorials/beginner/basics/) и [HF LLM Course](https://huggingface.co/learn/llm-course/chapter1/1) — нужные пробелы, не обязательное чтение обоих курсов целиком.
3. NVIDIA Building RAG Agents из roadmap → assessment.
4. [Stanford IR](https://nlp.stanford.edu/IR-book/): retrieval/evaluation; [Qdrant docs](https://qdrant.tech/documentation/) — если он выбран для практики.
5. PEFT/fine-tuning брать после baseline и доказанной потребности; ссылки и книги остаются в roadmap.

## Практика: маленький поиск по документам

Подготовить около 20 синтетических документов и 20 вопросов. Добавить вопросы без ответа и документы разных учебных владельцев. Такой набор проверяет механику, а не доказывает production-качество.

- Зафиксировать простой baseline, затем embedding retrieval и при необходимости reranking.
- Для вопросов указать релевантные документы; отделить примеры для настройки от итоговой проверки.
- Измерять retrieval отдельно от generation: найден ли источник, отвечает ли ответ на вопрос, подтверждён ли он источником, где система должна отказаться.
- Проверить, что контекст и ответ не раскрывают документы другого владельца. Post-filter после генерации не заменяет контроль доступа.
- Сравнить один параметр: chunk size, k или reranker. Сохранить конфигурации, сырые результаты и ошибки.
- LLM-as-judge использовать с проверкой на размеченных примерах; не объявлять его оценку независимой истиной.

[QA-модуль](quality-and-evaluation.md) помогает с выборкой и регрессиями. Serving и нагрузку разбирать в [CUDA/inference](cuda-and-inference.md).

## Capstone — по желанию, один сценарий

Выбрать **либо** поиск с цитатами, **либо** review PII findings. Не требуется одновременно строить два продукта.

Состав: синтетические входы → backend → выбранный pipeline → review/API → экспорт результата. Добавить один quality report, границу доступа, воспроизводимый запуск и сценарий восстановления. Интерфейс может быть минимальным.

Финиш — другой человек или ты из чистого учебного окружения воспроизводит запуск, проверяет один успешный и один ошибочный сценарий. Реальная эксплуатация требует отдельной приёмки.

## Выход и награда

Есть baseline, честное сравнение и понятные ограничения. [LLM Systems Exam](../exams/MASTER_EXAMS.md#llm-systems-exam).

Сертификат NVIDIA относится к завершению курса. Собственный retrieval baseline и capstone дают отдельные личные ачивки; замкнутый проект можно отметить до любого следующего курса.
