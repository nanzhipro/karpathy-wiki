---
title: Model Context Protocol (MCP)
type: entity
created: 2026-04-17
updated: 2026-04-17
sources: [andrej-karpathy-software-is-changing-again/transcript.md]
tags: [protocol, anthropic, agents, infrastructure]
---

# Model Context Protocol (MCP)

Anthropic's open protocol for exposing tools, data, and context to LLMs in a standardized shape. One of the three concrete examples Karpathy uses when making the [[build-for-agents]] pitch in his YC talk.

## What it is

- A client/server spec where applications ("MCP servers") expose tools and resources that any MCP-aware LLM client can discover and use.
- Standardizes the shape of tool definitions, resource fetches, and streamed responses — reducing bespoke glue per integration.

## Why Karpathy flags it

- Agents need predictable, enumerable interfaces. HTML was built for humans; MCP is built for models.
- Protocols beat per-app integrations in the long run; MCP is a serious attempt at the protocol layer.
- Sits in the same conceptual bucket as `lm.txt` and repo-flattening tools like gitingest: **agent-facing infrastructure.**

## Position

- Anthropic's contribution to the [[llm-os]] stack's peripherals layer.
- A protocol, not a product — success looks like ubiquity, not market share.

## Related

- [[build-for-agents]]
- [[claude-code]]
- [[llm-os]]
