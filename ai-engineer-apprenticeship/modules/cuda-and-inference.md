<a id="cuda-и-llm-inference"></a>

# CUDA and LLM inference

Main stage 1. [Course and award conditions](../WORK_INTEGRATED_ROADMAP.md) · [Module map](README.md)

Prerequisites: Python functions/loops, NumPy ndarray, and willingness to examine a small kernel. The goal is to understand execution and measurement, then connect them to inference behavior.

<a id="читать-и-делать-по-порядку"></a>

## Read and practice in order

1. NVIDIA CUDA Python from the roadmap: introduction → custom kernels → multidimensional grids/shared memory → assessment.
2. [Open Accelerated Python Tutorial](https://github.com/NVIDIA/accelerated-computing-hub/tree/main/tutorials/accelerated-python): memory, data transfer, asynchrony, and a small kernel.
3. [GPU Performance Background](https://docs.nvidia.com/deeplearning/performance/dl-performance-gpu-background/index.html): computation and bandwidth.
4. Roadmap section 1: transformer workload → prefill/decode → KV → serving → Nsight. Do not read the entire CUDA Guide before your first run.

<a id="практика-a-один-маленький-workload"></a>

## Exercise A: one small workload

Adding two arrays is enough for a first example.

- Before running, draw host/device, threads/blocks, and the mapping from each thread to an element.
- Check the result against the CPU; test a size that is not a multiple of the block size.
- Separately measure the full path including data transfers and computation on data that is already on the device.
- Record warmup, synchronization, size, dtype, repetitions, and versions. Claim a speedup only for comparable measurements.
- Change one parameter and explain the result; the GPU does not have to win on a small example.

If you do not have a working GPU environment, save the calculation and expected result, marked “not executed.”

<a id="практика-b-один-inference-benchmark"></a>

## Exercise B: one inference benchmark

One model, one engine/version, and fixed prompt/output lengths. Start at concurrency 1, then compare 4 and 8 if resources allow.

Record TTFT, ITL, output token count, throughput, VRAM, errors, and the number of observations. Specify streaming, quantization, GPU count, and warmup. A short sample gives only a preliminary estimate of tail latency.

Before running, estimate weights and KV memory from the config; afterward, explain the difference from runtime VRAM. Account for the architecture, overhead, and placement across GPUs. Collect one profile for a specific hypothesis, such as CPU waiting or data transfer.

<a id="выход"></a>

## Outcome

- You can explain the data path and measurement result.
- Raw measurements and comparison limits are available.
- You have one conclusion about the workload, not just a tok/s number.

[CUDA check](../exams/MASTER_EXAMS.md#cuda-and-inference). The course certificate comes from the provider’s assessment; the benchmark is a separate [achievement](../templates/achievement.md). Next: [Git/GitLab](git-and-gitlab.md).
