---
title: modded-nanoGPT
type: entity
created: 2026-04-17
updated: 2026-04-17
sources: [2026/1.8.md, 2026/1.29.md, 2026/2.2.md]
tags: [repo, karpathy, community, nanogpt]
---

# modded-nanoGPT

A community-driven, continuously tuned fork of Karpathy's [[nanogpt|nanoGPT]]. Serves as a benchmark for "GPT-2 reproduction, cheap."

## Relation to nanochat

Karpathy's Jan 8 2026 [[nanochat]] miniseries borrows several tricks from modded-nanoGPT, including:

- **Muon optimizer** — a newer, faster-converging alternative.
- **Value Embeddings** — shape tweaks that reduce training compute.

## The cost curve

Karpathy's Jan 29 note: GPT-2 reproduction, which once cost millions, now costs **under $100** on a community-tuned stack — a **~600× reduction in seven years**.

## Related

- [[nanogpt]]
- [[nanochat]]
- [[bacterial-code]]
- [[andrej-karpathy]]
