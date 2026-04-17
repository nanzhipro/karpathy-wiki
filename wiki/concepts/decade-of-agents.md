---
title: Decade of Agents
type: concept
created: 2026-04-17
updated: 2026-04-17
sources: [andrej-karpathy-were-summoning-ghosts-not-building-animals/transcript.md, andrej-karpathy-software-is-changing-again/transcript.md]
tags: [agents, timelines, karpathy-coinage]
---

# Decade of Agents

Karpathy's deliberate reframing of the industry's "year of agents" slogan. His prediction: useful agents will arrive, but the work from demo to deployment is a **ten-year program**, not a twelve-month sprint.

## Sources

- [Karpathy, Summoning Ghosts](../sources/summoning-ghosts-not-animals.md) — the canonical statement. Grounded in the [[waymo|Waymo]] arc (2013 demo → 2025 commercial) and applied directly to coding agents.
- [Karpathy, Software Is Changing (Again)](../sources/software-is-changing-again.md) — the YC framing: today's agents are early, the [[autonomy-slider]] is needed precisely because full autonomy is a decade out.

## The argument

1. **Demos ≠ products.** An agent that completes a task 80% of the time is a demo. A deployable agent needs many more nines (see [[march-of-nines]]).
2. **Each nine is a separate project.** 90% → 99% isn't 10× the work; it's a different class of failure modes requiring different instrumentation.
3. **Self-driving is the empirical prior.** The first [[waymo|Waymo]] demo ride was flawless in 2013. Full commercial service took until 2025. Coding agents are at the 2013-Waymo stage.

## Product implications

- Bet on [[partial-autonomy-apps]] over full-autonomy ones for this decade.
- Default the [[autonomy-slider]] low.
- Plan for a long tail of edge cases, not a hockey-stick reliability curve.

## Related

- [[march-of-nines]]
- [[partial-autonomy-apps]]
- [[autonomy-slider]]
- [[waymo]], [[tesla]]
