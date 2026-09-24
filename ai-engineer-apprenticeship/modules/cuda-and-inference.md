# CUDA и LLM inference

Основной этап 1. [Курс и условия награды](../WORK_INTEGRATED_ROADMAP.md) · [Карта модулей](README.md)

Вход: функции/циклы Python, ndarray NumPy, готовность разбирать небольшой kernel. Цель — понимать исполнение и измерение, затем связать их с поведением inference.

## Читать и делать по порядку

1. NVIDIA CUDA Python из roadmap: вводный раздел → custom kernels → multidimensional grids/shared memory → assessment.
2. [Открытый Accelerated Python Tutorial](https://github.com/NVIDIA/accelerated-computing-hub/tree/main/tutorials/accelerated-python): память, перенос данных, asynchrony, небольшой kernel.
3. [GPU Performance Background](https://docs.nvidia.com/deeplearning/performance/dl-performance-gpu-background/index.html): вычисления и bandwidth.
4. Раздел 1 roadmap: transformer workload → prefill/decode → KV → serving → Nsight. Не читать весь CUDA Guide перед первым запуском.

## Практика A: один маленький workload

Сложение двух массивов — достаточный первый пример.

- До запуска нарисовать host/device, threads/blocks и соответствие потока элементу.
- Проверить результат относительно CPU; проверить случай, когда размер не кратен размеру блока.
- Отдельно измерить полный путь с копированием данных и вычисление на уже размещённых данных.
- Указать warmup, синхронизацию, размер, dtype, повторения и версии. Ускорение фиксировать только при сопоставимых измерениях.
- Изменить один параметр и объяснить результат; GPU не обязан выигрывать на маленьком примере.

Если нет рабочего GPU-окружения, сохранить расчёт и ожидаемый результат с пометкой «запуск не выполнен».

## Практика B: один inference benchmark

Одна модель, один engine/version, фиксированные prompt/output lengths. Начать с concurrency 1, затем сравнить 4 и 8, если ресурсы позволяют.

Записать TTFT, ITL, число output tokens, throughput, VRAM, ошибки и число наблюдений. Зафиксировать streaming, quantization, количество GPU и warmup. Короткая выборка даёт только предварительную оценку хвостовых задержек.

До запуска оценить память весов и KV по config; после — объяснить разницу с runtime VRAM. Учитывать архитектуру, служебную память и размещение по GPU. Один профиль собирать для конкретной гипотезы, например ожидания CPU или передачи данных.

## Выход

- Можно объяснить путь данных и результат замера.
- Есть исходные измерения и ограничения сравнения.
- Есть один вывод о workload, а не только число tok/s.

[Проверка CUDA](../exams/MASTER_EXAMS.md#cuda-and-inference). Сертификат курса — по assessment провайдера; benchmark — отдельная [ачивка](../templates/achievement.md). Затем [Git/GitLab](git-and-gitlab.md).
