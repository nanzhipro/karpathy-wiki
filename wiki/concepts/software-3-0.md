---
title: Software 3.0
type: concept
created: 2026-04-17
updated: 2026-04-17
sources: [andrej-karpathy-software-is-changing-again/transcript.md, gpu-mode-irl-2024-keynotes/transcript.md]
tags: [software-paradigm, llm, karpathy-coinage]
---

# Software 3.0

Karpathy's tripartite framing of how software is produced. Each paradigm is a different *substrate* with different tooling, skills, and economics.

| Paradigm | Substrate | Written by | Dominant tooling |
|---|---|---|---|
| **Software 1.0** | Source code | Humans, in programming languages | IDEs, compilers, GitHub |
| **Software 2.0** | Neural-net weights | Optimizers, on datasets | PyTorch, Hugging Face (Karpathy: "the GitHub of Software 2.0") |
| **Software 3.0** | LLM prompts | Humans, in English | Prompts, context windows, agent harnesses |

## Sources

- [Karpathy, Software Is Changing (Again)](../sources/software-is-changing-again.md) — the definitional talk. "Software has just changed, twice, in 70 years. We're in the middle of the second rewrite."
- [Karpathy, GPU MODE IRL 2024 — llm.c](../sources/gpu-mode-irl-2024-keynote.md) — applies the hierarchy as an *execution stack*: Python/PyTorch is the high-level language, `torch.compile` is the compiler, hand-written CUDA (`llm.c`) is the assembly.

## Karpathy's consequential claims

1. **Substrate eats substrate.** Software 2.0 is visibly eating 1.0 (Tesla Autopilot: C++ replaced by weights layer by layer). Software 3.0 is starting to eat 2.0 (prompts orchestrate model calls that used to be hard-coded pipelines).
2. **Everyone is a programmer now.** English is the new programming language; [[vibe-coding]] follows.
3. **The hard part is not coding.** Karpathy's MenuGen experience: writing the code is the easy part; the "DevOps" of making it real (Apple Dev IDs, payments, hosting) is the week-long grind.
4. **LLMs may become the compiler for Software 2.0.** [[llm-c|llm.c]]'s existence is framed as preparation for a world where LLMs emit custom low-level code on demand.

## Related

- [[llm-os]] — the runtime side of the Software 3.0 world
- [[vibe-coding]] — the user-facing experience of Software 3.0
- [[build-for-agents]] — infrastructure changes required by Software 3.0
- [[llm-c]]
