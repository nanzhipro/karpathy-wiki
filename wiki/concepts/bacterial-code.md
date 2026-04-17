---
title: Bacterial Code
type: concept
created: 2026-04-17
updated: 2026-04-17
sources: [2026/2.12.md, 2026/3.19.md, 2026/3.31.md]
tags: [architecture, dependencies, karpathy-coinage]
---

# Bacterial Code

Karpathy's aesthetic (Feb 12 2026) for code designed to be **easily ripped out and reused**. The analogy: bacteria have small, self-contained genomes that can horizontally transfer between organisms. Code written in this style survives the [[agentic-engineering|agent era]] better than tangled, dependency-heavy monoliths.

## The properties

> "Building more **'bacterial code'** — code that is less tangled, more self-contained, more dependency-free, more stateless, much easier to rip out from the repo."

— Karpathy, Feb 12 2026

| Property | What it means in practice |
|----------|---------------------------|
| Less tangled | Narrow call graphs; no hidden coupling |
| Self-contained | A single file or tight cluster, minimal imports |
| Dependency-free | Prefer stdlib / inline over `pip install monster` |
| Stateless | No hidden globals; fresh run = same result |
| Easily rippable | Agents can lift it into another project cleanly |

## The "yoink" workflow

On Feb 12, Karpathy demonstrated the pattern: he wanted fp8 training without the `torchao` dependency. He told Claude:

> "Use DeepWiki MCP and Github CLI to look at how torchao implements fp8 training. Is it possible to 'rip out' the functionality? Implement nanochat/fp8.py that has identical API but is fully self-contained."

Claude produced **150 lines of self-contained fp8 training** that runs 3% faster than torchao in his setup, with tests proving equivalence.

> "Libraries are over, LLMs are the new compiler." *(half-joking)*

## Why this matters in 2026

1. **Dependencies are a supply-chain attack surface.** See [[supply-chain-attacks]] — litellm, npm axios, etc. A `pip install` can own your machine.
2. **LLMs make the "import → re-derive" cost-benefit very different.** What was expensive to rewrite becomes cheap; the library's code-as-docs is better leverage than its binary artifact.
3. **Agents navigate bacterial repos more effectively.** Less latent knowledge, fewer cross-file gotchas.

## The stance Karpathy has evolved toward

> "Classical software engineering would have you believe that dependencies are good (we're building pyramids from bricks), but imo this has to be re-evaluated."

— Karpathy, Mar 19 2026

## Concrete exemplars

- [[microgpt]] — 200 LoC, dependency-free, full GPT train + inference.
- [[nanochat]]'s ripped-in `fp8.py` — 150 LoC, replacing torchao.
- [[autoresearch]] — 630 LoC, single-GPU, one file.

## Related

- [[supply-chain-attacks]]
- [[build-for-agents]]
- [[microgpt]]
- [[deepwiki]]
- [[agentic-engineering]]
