# Python runtime, Linux и containers

[Карта модулей](README.md) · [Справочник и LFS162](../WORK_INTEGRATED_ROADMAP.md)

Открывать, когда неясно, как код становится работающим процессом. Результат — объяснённый запуск одной небольшой системы.

## Порядок чтения

1. [Python tutorial](https://docs.python.org/3/tutorial/): modules/virtual environments; [typing](https://docs.python.org/3/library/typing.html) и [asyncio](https://docs.python.org/3/library/asyncio.html) под конкретный код.
2. [The Linux Command Line](https://linuxcommand.org/tlcl.php): permissions, processes, I/O; [systemd](https://systemd.io/) для сервисов.
3. [Docker overview](https://docs.docker.com/get-started/docker-overview/) → [Compose](https://docs.docker.com/compose/).
4. [Podman](https://docs.podman.io/en/latest/) — если он используется в твоём окружении; [NVIDIA Container Toolkit](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/) — для GPU-контейнеров.

Установка всех инструментов сразу не нужна. Версии фиксировать по фактическому dev-окружению.

## Практика

Выбрать один сервис, предпочтительно учебный Python API.

- Проследить interpreter → imports/config → process → port → response. Отличить CPU-bound работу от ожидания I/O.
- Собрать image и объяснить build context, слои, runtime user и запуск.
- Нарисовать путь container → network → volume → dependency; при GPU-сервисе добавить GPU device.
- Сохранить учебную запись в volume, перезапустить контейнер и проверить данные.
- По одному воспроизвести неверный адрес зависимости и отказ доступа к тестовому файлу. Для каждого записать симптом, наблюдение и минимальное исправление.
- Проверить завершение процесса и повторный запуск. Для stateful-компонента отдельно проверить restore в пустое учебное окружение.

Агент может собирать конфигурацию; человек проверяет права, пути, зависимости и наблюдаемый результат. Удалять volumes или менять права на production ради упражнения не требуется.

## Выход

Есть команда запуска, версии, схема runtime и одно подтверждённое исправление. [Docker Exam](../exams/MASTER_EXAMS.md#docker-exam).

LFS162 даёт вводную основу и собственный badge по условиям roadmap; этот модуль углубляет практику Linux/containers. За восстановление сервиса — личная ачивка. Далее [SRE](observability-and-sre.md) или возврат к текущей задаче.
