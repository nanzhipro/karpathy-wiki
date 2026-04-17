---
title: nanoGPT
type: entity
created: 2026-04-17
updated: 2026-04-17
sources: [gpu-mode-irl-2024-keynotes/transcript.md, andrej-karpathy-were-summoning-ghosts-not-building-animals/transcript.md]
tags: [karpathy-project, education, open-source, llm]
---

# nanoGPT

**Type:** Open-source project (Karpathy, 2022+) — a minimal PyTorch implementation of GPT pretraining. "The simplest, fastest repository for training/finetuning medium-sized GPTs."

## Relevance to this wiki

- The origin of [[llm-c]]. In [[gpu-mode-irl-2024-keynote]], Karpathy describes being "stuck hacking on nanoGPT" when `torch.compile` errors on eval drove him to rewrite the whole thing in C.
- Part of the [[ramps-to-knowledge]] hierarchy: [[micrograd]] → [[nanogpt]] → [[nanochat]] → [[llm-c]]. Each one strips one more layer of abstraction.
- Referenced in [[summoning-ghosts-not-animals]] as a teaching artifact Karpathy uses when talking about [[eureka|Eureka]].

## Related

- [[llm-c]] — the C/CUDA rewrite
- [[nanochat]], [[micrograd]] — siblings in the ramp hierarchy
- [[andrej-karpathy]]
