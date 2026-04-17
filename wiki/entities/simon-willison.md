---
title: Simon Willison
type: entity
created: 2026-04-18
updated: 2026-04-18
sources: [2025/7.11.md]
tags: [person, llm-commentator, security]
---

# Simon Willison

Independent developer and writer; the most prolific practical commentator on LLM security and tooling. Referenced by Karpathy in [[karpathy-x-2025-misc|Jul 11 2025]] on [[prompt-injection]].

## Why he's a load-bearing reference for 2025

Willison popularized the term **"prompt injection"** (2022), catalogued dozens of attack variants, and in 2025 became the canonical source developers linked to when explaining why "treat tool outputs as untrusted input" was no longer optional.

- Runs [simonwillison.net](https://simonwillison.net) — the de facto logbook for LLM developers.
- Author of *Datasette* and other open-source tools.
- Frequent coiner of terms that stick (prompt injection, *Tools aren't safe*, *the lethal trifecta*).

## Karpathy's overlap

Karpathy's [[prompt-injection|Jul 11 wild-west-of-computing post]] lands in territory Willison has been mapping for years. Karpathy's framing (agents need kernel/user-space-style separation, capability-based actions) is compatible with Willison's practical warnings (connectors + memory = data exfiltration vector).

## Related

- [[prompt-injection]]
- [[supply-chain-attacks]]
- [[model-context-protocol]]
