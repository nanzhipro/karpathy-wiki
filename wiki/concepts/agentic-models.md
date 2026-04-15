---
title: Agentic Models
type: concept
created: 2026-04-15
updated: 2026-04-15
sources: [4.10.md]
tags: [agentic, capability]
---

# Agentic Models

Models that act over long horizons given access to tools (a terminal, a filesystem, code execution) rather than answering single-turn queries.

## Characterizations from sources

- [Karpathy, "AI Capability Gap"](../sources/ai-capability-gap.md) — implicit definition: "When you hand a computer terminal to one of these models" they can "go off for 1 hour to coherently restructure an entire code base, or find and exploit vulnerabilities in computer systems." Canonical examples: [[openai-codex|OpenAI Codex]] and [[claude-code|Claude Code]].

## Key properties (observed so far)

- **Long-horizon action.** Measured in hours of autonomous work, not seconds.
- **Tool use.** Terminal, code execution, filesystem.
- **Trained with [[reinforcement-learning]] on [[verifiable-rewards]].** This is the mechanism Karpathy credits for their recent capability jump.

## Related

- [[peaky-capability]] — why agentic models shine in programming but not in advice/writing
