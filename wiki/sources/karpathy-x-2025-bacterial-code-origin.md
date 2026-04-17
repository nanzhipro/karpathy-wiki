---
title: "2025-07-06 — Bacterial Code (Origination)"
type: source-summary
created: 2026-04-17
updated: 2026-04-17
sources: [2025/7.6.md]
tags: [bacterial-code, software-aesthetics, karpathy-coinage]
---

# 2025-07-06 — Bacterial Code (Origination Post)

The original coinage of [[bacterial-code]], from July 2025. The 2026 posts reference this as canon.

## The full post

> "How to build a thriving open source community by writing code like bacteria do 🦠. Bacterial code (genomes) are:
> - **small** (each line of code costs energy)
> - **modular** (organized into groups of swappable operons)
> - **self-contained** (easily 'copy paste-able' via horizontal gene transfer)
>
> If chunks of code are small, modular, self-contained and trivial to copy-and-paste, the community can thrive via horizontal gene transfer. For any function (gene) or class (operon) that you write: can you imagine someone going 'yoink' without knowing the rest of your code or having to import anything new, to gain a benefit? Could your code be a trending GitHub gist?
>
> This coding style guide has allowed bacteria to colonize every ecological nook… along with an insane diversity of carbon anabolism, energy metabolism, etc. It excels at rapid prototyping but… it can't build complex life. By comparison, the eukaryotic genome is a significantly larger, more complex, organized and coupled monorepo. Significantly less inventive but necessary for complex life — for building entire organs and coordinating their activity. With our advantage of intelligent design, it should be possible to take advantage of both. **Build a eukaryotic monorepo backbone if you have to, but maximize bacterial DNA.**"

## Biological analogy → software rule

| Biology | Software |
|---|---|
| Genome size → metabolic cost | Line count → maintenance + context-window cost |
| Operons (swappable modules) | Classes / functions that stand alone |
| Horizontal gene transfer | Copy-paste a gist without importing a framework |
| Eukaryote backbone | Monorepo for coordinated organs (UI ↔ DB ↔ infra) |
| Bacterial branch | Small dependency-free utilities, research scripts |

## What the 2026 corpus built on top

The 2026 expansions ([[karpathy-x-2026-malleable-software]], [[karpathy-x-2026-supply-chain]]) use this aesthetic to argue:
- Depend on fewer packages — every `pip install` is a potential supply-chain surface.
- Rippable code is agent-friendly — [[build-for-agents]].
- [[microgpt]] (Feb 12 2026) is a literal bacterial-code demo: a 200-line LLM.

## Why this post matters in 2025

Arrives mid-year, before the [[software-is-changing-again|YC talk]] is released publicly — gives language for what "right-shaped" LLM-collaborative code looks like. The [[autonomy-slider]]'s sweet spot shifts toward small, [[atrophy|reviewable]] diffs; bacterial code makes reviewable the *default*.

## Related

- [[bacterial-code]] — the concept page
- [[microgpt]] — the bacterial demo
- [[build-for-agents]]
- [[supply-chain-attacks]]
- [[andrej-karpathy]]
