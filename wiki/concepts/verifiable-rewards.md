---
title: Verifiable Rewards
type: concept
created: 2026-04-15
updated: 2026-04-15
sources: [4.10.md]
tags: [rl, capability, training]
---

# Verifiable Rewards

Reward signals that can be checked mechanically — no human judgment in the loop. Canonical example: a unit test passes or fails. Contrast: judging the quality of a piece of writing.

## Why it matters

- [Karpathy, "AI Capability Gap"](../sources/ai-capability-gap.md) — argues verifiable rewards are one of two key drivers of the recent "peaky" capability jump in programming/math/research. *(asserted, single-source)*

  > "these domains offer explicit reward functions that are verifiable meaning they are easily amenable to reinforcement learning training (e.g. unit tests passed yes or no, in contrast to writing, which is much harder to explicitly judge)"

## Implications (to test against future sources)

- Domains *with* verifiable rewards are more amenable to large-scale [[reinforcement-learning]] and therefore more likely to see capability jumps.
- Domains *without* verifiable rewards (writing, advice, conversation) lag — this is the mechanism behind [[peaky-capability]].
- **Prediction worth tracking:** adjacent domains with good eval harnesses (theorem proving, sysadmin, data analysis) should be next to jump.

## Related

- [[reinforcement-learning]] — the training method that consumes these rewards
- [[peaky-capability]] — the observed outcome
