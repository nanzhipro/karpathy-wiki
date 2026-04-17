---
title: DeepWiki
type: entity
created: 2026-04-17
updated: 2026-04-17
sources: [2026/2.12.md]
tags: [tool, agents, documentation]
---

# DeepWiki

An agent-oriented product that turns GitHub repositories into structured, LLM-queryable wikis. Exposed to agents over MCP.

## Karpathy's use

On Feb 12 2026, he used DeepWiki MCP + GitHub CLI to have Claude study `torchao`'s fp8 training internals and **rip out** a ~150-line self-contained equivalent for nanochat. The exchange demonstrated the [[bacterial-code#the-yoink-workflow|yoink workflow]]:

> "Use DeepWiki MCP and Github CLI to look at how torchao implements fp8 training. Is it possible to 'rip out' the functionality? Implement nanochat/fp8.py that has identical API but is fully self-contained."

## Why it matters in the 2026 stack

- **Repos as documentation.** Agents consume DeepWiki pages instead of parsing source.
- **Aligns with [[build-for-agents]].** Products exposing structured agent-readable views get used by agents.
- **Leverage for bacterial-code.** Makes "rip it out and inline" cheaper than "`pip install` and pray."

## Related

- [[bacterial-code]]
- [[model-context-protocol]]
- [[build-for-agents]]
- [[nanochat]]
