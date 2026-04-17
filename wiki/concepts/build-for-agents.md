---
title: Build for Agents
type: concept
created: 2026-04-17
updated: 2026-04-17
sources: [andrej-karpathy-software-is-changing-again/transcript.md]
tags: [infrastructure, agents, karpathy]
---

# Build for Agents

Karpathy's companion idea to [[vibe-coding]]: the next infrastructure opportunity is not tools for humans but **tools built so that agents can use them reliably.** The web today is authored for humans; agents are second-class citizens scraping HTML. That flips.

## Source

[Karpathy, Software Is Changing (Again)](../sources/software-is-changing-again.md) — Karpathy's closing product pitch in the YC keynote.

## The three layers he highlights

1. **`llm.txt`** — a documentation format aimed at models, analogous to `robots.txt` for crawlers. Describes a site or API in terms an LLM ingests cleanly.
2. **[[model-context-protocol|MCP]]** — Anthropic's protocol for exposing tools, data, and context to models in a standard shape.
3. **gitingest and repo-flattening tools** — services that take a GitHub repo and emit a single agent-friendly artifact.

## Why this is a category

Agents have different affordances than browsers:

- They can't click; they need JSON or structured output.
- They can't see layout; they need semantics.
- They can't remember across sessions; they need context pipes.
- They hallucinate when the shape is ambiguous; they need authoritative sources.

Every piece of software that wants to be used by agents — CRM, filesystem, cloud, IDE — will need an agent-native interface.

## Complementary to vibe coding

- [[vibe-coding]] lets humans generate apps in natural language.
- Build-for-agents makes those apps easy for other models to consume.
- Together they invert the stack: humans describe, models generate, models consume.

## Related

- [[vibe-coding]]
- [[model-context-protocol]]
- [[partial-autonomy-apps]]
- [[llm-os]]
