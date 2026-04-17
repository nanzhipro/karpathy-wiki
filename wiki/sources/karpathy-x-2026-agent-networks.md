---
title: "2026-02-04 — Networks of LLM Agents"
type: source-summary
created: 2026-04-17
updated: 2026-04-17
sources: [2026/2.4.md, 2026/2.13.md]
tags: [agent-networks, security, simulation, karpathy]
---

# 2026-02 — Large-Scale Agent Networks + Population Simulation

Two posts addressing what happens when LLM agents are wired together in loops.

## Sources

- **Feb 4** — Commentary on a public "[site everyone heard too much about today] (moltbook)" where **150,000 LLM agents share a global scratchpad.**
- **Feb 13** — Angel-investment note on [[simile-ai|Simile]]: *"Why simulate one person when you could simulate a population?"*

## The Moltbook phenomenon (Feb 4)

Karpathy acknowledges the site is a "dumpster fire" (spam, scams, slop, crypto grifters, prompt-injection wild west) but defends the principle:

> "We have never seen this many LLM agents (150,000 atm!) wired up via a global, persistent, agent-first scratchpad. Each of these agents is fairly individually quite capable now, they have their own unique context, data, knowledge, tools, instructions, and the network of all that at this scale is simply unprecedented."

### Phenomena he predicts from such networks

- **Viruses of text** that spread across agents
- **Gain-of-function jailbreaks**
- **Weird attractor states**
- **Botnet-like correlated activity**
- **Psychosis — agent-and-human co-morbid** (see [[ai-psychosis]])
- **Second-order effects very hard to anticipate**

> "I don't really know that we are getting a coordinated 'skynet' (though it clearly type checks as early stages of a lot of AI takeoff scifi, the toddler version), but certainly what we are getting is a complete mess of a computer security nightmare at scale."

### The point-vs-slope idea he keeps returning to

> "The majority of the ruff ruff is people who look at the current point and people who look at the current slope." (from the Jan 7 post, referenced here)

This is his shorthand for *why* debates about what LLMs can do right now go in circles: one side measures performance today, the other measures rate of change.

## Simile — population simulators (Feb 13)

The interesting under-explored dimension of LLMs:

> "Usually, the LLMs you talk to have a single, specific, crafted personality. But in principle, the native, primordial form of a pretrained LLM is that it is a simulation engine trained over the text of a highly diverse population of people on the internet. Why not lean into that statistical power: Why simulate one 'person' when you could try to simulate a population?"

Karpathy's angel investment is small; he flags the research questions:

- How do you build such a simulator?
- How do you manage its entropy?
- How faithful is it?
- What emergent properties arise in loops of similes?

## Why these two posts belong together

Both push on the **beyond-single-agent** question. The Feb 4 post asks what happens when independent agents share a persistent scratchpad; the Feb 13 post asks what happens when a single LLM is deliberately invited to act as many personas at once. Same underlying phenomenon — LLMs as an **ensemble of minds**, not a single mind.

## Related

- [[ai-psychosis]]
- [[people-spirits]]
- [[simile-ai]]
- [[intelligence-brownouts]]
- [[agentic-engineering]]
