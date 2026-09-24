<a id="python-runtime-linux-и-containers"></a>

# Python runtime, Linux, and containers

[Module map](README.md) · [Reference materials and LFS162](../WORK_INTEGRATED_ROADMAP.md)

Open this when it is unclear how code becomes a running process. The outcome is an explained startup of one small system.

<a id="порядок-чтения"></a>

## Reading order

1. [Python tutorial](https://docs.python.org/3/tutorial/): modules/virtual environments; [typing](https://docs.python.org/3/library/typing.html) and [asyncio](https://docs.python.org/3/library/asyncio.html) for the specific code.
2. [The Linux Command Line](https://linuxcommand.org/tlcl.php): permissions, processes, I/O; [systemd](https://systemd.io/) for services.
3. [Docker overview](https://docs.docker.com/get-started/docker-overview/) → [Compose](https://docs.docker.com/compose/).
4. [Podman](https://docs.podman.io/en/latest/) if it is used in your environment; [NVIDIA Container Toolkit](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/) for GPU containers.

You do not need to install every tool at once. Record versions from the actual dev environment.

<a id="практика"></a>

## Practice

Choose one service, preferably a learning Python API.

- Trace interpreter → imports/config → process → port → response. Distinguish CPU-bound work from waiting for I/O.
- Build an image and explain the build context, layers, runtime user, and startup.
- Draw the path container → network → volume → dependency; add the GPU device for a GPU service.
- Save a practice record in a volume, restart the container, and check the data.
- Reproduce an incorrect dependency address and a test-file access failure one at a time. For each, record the symptom, observation, and smallest fix.
- Check process termination and restart. For a stateful component, separately test restoring into an empty learning environment.

An agent may assemble the configuration; the human checks permissions, paths, dependencies, and the observed result. Deleting volumes or changing production permissions is not required for the exercise.

<a id="выход"></a>

## Outcome

A run command, versions, a runtime diagram, and one verified fix. [Docker Exam](../exams/MASTER_EXAMS.md#docker-exam).

LFS162 provides an introductory foundation and its own badge under the roadmap’s conditions; this module adds Linux/container practice. Service recovery earns a personal achievement. Next: [SRE](observability-and-sre.md) or return to your current task.
