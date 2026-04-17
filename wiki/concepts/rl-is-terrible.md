---
title: "RL is Terrible"
type: concept
created: 2026-04-17
updated: 2026-04-17
sources: [andrej-karpathy-were-summoning-ghosts-not-building-animals/transcript.md]
tags: [reinforcement-learning, karpathy-coinage, learning-algorithms]
---

# "RL is Terrible"

Karpathy's deliberate overstatement of a real point: reinforcement learning as currently practiced for LLMs is an **information-starved** learning algorithm. The vivid phrase he uses: *"sucking supervision through a straw."*

## Source

[Karpathy, Summoning Ghosts](../sources/summoning-ghosts-not-animals.md) — the most extended critique of RL-for-LLMs in his public talks.

## The argument

For a long episode — say, a 10,000-token reasoning trace — conventional RL assigns **one scalar reward** at the end. That single bit of feedback has to be apportioned, by the gradient, across every token and every decision that led to the outcome.

- The trace contains enormous information about *which steps were good* and *which were bad*.
- The reward signal throws almost all of that away and keeps one number.
- Hence: "sucking supervision through a straw."

## Why it still works

- Large batches and many rollouts average out the noise.
- Trained models already speak coherent language, so the credit-assignment problem is less savage than in tabula-rasa RL.
- [[verifiable-rewards]] on clean domains (math, code) give relatively low-noise signals.

## What would be better

Karpathy's preferred directions, sketched in the interview:

- **Process-level supervision** — reward or critique each step, not just the end.
- **LLM-judge feedback** — models grading reasoning traces at a finer grain.
- **Agentic data** — capture long-horizon, verifiable trajectories from real deployment, not just benchmark rollouts.

## Relation to scaling

RL is where LLMs are currently scaling *hardest*, and where performance gains feel largest. Karpathy's point is not "don't do RL" but "don't mistake this for a good learning algorithm." It's the best tool we have for this step of the journey, not a permanent ingredient.

## Related

- [[reinforcement-learning]]
- [[verifiable-rewards]]
- [[agentic-models]]
- [[people-spirits]]
