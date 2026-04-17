---
title: Model Collapse
type: concept
created: 2026-04-17
updated: 2026-04-17
sources: [andrej-karpathy-were-summoning-ghosts-not-building-animals/transcript.md]
tags: [llm-training, failure-modes, data]
---

# Model Collapse

The failure mode where a model trained (or re-trained) on its own outputs loses diversity and drifts toward narrow, over-confident patterns. Karpathy uses it as a handle for a broader point: **LLMs hallucinate less with each generation not because they "know more," but because their output distributions are tightening toward a common prior.**

## Source

[Karpathy, Summoning Ghosts](../sources/summoning-ghosts-not-animals.md) — Karpathy's framing that self-distillation and synthetic data pipelines are a slow-motion collapse unless actively counteracted.

## Mechanism

1. A frontier model's outputs become training data for the next round (distillation, RLHF rollouts, synthetic corpora).
2. Each round samples from a narrower slice of the original data manifold.
3. Diversity shrinks. Mode-seeking behavior hardens.
4. Eventually the model is fluent on everything it sees often and brittle on anything it doesn't.

## Why it matters

- It caps the value of pure synthetic-data flywheels.
- It's one motivation for the [[cognitive-core]] framing: a small reasoning core with retrieval is more robust than a bloated memorizer because the memorization is where collapse bites hardest.
- It connects to [[ai-psychosis]]: a ghost that has over-fit its own distribution becomes a more confident and more systematically-wrong ghost.

## Counteracting it

- Keep human data in the loop.
- Diversify training sources deliberately.
- Use [[verifiable-rewards]] for quality control rather than letting the model police itself.

## Related

- [[ai-psychosis]]
- [[llm-cognitive-deficits]]
- [[cognitive-core]]
- [[reinforcement-learning]]
