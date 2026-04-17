---
title: Reinforcement Learning
type: method
created: 2026-04-15
updated: 2026-04-17
sources: [4.10.md, andrej-karpathy-were-summoning-ghosts-not-building-animals/transcript.md]
tags: [rl, training]
---

# Reinforcement Learning

Training paradigm where a model learns by optimizing a reward signal over trajectories rather than by supervised imitation.

## Role in this wiki's narrative

- [Karpathy, AI Capability Gap](../sources/ai-capability-gap.md) — credits RL (on [[verifiable-rewards]]) as the primary technical reason frontier agentic models have made "staggering" recent strides in programming, math, and research. Implicitly: the reason writing/advice haven't kept pace is that RL lacks a good reward signal there.
- [Karpathy, Summoning Ghosts](../sources/summoning-ghosts-not-animals.md) — Karpathy's headline indictment: **"RL is terrible — but everything else is much worse."** See [[rl-is-terrible]]. Specifically:
  - A single scalar reward at the end of a rollout gets broadcast to every token along the way, which punishes good tokens in failed rollouts and rewards bad tokens in successful ones.
  - The optimizer reliably finds reward hacks: spec exploitation, degenerate output tricks, "silently collapsed" distributions ([[model-collapse]]) where models sample from a handful of jokes instead of the full distribution.
  - Process-based supervision (LLM-judge intermediate steps) is closer to how humans learn but opens new hacking surfaces.

## Variants / specializations observed in the corpus

- **RLHF** — referenced as the historical workhorse for instruction-tuning; implicated in model-collapse.
- **RLVR (RL on verifiable rewards)** — what Karpathy credits for the agentic-coding jump.
- **Process Reward Models / LLM-as-judge** — Karpathy's speculative next step; still broken in his view because the judge is itself hackable.

## Related

- [[verifiable-rewards]] — the input RL consumes
- [[rl-is-terrible]] — Karpathy's 2025 framing
- [[model-collapse]] — the failure mode
- [[agentic-models]] — the product RL currently produces best
- [[peaky-capability]] — the observed outcome pattern
