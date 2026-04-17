---
title: Agentic Models
type: concept
created: 2026-04-15
updated: 2026-04-17
sources: [4.10.md, andrej-karpathy-software-is-changing-again/transcript.md, andrej-karpathy-were-summoning-ghosts-not-building-animals/transcript.md]
tags: [agentic, capability, product]
---

# Agentic Models

Models that act over long horizons given access to tools (a terminal, a filesystem, code execution, a browser) rather than answering single-turn queries.

## Characterizations from sources

- [Karpathy, AI Capability Gap](../sources/ai-capability-gap.md) — canonical framing: "When you hand a computer terminal to one of these models" they "go off for 1 hour to coherently restructure an entire code base, or find and exploit vulnerabilities in computer systems." Canonical examples: [[openai-codex|OpenAI Codex]] and [[claude-code|Claude Code]].
- [Karpathy, Software Is Changing (Again)](../sources/software-is-changing-again.md) — shifts the emphasis from "agentic models" to **[[partial-autonomy-apps|partial-autonomy apps]] wrapping agentic models**. The model is the engine; the product is the loop with a human verifier. The [[autonomy-slider]] controls how much rope the agent gets.
- [Karpathy, Summoning Ghosts](../sources/summoning-ghosts-not-animals.md) — sobering: today's agents are impressive demos that collapse under real work. Missing pieces: continual learning, persistent memory, robust multimodality, reliable computer-use. The honest timeline is the [[decade-of-agents]], not the year of agents.

## Key properties (consolidated)

- **Long-horizon action.** Measured in hours of autonomous work, not seconds.
- **Tool use.** Terminal, code execution, filesystem, browser, MCP-exposed services.
- **Trained with [[reinforcement-learning]] on [[verifiable-rewards]].** The mechanism behind the current capability jump, but [[rl-is-terrible|RL is terrible]] and the gains are hitting the [[march-of-nines]] wall.
- **[[people-spirits|People-spirit]] psychology.** Hallucinations, [[jagged-intelligence]], anterograde amnesia, prompt-injection vulnerability — agent loops amplify all of these unless the UI surfaces them.

## Product shape

- Don't ship raw agent demos. Ship [[partial-autonomy-apps]] with a GUI that makes verification fast and an [[autonomy-slider]] that defaults low.
- Wrap the agent with a concrete, narrow task surface ([[cursor|Cursor]] on code, [[perplexity|Perplexity]] on research).
- Prefer the [[iron-man-analogy|Iron Man suit over the Iron Man robot]] — augmentation over automation, for this decade at least.

## Related

- [[peaky-capability]] — why agentic models shine in programming but not in advice/writing
- [[partial-autonomy-apps]] — the product shape that turns agents into revenue
- [[autonomy-slider]] — the UX mechanic
- [[march-of-nines]] — why agent reliability is a decade-long grind
- [[decade-of-agents]] — Karpathy's timeline
