---
title: llm-council
type: entity
created: 2026-04-18
updated: 2026-04-18
sources: [2025/11.23.md]
tags: [karpathy-project, vibe-coded, multi-model]
---

# llm-council

Karpathy's [[karpathy-x-2025-evals-and-model-vibes|Nov 23 2025]] vibe-coded project: a local app that queries multiple frontier models in parallel, then has them critique each other's answers.

## What it does

1. User asks a question.
2. The app fans the query out to GPT-5, Claude, Gemini, Grok (etc.).
3. Each model sees the others' answers and writes a critique.
4. A final "chair" model synthesizes a consensus or points out where the panel disagrees.

## Why Karpathy built it

- **Escape single-model taste.** He's noted that [[karpathy-x-2025-evals-and-model-vibes|model "vibes"]] diverge — one model's confident answer can be another's obvious mistake.
- **Calibrated disagreement is information.** Where the council *agrees* is probably right; where it *splits*, you've found the interesting question.
- **Demo of the [[code-post-scarcity]] regime.** A multi-model orchestration app used to be a startup. Now it's a weekend project.

## Related

- [[code-post-scarcity]]
- [[vibe-coding]]
- [[verification-gap]]
- [[andrej-karpathy]]
