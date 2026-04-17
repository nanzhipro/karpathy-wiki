---
title: Prompt Injection
type: concept
created: 2026-04-18
updated: 2026-04-18
sources: [2025/7.11.md]
tags: [security, llm-risk, wild-west]
---

# Prompt Injection

Adversarial instructions hidden in data (web pages, documents, tool outputs) that an LLM agent reads and treats as instructions from the user. The 2025 equivalent of early-computing viruses.

## Karpathy's framing ([[karpathy-x-2025-misc|Jul 11 2025]])

> "Feels a bit like the wild west of early computing, with computer viruses (now = malicious prompts hiding in web data/tools), and not well developed defenses (antivirus, or a lot more developed kernel/user-space security paradigm where e.g. an agent is given very specific action types instead of the ability to run arbitrary bash scripts)."

> "Conflicted because I want to be an early adopter of LLM agents in my personal computing but the wild west of possibility is holding me back."

## Risk hierarchy

| Risk | Scenario |
|---|---|
| **Highest** | Local LLM agents ([[cursor|Cursor]], [[claude-code|Claude Code]]) — arbitrary file/network access |
| Medium | ChatGPT/web UI with [[model-context-protocol\|MCP]] Connectors enabled |
| Low | Plain ChatGPT, no connectors, no memory |

## Especially bad combinations

Connectors + memory:

> "Imagine ChatGPT telling everything it knows about you to some attacker on the internet just because you checked the wrong box in the Connectors settings."

## Toward better defenses

The security paradigm Karpathy alludes to:
- **Capability-based agent action types** — agent granted a specific verb (read file X, commit to repo Y) rather than "run arbitrary bash."
- **User-space / kernel-space separation** — untrusted content parsed in a lower-privilege context.
- **Content provenance** — cryptographic signatures on trusted content vs untrusted web data.
- **Agent-level AV** — sandboxing, signature-based detection of known injection patterns.

## Why it matters in 2026

The 2026 [[supply-chain-attacks]] corpus (litellm credential theft Mar 19, npm axios compromise Mar 31) made the same argument materially: the package ecosystem is a giant prompt-injection vector. [[bacterial-code|Bacterial code]] is in part a response.

## Relation to other concepts

- **[[supply-chain-attacks]]** — the 2026 large-scale manifestation.
- **[[build-for-agents]]** — the agent-ergonomics side of the same problem: LLM-readable everything also means LLM-injectable everything.
- **[[agentic-engineering]]** — agent workflows must assume adversarial inputs.

## Related

- [[supply-chain-attacks]]
- [[agentic-engineering]]
- [[model-context-protocol]]
- [[digital-hygiene]]
- [[claude-code]]
- [[simon-willison]]
