---
title: Overview
type: overview
created: 2026-04-15
updated: 2026-04-17
sources: [4.10.md, andrej-karpathy-software-is-changing-again/transcript.md, andrej-karpathy-were-summoning-ghosts-not-building-animals/transcript.md, andrej-karpathy-berkeley-ai-hackathon-2024-keynote/transcript.md, andrej-karpathy-gpu-mode-irl-2024-keynote/transcript.md]
tags: [overview, karpathy, llm, agents, software-3-0]
---

# karpathy-wiki — Overview

> Top-level synthesis of the entire knowledge base.
> Revised as sources are ingested and understanding deepens.

## Scope

A research wiki built from Andrej Karpathy's X posts, talks, and interviews, covering the LLM era's pedagogy, product shape, reliability arc, and engineering substrate.

## Current State

**5 sources ingested** spanning October 2024 → October 2025:

1. **GPU MODE IRL 2024** (Oct 2024) — systems/CUDA talk; [[llm-c|llm.c]] origin story.
2. **Berkeley SkyDeck Hackathon keynote** (July 2024 recording, released later) — student pitch, career advice, "[[feel-the-agi]]".
3. **April 10 X post** (April 2025) — [[peaky-capability]] and [[ai-psychosis]].
4. **YC AI Startup School keynote** — *Software Is Changing (Again)* (June 2025) — [[software-3-0]], [[llm-os]], [[partial-autonomy-apps]], [[vibe-coding]].
5. **Dwarkesh Patel interview** — *We're Summoning Ghosts, Not Building Animals* (Oct 2025) — [[animals-vs-ghosts]], [[march-of-nines]], [[cognitive-core]], [[rl-is-terrible|RL is terrible]].

Together they span three registers: **pedagogy** (Berkeley, GPU MODE), **product vision** (YC), and **research posture** (Dwarkesh), with the X post as a datapoint snapshot in between.

## Central Claims Across the Corpus

### 1. This is the Software 3.0 era — and the pitch to engineers changes

[[software-3-0|Software 3.0]] reframes programming itself: English prompts are the new source code, the LLM is the new runtime. This isn't metaphor — Karpathy pairs it with a three-way analogy for the LLM industry (utility / fab / OS) and with the [[llm-os]] thesis that we're "in the 1960s/1980s of LLM computing."

### 2. Agents are a decade away — and that's the bullish case

[[march-of-nines]] + [[decade-of-agents]] frame Karpathy's posture: the demos are 90% of the way, and the remaining 9%, 0.9%, 0.09% each cost as much as the prior one. Self-driving is the empirical prior ([[waymo]] 2013→2025; [[tesla]] Autopilot 12+ years and counting). The same curve is coming for coding agents.

### 3. Products should be [[partial-autonomy-apps]], not full-autonomy ones

[[iron-man-analogy|Build suits, not robots.]] Put an [[autonomy-slider]] on every product; default it low; make human verification fast. [[cursor|Cursor]] and [[perplexity|Perplexity]] are the canonical examples. The [[ai-capability-gap|capability gap]] users perceive is partly a product-surface failure to expose [[jagged-intelligence]].

### 4. LLMs are [[people-spirits|people spirits]], not animals

[[animals-vs-ghosts|Animals vs Ghosts]] is the frame: we aren't recreating biological intelligence; we're summoning a new thing shaped like people because it was trained on people. That explains [[llm-cognitive-deficits|the specific deficits]] — no persistent memory, [[ai-psychosis|psychosis]] under long runs, [[model-collapse|collapse]] under self-consumption, [[jagged-intelligence|jagged]] task-level performance.

### 5. Capability is peaky; [[verifiable-rewards|verifiable rewards]] are the reason

The April X post's thesis — that [[peaky-capability|frontier capability spikes in RL-tractable domains]] — is consistent with and reinforced by the Dwarkesh interview's critique of "[[rl-is-terrible|RL is terrible]]." Gains are concentrated where the reward signal is clean; the rest of the skills suffer the "sucking supervision through a straw" problem.

### 6. The right model is a [[cognitive-core]], not a trivia monster

Karpathy's research bet: the next useful scaling move is **downward** — distilling a small reasoning-and-language core, pairing it with retrieval and tools. Memorization migrates to context; reasoning stays in weights.

### 7. Infrastructure must now be [[build-for-agents|built for agents]]

The other half of the [[vibe-coding]] story: code generation is easy; production plumbing (Apple IDs, OAuth, Stripe, DNS — the [[menugen|MenuGen]] anecdote) is the bottleneck. `lm.txt`, [[model-context-protocol|MCP]], repo-flatteners like gitingest are early moves in a whole new category.

### 8. Pedagogy is a [[ramps-to-knowledge|ramp]], not a cliff

Karpathy's teaching stack — [[cs231n]], [[zero-to-hero]], [[micrograd]], [[nanogpt]], [[llm-c]], [[nanochat]] — is engineered as graded climbs. The [[10000-hours]] rule still holds; the per-hour productivity rises with better ramps and LLM tools. [[snowballs|Snowball projects]] compound the hours into reputation and depth.

## Open Questions

- Is the ["feel the AGI"](concepts/feel-the-agi.md) / "[[agi-blends-into-2-percent-growth|AGI blends into 2% growth]]" pair a stable view, or does Karpathy slide along it from talk to talk?
- Which adjacent domain gets the [[verifiable-rewards|verifiable-rewards]] treatment next — theorem proving, systems work, scientific computation?
- Does [[cognitive-core]] materialize on the open-weights side first ([[deepseek-v3-2|DeepSeek]], [[llama|LLaMA]] family) or frontier labs first?
- How does [[eureka|Eureka]]'s delivery — starting with [[llm101n]] — reshape Karpathy's influence now that he's out of a frontier lab?
- The "1960s" (YC 2025) vs "1980s" (Berkeley 2024) [[llm-os]] dating: a rhetorical slide, or does Karpathy genuinely think the field regressed in his reckoning?

## Navigating the Wiki

- **Entry point for newcomers:** `entities/andrej-karpathy.md` — career arc and a table of every Karpathy coinage in the corpus.
- **By theme:**
  - *Product mechanics* → [[partial-autonomy-apps]], [[autonomy-slider]], [[iron-man-analogy]].
  - *Reliability arc* → [[march-of-nines]], [[decade-of-agents]], [[tesla-autopilot]], [[waymo]].
  - *LLM psychology* → [[people-spirits]], [[animals-vs-ghosts]], [[jagged-intelligence]], [[llm-cognitive-deficits]].
  - *Research direction* → [[cognitive-core]], [[rl-is-terrible]], [[model-collapse]], [[in-context-learning]].
  - *Pedagogy* → [[ramps-to-knowledge]], [[zero-to-hero]], [[10000-hours]], [[snowballs]].
- **By source:** `wiki/sources/*.md` — each source summary links out to every page it touches.
