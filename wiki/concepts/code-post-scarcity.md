---
title: Code Post-Scarcity
type: concept
created: 2026-04-18
updated: 2026-04-18
sources: [2025/10.27.md]
tags: [coding, agentic-engineering, karpathy-coinage]
---

# Code Post-Scarcity

The state in which writing code is no longer expensive, so code itself is no longer a precious artifact. Karpathy's [[karpathy-x-2025-ai-assisted-coding|Oct 27 2025]] coinage.

## The observation

> "**It's the code post-scarcity era** — you can just create and then delete thousands of lines of super custom, super ephemeral code now, it's ok, it's not this precious costly thing anymore."

Concrete example in the same post: [[claude-code|Claude Code]] can hammer out 1,000 lines of one-off extensive visualization/debugging code just to identify a specific bug, which gets all deleted right after you find it.

## The economic shift

| Era | Code economics |
|---|---|
| Pre-LLM | Expensive to write → kept, reused, abstracted, maintained |
| Post-LLM | Cheap to write → written, used once, thrown away |

The old intuitions around "don't duplicate, write helpers, abstract early" partially invert in the throwaway regime.

## Second-order effects

- **Ephemeral apps.** [[app-store-outdated]] (Feb 2026) generalizes this to whole applications: agent-built, task-specific, discarded after use.
- **Exploratory visualizations normalize.** Previously you'd eyeball a data issue because building a dashboard cost hours; now you ask for the dashboard.
- **Code review pressure flips** — the real cost isn't writing, it's [[verification-gap|verifying]].
- **[[bacterial-code|Bacterial-code]] sensibility wins** — rippable, dependency-free code is cheap to generate *and* cheap to throw away.
- **Repo hygiene under strain** — if one-offs get committed instead of deleted, repos bloat. Karpathy's actual practice is aggressive deletion.

## What it does NOT imply

- Code **quality** is less important — [[atrophy|review]] is still load-bearing, arguably more so.
- Libraries are obsolete — dependency-free inlining is a *choice* made easier, not a mandate.
- Engineering skill is obsolete — taste, architecture, and verification ability now concentrate the value.

## Relation to other concepts

- **[[bacterial-code]]** — the style that fits a post-scarcity regime.
- **[[app-store-outdated]]** — the app-level version of the same economics.
- **[[verification-gap]]** — the bottleneck that remains scarce.
- **[[atrophy]]** — the risk in a post-scarcity regime: skills fade when code is always cheap.
- **[[agentic-engineering]]** — the named practice that operates inside the post-scarcity regime.

## Related

- [[bacterial-code]]
- [[app-store-outdated]]
- [[verification-gap]]
- [[atrophy]]
- [[vibe-coding]]
- [[claude-code]]
