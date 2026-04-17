---
title: Cognitive Core
type: concept
created: 2026-04-17
updated: 2026-04-17
sources: [andrej-karpathy-were-summoning-ghosts-not-building-animals/transcript.md]
tags: [llm-architecture, agents, karpathy-coinage]
---

# Cognitive Core

Karpathy's proposed target for the "right" model size: a small, distilled model that has the **reasoning, language, and meta-cognitive ability** of a large model but strips out rote memorization of facts. Pair it with retrieval and tools and you get a better agent than a giant frozen LLM.

## Source

[Karpathy, Summoning Ghosts](../sources/summoning-ghosts-not-animals.md) — Karpathy's framing of what comes after the scaling plateau.

## The argument

Today's frontier models are bloated with memorized trivia they don't need to *have* — they need to *find*. A cognitive core is:

- **Thinking** — multi-step reasoning, planning, self-correction.
- **Language** — fluent generation and comprehension.
- **Meta-cognition** — knowing what it doesn't know, when to search, when to call a tool.
- **Minimal memorization** — just enough world model to navigate, not a textbook per domain.

Size estimate (Karpathy's guess): **low billions of parameters**, not trillions. Everything else comes from tools, retrieval, and context.

## Why it's attractive

- Cheaper inference → more iteration → faster [[march-of-nines]] progress.
- Less [[model-collapse|collapse]] risk during post-training because the substrate is leaner.
- Better generalization: a core that *reasons* transfers; a core that *memorizes* doesn't.
- Plays to the [[llm-os]] frame: the model is the CPU, not the disk.

## What would enable it

- Better distillation recipes from frontier models.
- Robust retrieval and tool-use scaffolding (think: [[build-for-agents|agent-native infrastructure]]).
- Evaluations that separate reasoning from memorization.

## Related

- [[llm-os]] — cognitive core is the OS's CPU
- [[people-spirits]]
- [[animals-vs-ghosts]]
- [[march-of-nines]]
