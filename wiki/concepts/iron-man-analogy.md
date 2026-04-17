---
title: Iron Man Analogy
type: concept
created: 2026-04-17
updated: 2026-04-17
sources: [andrej-karpathy-software-is-changing-again/transcript.md]
tags: [product, agents, karpathy-coinage]
---

# Iron Man Analogy

Karpathy's product north star for the LLM era: **build suits, not robots.** Iron Man is a human augmented by machine; the Iron Man drones in the same films are fully autonomous and much less interesting to build *right now*.

## Source

[Karpathy, Software Is Changing (Again)](../sources/software-is-changing-again.md) — the talk's most quotable image.

## The claim

- Agents at current reliability want a pilot in the loop.
- The best product surface lets the user dial autonomy up or down per task (see [[autonomy-slider]]).
- "Suit" means the human keeps situational awareness; the machine amplifies what the human already decides. "Robot" means the machine decides on its own.

## Why suits beat robots in the 2020s

1. [[jagged-intelligence|Jagged intelligence]] — models fail in ways a human can catch but the model can't.
2. [[march-of-nines|March of nines]] — full autonomy requires reliability we don't yet have.
3. [[partial-autonomy-apps]] have fast feedback loops (diff accepted/rejected, citation clicked) that generate training signal.
4. Trust transfers per interaction, not per deployment — people ratchet up autonomy as they see it work.

## Design consequences

- Default the [[autonomy-slider]] low.
- Show the work (diffs, citations, traces).
- Let the pilot override cheaply.
- Fail gracefully from level N to level N-1, not from N to zero.

## Related

- [[partial-autonomy-apps]]
- [[autonomy-slider]]
- [[march-of-nines]]
- [[cursor]], [[perplexity]] — canonical suits
