---
title: autoresearch
type: entity
created: 2026-04-17
updated: 2026-04-17
sources: [2026/2.28.md, 2026/3.8.md, 2026/3.9.md, 2026/3.10.md]
tags: [repo, karpathy, agents, research]
---

# autoresearch

A small, single-file agent-driven ML research harness Karpathy open-sourced on **Mar 8 2026**.

## Properties

- **Size:** ~630 lines of code.
- **Scope:** single GPU, single file — exemplar of [[bacterial-code|bacterial code]].
- **Job:** run, monitor, and branch nanochat training experiments autonomously, proposing changes, judging the results, and keeping logs.

## Why it matters

> "The dream is a SETI@home-style distributed research swarm, except instead of parsing radio signals, volunteer machines run branches of a living ML-research tree."
> — Karpathy, Mar 9 2026

- **Feb 28:** first demo — autonomous overnight ablations.
- **Mar 8:** public release.
- **Mar 10:** autoresearch-guided experiments improve nanochat's loss by ~11%.

## Related

- [[nanochat]]
- [[autoresearch|autoresearch (concept)]] — see `wiki/concepts/autoresearch.md`
- [[bacterial-code]]
- [[claws]]
