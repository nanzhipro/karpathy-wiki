---
title: PyTorch
type: entity
created: 2026-04-17
updated: 2026-04-17
sources: [andrej-karpathy-gpu-mode-irl-2024-keynote/transcript.md]
tags: [framework, ml-infrastructure]
---

# PyTorch

The dominant deep-learning framework. In the GPU Mode talk Karpathy uses PyTorch as both the tool he'd normally reach for and the thing [[llm-c|llm.c]] was written in reaction to — specifically, the pain of `torch.compile` failing on his 1.6B-param GPT-2 training job.

## Role in the llm.c origin story

- **The trigger.** `torch.compile` errors sent Karpathy down the "what if I just write it in C?" path.
- **The baseline.** llm.c measures itself against equivalent PyTorch configurations — 30% less memory, ~20% faster throughput on the same workload.
- **The abstraction to escape.** Karpathy enumerates what PyTorch provides (autograd, `nn.Module`, optimizers, distributed, dtype promotion) and which of those he had to re-implement manually.

## Karpathy's posture

Not anti-PyTorch. Anti-*magic you can't inspect when the build is broken and the debugger can't help*. PyTorch is the right default for most users; llm.c is an argument for knowing what's underneath.

## Related

- [[llm-c]]
- [[nanogpt]]
- [[software-3-0]] — llm.c is presented as "assembly of Software 2.0"
