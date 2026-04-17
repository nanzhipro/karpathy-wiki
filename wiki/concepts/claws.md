---
title: Claws (The Orchestration Layer Above Agents)
type: concept
created: 2026-04-17
updated: 2026-04-17
sources: [2026/3.6.md, 2026/3.12.md, 2026/2.25.md]
tags: [agents, orchestration, karpathy-coinage]
---

# Claws

Karpathy's name (Mar 6 2026) for the emerging layer above coding agents: long-running orchestrators that manage multiple agents, hold persistent state and tools, and expose a unified control surface.

## The stack (Karpathy's framing)

> "Just like LLM agents were a new layer on top of LLMs, Claws are now a new layer on top of LLM agents, taking the orchestration, scheduling, context, tool calls and a kind of persistence to a next level."

| Layer | Example |
|-------|---------|
| LLM | GPT-5, Claude Sonnet, etc. |
| Agent | [[claude-code|Claude Code]], [[openai-codex|Codex]] |
| **Claw** | OpenClaw, NanoClaw, nanobot, zeroclaw, ironclaw, picoclaw |

> "First there was chat, then there was code, now there is claw. Ez"

## The design consensus Karpathy approves of

- **Small, forkable core.** NanoClaw's ~4,000-LoC core "fits in both my head and that of AI agents — manageable, auditable, flexible."
- **Containers by default.** Isolate what the Claw runs.
- **Config via skills, not config files.** `/add-telegram` is a skill that *instructs the agent to modify the repo code* — integrating by code generation rather than switches. "The implied new meta is to write the most maximally forkable repo and then have skills that fork it into any desired more exotic configuration."
- **Local-first.** Cloud-hosted Claws are harder to tinker with and can't reach home-LAN devices.

## What Claws give you

- **Multi-agent orchestration** (e.g. multiple [[claude-code|Claude Code]] or [[openai-codex|Codex]] instances in parallel).
- **Persistent memory and tool state across runs.**
- **Scheduling and long-horizon coordination** — the Jan 27 "tenacity" observation but at the *team* level.

## What Karpathy doesn't love

> "Giving my private data/keys to 400K lines of vibe coded monster that is being actively attacked at scale is not very appealing at all. Already seeing reports of exposed instances, RCE vulnerabilities, supply chain poisoning, malicious or compromised skills in the registry."

Explicit connection to [[supply-chain-attacks]] and [[bacterial-code]]: **a Claw you can't audit is a liability.**

## Dobby (Mar 12)

Karpathy's personal Claw, **"Dobby"** — "runs my entire house over WhatsApp. Lights, shades, pool/spa, sonos, security HVAC etc." One of four unfinished blog posts.

> "There is something aesthetically pleasing about there being a physical device 'possessed' by a little ghost of a personal digital house elf."

Also connects to the [[people-spirits]] frame — the Claw is a persistent house-elf ghost given a body (the Mac mini / DGX Spark).

## Related

- [[agentic-engineering]]
- [[nanoclaw]]
- [[autoresearch]]
- [[org-code]]
- [[build-for-agents]]
- [[supply-chain-attacks]]
