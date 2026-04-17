---
title: "2026-02 — Agentic Engineering: Naming the Successor to Vibe Coding"
type: source-summary
created: 2026-04-17
updated: 2026-04-17
sources: [2026/2.5.md, 2026/2.25.md]
tags: [agentic-engineering, vibe-coding, karpathy-coinage]
---

# 2026-02 — Agentic Engineering

Two posts that together make the case for a successor term to [[vibe-coding]] and date the "phase shift" precisely.

## Sources

- **Feb 5** — 1-year retrospective on the original vibe-coding tweet. Introduces **"agentic engineering"**.
- **Feb 25** — *"Programming has changed due to AI in the last 2 months"*. Concrete workflow example; dates the threshold to **December 2025**.

## The naming argument (Feb 5)

Karpathy concedes that "vibe coding" names a specific moment — fun, throwaway, imperfect — and proposes a term for the next:

> "Many people have tried to come up with a better name… personally my current favorite **agentic engineering**:
> - *'agentic'* because the new default is that you are not writing the code directly 99% of the time, you are orchestrating agents who do and acting as oversight.
> - *'engineering'* to emphasize that there is an art & science and expertise to it."

## The phase-shift claim (Feb 25)

> "It is hard to communicate how much programming has changed due to AI in the last 2 months: not gradually and over time in the 'progress as usual' way, but specifically this last December. There are a number of asterisks but imo coding agents basically didn't work before December and basically work since."

### The DGX Spark example

He gives an agent a local IP + username/password and this prompt:

> "Log in, set up ssh keys, set up vLLM, download and bench Qwen3-VL, set up a server endpoint to inference videos, a basic web ui dashboard, test everything, set it up with systemd, record memory notes for yourself and write up a markdown report for me."

The agent runs for ~30 minutes, debugs multiple issues, deploys, writes the report. **"All of this could easily have been a weekend project just 3 months ago but today it's something you kick off and forget about for 30 minutes."**

## The new programming surface

> "You're not typing computer code into an editor like the way things were since computers were invented, that era is over. You're spinning up AI agents, giving them tasks *in English* and managing and reviewing their work in parallel."

Karpathy's preferred abstraction escalator: **long-running orchestrator "[[claws|Claws]]"** that manage multiple parallel Code instances with the right tools, memory, and instructions.

## Pushback he anticipates

- **"Prompters" is a misunderstanding.** Deep technical expertise becomes *even more* of a multiplier at the top tier, because of the added leverage.
- **Not magic, delegation.** "In this intermediate state, you go faster if you can be more explicit and actually understand what the AI is doing on your behalf."
- **"You're holding it wrong."** To UI complaints: `chrome` extensions exist; network/UI legibility is a solvable design problem; "every action is error" (a Tesla saying).

## Related

- [[agentic-engineering]]
- [[vibe-coding]]
- [[claude-code]], [[openai-codex]]
- [[claws]]
- [[build-for-agents]]
