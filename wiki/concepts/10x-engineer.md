---
title: 10x Engineer (in the Agent Era)
type: concept
created: 2026-04-17
updated: 2026-04-17
sources: [2026/1.27.md, 2026/2.5.md, 2026/3.11.md]
tags: [productivity, agents, karpathy]
---

# 10x Engineer (in the Agent Era)

Karpathy's update on the old industry trope: in the [[agentic-engineering]] era, a "10× engineer" is not someone who types faster, but someone who **runs a supervised swarm of agents and catches their mistakes** before they hit main.

## The shape of the 10x workflow

From Jan 27 (Claude coding reflections) and Mar 11 (command-center IDE):

1. **Orchestrate.** Several agents in parallel — implementation, tests, review, benchmarks.
2. **Supervise.** Human eye on diffs, not keystrokes; [[atrophy|discrimination beats generation]].
3. **Compose with [[claws]].** Patterns — "implement, then critique, then patch, then benchmark" — as reusable recipes.
4. **Use [[bacterial-code|bacterial code]].** Keep modules small so agents can lift and repair them cleanly.
5. **Own the context.** [[byoai|BYOAI]] + [[llm-knowledge-bases|personal KB]]: the engineer carries their own editable memory across providers.

## What's new vs the old trope

| Old 10×-er | Agent-era 10×-er |
|-----------|------------------|
| Types fast, keeps more in head | Composes and reviews agent output |
| Leverages good abstractions | Leverages good *prompts*, skills, claws |
| Bottleneck: attention + typing | Bottleneck: review throughput |
| Scales linearly with hours | Scales with how many agents they can supervise before quality falls |

## The caution

Karpathy is explicit that review throughput — not agent throughput — is the hard ceiling. The 10× gains collapse into a regression factory the moment supervision slips. See [[atrophy]] and [[slopacolypse]].

## Related

- [[agentic-engineering]]
- [[claws]]
- [[atrophy]]
- [[bacterial-code]]
- [[vibe-coding]]
- [[byoai]]
