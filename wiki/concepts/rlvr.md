---
title: RLVR (Reinforcement Learning from Verifiable Rewards)
type: concept
created: 2026-04-18
updated: 2026-04-18
sources: [2025/12.20.md]
tags: [training, rl, 2025-paradigm]
---

# RLVR — Reinforcement Learning from Verifiable Rewards

The 2025 training paradigm that turned [[verifiability]] into capability. From Karpathy's [[karpathy-x-2025-software-paradigm|Dec 20 year-in-review]], listed as the **#1 paradigm change of 2025**.

## The capability-overhang story

Labs had pretraining-sized compute committed, but the scaling returns were flattening. They **redirected that compute into RLVR** — reinforcement learning against tasks with clean, mechanical reward signals (math correct? unit test passes? proof typechecks?).

## The result: reasoning models with a new knob

RLVR produced a new generation of models with a test-time-compute knob, branded "thinking time":
- **o1** (late 2024) showed it.
- **o3** (early 2025) was the **inflection point**.
- By mid-2025, essentially every frontier lab shipped a reasoning variant.

The knob: at inference, spend more compute (longer chain-of-thought, more rollouts) to get better answers. This is the first clear case of **test-time compute as a product dial**.

## Why RLVR works where prior RL didn't

- **Clean rewards** — no human-preference noise, no Goodhart shape.
- **Parallel environments** — math problems, coding tasks, proofs, games all scale horizontally.
- **Sharp discrimination** — binary pass/fail is a stronger gradient than a 1-5 preference rating.

## Where RLVR can't go

Everywhere without a clean verifier:
- Writing quality
- Strategic advice
- Common-sense judgment
- Long-horizon taste decisions

This is exactly the lagging half of [[jagged-intelligence]].

## Karpathy's skepticism

Paired with [[rl-is-terrible]] — "sucking supervision through a straw." Even with verifiable rewards, the broadcast-scalar structure of RL limits how far capability climbs from any given reward signal. [[system-prompt-learning]] is his proposed next paradigm.

## Relation to other concepts

- **[[verifiable-rewards]]** — the reward shape that makes RLVR possible.
- **[[verifiability]]** — the 2025 essay-level restatement.
- **[[peaky-capability]]** — the observed capability surface RLVR produced.
- **[[reinforcement-learning|RL]]** — the parent method.
- **[[reasoning-models]]** — the category of models RLVR produced.

## Related

- [[verifiable-rewards]]
- [[verifiability]]
- [[jagged-intelligence]]
- [[peaky-capability]]
- [[rl-is-terrible]]
