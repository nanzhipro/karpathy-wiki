---
title: Verifiability (Software 2.0 Automation Predicate)
type: concept
created: 2026-04-18
updated: 2026-04-18
sources: [2025/11.17.md, 2025/12.20.md]
tags: [rl, software-2-0, automation, karpathy-essay]
---

# Verifiability

Karpathy's [[karpathy-x-2025-software-paradigm|Nov 17 2025]] compact restatement of the Software 2.0 automation predicate:

> **Software 1.0 easily automates what you can specify.**
> **Software 2.0 easily automates what you can verify.**

## The shift

| Era | Predicate of automation |
|---|---|
| Software 1.0 (1980s) | Whether the algorithm was **fixed** (rote rules) |
| Software 2.0 (present) | Whether there's a **resettable, efficient, rewardable environment** for the AI to practice in |

Verifiable → optimizable via [[reinforcement-learning|RL]] → neural nets learn to excel.

Non-verifiable → hope for generalization, or imitation. Significantly slower progress.

## Implication: the mechanism behind jagged intelligence

[[jagged-intelligence]] isn't random — it tracks **which domains have good verifiers**.

- **Leap-ahead:** math, code, puzzles, games, theorem proving, some systems admin — resettable, efficient, rewardable.
- **Lagging:** creative, strategic, common-sense, long-horizon, advice, writing, taste — non-verifiable or only verifiable by expensive / subjective human review.

## Why this framing matters

- **Capital-allocation guide** — want to automate a job? Ask first: does the job have a verifier? If yes, build the verifier. If no, expect slow imitation-based progress.
- **Research direction** — the interesting frontier is *making non-verifiable things verifiable*. [[autoresearch]] is an attempt to do this for ML research itself.
- **Benchmark critique** — the [[karpathy-x-2025-software-paradigm|Dec 20 year-in-review]] says "training on the test set is a new art form" and admits a **general apathy and loss of trust in benchmarks**. The fix is better environments, not better leaderboards.

## Relation to other concepts

- **[[verifiable-rewards]]** — the RL-facing name for the same idea, with caveats on noise.
- **[[rlvr]]** — RL from Verifiable Rewards; the 2025 training paradigm that operationalized this.
- **[[jagged-intelligence]]** — the observed result.
- **[[peaky-capability]]** — the same story, told as a capability-surface topography.
- **[[rl-is-terrible]]** — why verifiability is **necessary but not sufficient**.

## Related

- [[software-2-0]]
- [[software-3-0]]
- [[reinforcement-learning]]
- [[peaky-capability]]
- [[autoresearch]]
