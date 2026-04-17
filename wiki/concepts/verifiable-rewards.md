---
title: Verifiable Rewards
type: concept
created: 2026-04-15
updated: 2026-04-17
sources: [4.10.md, andrej-karpathy-were-summoning-ghosts-not-building-animals/transcript.md]
tags: [rl, capability, training]
---

# Verifiable Rewards

Reward signals that can be checked mechanically — no human judgment in the loop. Canonical example: a unit test passes or fails. Contrast: judging the quality of a piece of writing.

## Why it matters

- [Karpathy, AI Capability Gap](../sources/ai-capability-gap.md) — argues verifiable rewards are one of two key drivers of the recent "peaky" capability jump in programming/math/research.

  > "these domains offer explicit reward functions that are verifiable meaning they are easily amenable to reinforcement learning training (e.g. unit tests passed yes or no, in contrast to writing, which is much harder to explicitly judge)"

- [Karpathy, Summoning Ghosts](../sources/summoning-ghosts-not-animals.md) — sharpens the critique: even *with* verifiable rewards, [[reinforcement-learning|RL]] is "sucking supervision through a straw." One scalar at rollout end gets broadcast to every token in the trajectory, so good tokens inside failing rollouts get punished and bad tokens inside successful ones get reinforced. See [[rl-is-terrible]].

## Implications (tracked across sources)

- Domains *with* verifiable rewards are more amenable to large-scale RL and therefore more likely to see capability jumps.
- Domains *without* verifiable rewards (writing, advice, conversation) lag — this is the mechanism behind [[peaky-capability]].
- **Refined prediction (2025):** verifiable rewards are *necessary but not sufficient* — even where they exist, the broadcast-scalar structure of RL limits how far capability can climb. Process-based supervision (LLM-judge intermediate steps) is the likely next step, but introduces new reward-hacking surfaces.
- Adjacent domains with good eval harnesses (theorem proving, sysadmin, data analysis) should still be next to jump, but expect diminishing returns from RL alone.

## Related

- [[reinforcement-learning]] — the training method that consumes these rewards
- [[rl-is-terrible]] — Karpathy's 2025 critique even where verifiable rewards exist
- [[peaky-capability]] — the observed outcome
- [[model-collapse]] — a failure mode of RL that verifiable rewards don't prevent
