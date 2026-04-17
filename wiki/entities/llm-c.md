---
title: llm.c
type: entity
created: 2026-04-17
updated: 2026-04-17
sources: [gpu-mode-irl-2024-keynotes/transcript.md]
tags: [karpathy-project, cuda, systems, open-source]
---

# llm.c

**Type:** Open-source project (Karpathy + ~60 contributors, 2024) — GPT-2 training implemented in pure C with a pinch of C++, plus hand-written CUDA kernels. MIT-licensed, no dependencies except (optional) cuDNN, ~3000 lines of code.

## What it does

Reproduces GPT-2 1.6B training on a single H100 node in ~24 hours for ~$600. At the time of launch, ran 20% faster and used 30% less memory than PyTorch for that specific training. See [GPU MODE IRL 2024 — llm.c](../sources/gpu-mode-irl-2024-keynote.md) for the full story.

## Why it exists

- **Anger at torch.compile.** Originated when Karpathy hit unsolvable `torch.compile` errors on eval/inference while working on [[nanogpt]] for a [[zero-to-hero|Zero to Hero]] video.
- **Pedagogical ramp.** "If PyTorch + torch.compile is GCC for Software 2.0, llm.c is writing assembly." The bottom of the [[ramps-to-knowledge]] hierarchy for LLM training.
- **Training data for future LLMs.** Karpathy's bet: LLMs will become compilers writing custom C/CUDA for specific apps; llm.c is example code meant to live in their context.

## Engineering highlights (from the talk)

- All memory pre-allocated at startup — zero dynamic allocation, fully deterministic, no OOMs.
- `Packed128` data structure that forces NVCC to emit 128-bit load/store instructions.
- CUDA streams tried, failed, and surgically removed ("`Ctrl-F` for stream and nuke it").
- NCCL + ZeRO-1 (sharded optimizer state) for multi-GPU; multi-node support.
- Notable forks: AMD, C++/modern-CUDA.

## Related

- [[nanogpt]], [[nanochat]], [[micrograd]] — siblings in Karpathy's ramp hierarchy
- [[software-3-0]] — the frame that makes llm.c "assembly" for Software 2.0
- [[andrej-karpathy]]
