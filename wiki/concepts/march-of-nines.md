---
title: March of Nines
type: concept
created: 2026-04-17
updated: 2026-04-17
sources: [andrej-karpathy-software-is-changing-again/transcript.md, andrej-karpathy-were-summoning-ghosts-not-building-animals/transcript.md]
tags: [reliability, product, karpathy-coinage]
---

# March of Nines

Karpathy's framing, drawn from self-driving: **each successive "nine" of reliability (90% → 99% → 99.9% → 99.99% → ...) is a separate project of roughly equal magnitude.** Reaching 99.99% is not 10× harder than 99%; it's a whole new program of work of the same shape, repeated.

## Sources

- [Karpathy, Software Is Changing (Again)](../sources/software-is-changing-again.md) — applied to Tesla Autopilot as the deep prior. 12 years from "perfect first drive" to still-not-full-autonomy.
- [Karpathy, Summoning Ghosts](../sources/summoning-ghosts-not-animals.md) — Karpathy's most detailed treatment. Traces [[waymo|Waymo]] from 2013 demo rides to 2025 commercial deployment, explains why self-driving took so long, and **transfers the frame directly to coding agents.**

## The transfer

Demos are 90% of the way. The remaining 9%, 0.9%, 0.09% take a decade. This is why:

- [[decade-of-agents]], not year of agents.
- [[partial-autonomy-apps]] beat full-autonomy apps for the foreseeable future.
- Products should be built assuming the reliability curve is flat-ish for a while.

## Karpathy's formula

> "Every nine is a constant amount of work."

## Why reliability is sub-linear in effort

Each nine is a different *class* of failure mode. The first 90% is "the happy path works." The next 9% is "common edge cases work." The next 0.9% is "rare but predictable edge cases work." The next 0.09% is "adversarial, correlated, or long-tail weirdness works" — each requires different instrumentation, different training data, different adjudication logic. The work doesn't scale; it repeats.

## Related

- [[decade-of-agents]]
- [[tesla]], [[waymo]] — the empirical basis
- [[autonomy-slider]] — the product response
- [[partial-autonomy-apps]]
