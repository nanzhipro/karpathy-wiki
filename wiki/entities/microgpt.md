---
title: microGPT
type: entity
created: 2026-04-17
updated: 2026-04-17
sources: [2026/2.12.md]
tags: [repo, karpathy, education, bacterial-code]
---

# microGPT

Karpathy's Feb 12 2026 demo: **a complete GPT training and inference stack in ~200 lines of code**, zero external dependencies.

## Properties

- **Lines of code:** ~200.
- **Dependencies:** none beyond Python + PyTorch.
- **Scope:** tokenizer → model → training loop → sampling, one file.
- **Purpose:** pedagogical — and a reference exemplar for [[bacterial-code|bacterial code]].

## Position in Karpathy's educational ladder

- [[micrograd]] — scalar autograd engine.
- [[nanogpt]] — a minimal but fuller GPT training repo.
- **microGPT** — the tightest possible "full GPT" demo.
- [[nanochat]] — full-stack chat model ("strong baseline ChatGPT clone").

## Related

- [[bacterial-code]]
- [[nanochat]]
- [[nanogpt]]
- [[micrograd]]
- [[build-for-agents]]
