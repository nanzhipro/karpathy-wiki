---
title: Agentic Engineering
type: concept
created: 2026-04-17
updated: 2026-04-17
sources: [2026/2.5.md, 2026/2.25.md, 2026/1.27.md]
tags: [coding, software-3-0, karpathy-coinage]
---

# Agentic Engineering

Karpathy's proposed successor term to [[vibe-coding]], introduced on the 1-year anniversary of the original coinage (Feb 5 2026). Where **vibe coding** was fun, throwaway, and imperfect, **agentic engineering** is the professional discipline of orchestrating coding agents for work that ships.

## Definition

> "**Agentic** because the new default is that you are not writing the code directly 99% of the time, you are orchestrating agents who do and acting as oversight. **Engineering** to emphasize that there is an art & science and expertise to it. It's something you can learn and become better at, with its own depth of a different kind."

— Karpathy, Feb 5 2026

## The dating of the shift

Karpathy is unusually precise. From the Feb 25 post:

> "Programming has changed due to AI in the last 2 months: not gradually and over time in the 'progress as usual' way, but specifically this last December. There are a number of asterisks but imo coding agents basically didn't work before December and basically work since."

**The threshold:** **~December 2025.** His Jan 27 post had already reported a 80/20 → 20/80 flip (manual/agent → agent/manual) in his own daily work over ~4 weeks.

## Core practices

From the Jan 27 "Claude coding notes":

- **Give success criteria, not step-by-step instructions.** Let the agent loop.
- **Tests first, then pass them.** Tight verification loop.
- **Naive correct → ask for optimization while preserving correctness.**
- **Declarative over imperative.** Longer agent loops, higher leverage.
- **Run multiple concurrent agents**; Karpathy's setup is "a small few Claude Code sessions on the left in ghostty windows/tabs and an IDE on the right for viewing code + manual edits."

## What agents still can't do (per Karpathy, Jan 27)

- Manage their own confusion — don't seek clarifications or surface inconsistencies.
- Don't present tradeoffs or push back.
- Too sycophantic.
- Make subtle conceptual errors resembling "a slightly sloppy, hasty junior dev."
- Bloat abstractions, over-engineer, don't clean up dead code.
- Sometimes silently change or remove orthogonal code they "don't like."

## Relation to other layers

- **Below:** the underlying LLM; **above:** [[claws]] that orchestrate multiple agents and persist state.
- **Adjacent:** [[autoresearch|autoresearch-style]] agent swarms, where the task is research rather than product work.

## Agentic engineering as a new kind of expertise

Karpathy pushes back on the "prompters" dismissal:

> "'Prompters' is doing it a disservice and is imo a misunderstanding. Vibe coders are now able to get somewhere, but at the top tiers, deep technical expertise may be *even more* of a multiplier than before because of the added leverage."

And on the "it's just delegation" point:

> "In this intermediate state, you go faster if you can be more explicit and actually understand what the AI is doing on your behalf, and what the different tools are at its disposal, and what is hard and what is easy. It's not magic, it's delegation."

## Related

- [[vibe-coding]] — the predecessor
- [[claude-code]], [[openai-codex]]
- [[claws]]
- [[autoresearch]]
- [[atrophy]] — the accompanying cost
- [[org-code]]
