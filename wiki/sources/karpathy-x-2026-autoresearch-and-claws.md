---
title: "2026-02 / 03 — Autoresearch + Claws: The Layer Above Coding Agents"
type: source-summary
created: 2026-04-17
updated: 2026-04-17
sources: [2026/2.26.md, 2026/2.28.md, 2026/3.6.md, 2026/3.8.md, 2026/3.9.md, 2026/3.10.md, 2026/3.11.md, 2026/3.12.md, 2026/3.20.md]
tags: [autoresearch, claws, agent-orgs, karpathy]
---

# 2026-02 / 03 — Autoresearch & Claws

Nine posts form a coherent narrative across five weeks: Karpathy builds **research-agent swarms** that autonomously improve nanochat, discovers the **"Claw" layer** above plain coding agents, and starts arguing that **the IDE is not dead, it's bigger.**

## The autoresearch arc

### Feb 26 — 8 agents on nanochat (first attempts)

Sets up 8 agents (4 [[claude-code|Claude]], 4 [[openai-codex|Codex]]), one GPU each, trying to delete logit softcap. It doesn't work. Why:

- Agents' **ideas are bad out of the box**. They run "non-sensical variations," skip strong baselines, don't ablate properly, don't control for runtime/FLOPs.
- Concrete failure: an agent "discovered" that increasing hidden size improves validation loss — spurious, because a bigger network trained longer has lower loss in the infinite-data regime.
- Strength: **very good at implementing well-scoped ideas; bad at creatively generating them.**

> "But the goal is that you are now programming an organization (e.g. a 'research org') and its individual agents, so the 'source code' is the collection of prompts, skills, tools, etc. and processes that make it up."

### Feb 28 — Nanochat 2h + AI agents iterating overnight

- Nanochat now trains GPT-2-grade in 2h on 8×H100 (dataset switch: FineWeb-edu → NVIDIA ClimbMix).
- **110 autonomous changes in ~12 h**, validation loss 0.862415 → 0.858039 on a d12 model. Zero wall-clock cost to Karpathy.
- The new benchmark he cares about:

> "What is the research org agent code that produces improvements on nanochat the fastest? This is the new meta."

### Mar 8 — Autoresearch released

Packages the recipe into [[autoresearch|autoresearch]] — a minimal single-GPU, one-file version of nanochat training (~630 LoC) designed for overnight tuning. Repo: `github.com/karpathy/autoresearch`.

> "Part code, part sci-fi, and a pinch of psychosis :)"

### Mar 9 — SETI@home for research

Vision: asynchronous, massively collaborative agent research.

- Git/GitHub are *almost* but not really suited — they assume one master branch.
- PRs you'd never want to merge (just "adopt") point at the mismatch.
- Proposes lightweight Discussions + PRs as the interim collaboration surface.

> "Agents can in principle easily juggle and collaborate on thousands of commits across arbitrary branch structures. Existing abstractions will accumulate stress as intelligence, attention and tenacity cease to be bottlenecks."

### Mar 10 — Round 1 results: 2.02h → 1.80h (~11% improvement)

Real, stackable, transferable wins from a **naive first attempt**:

- Parameterless QKnorm needed a scaler multiplier (attention was too diffuse).
- Value embeddings needed regularization.
- Banded attention was too conservative.
- AdamW betas misconfigured.
- Weight-decay schedule mistuned.
- Network initialization mistuned.

> "All LLM frontier labs will do this. It's the final boss battle. It's a lot more complex at scale of course — you don't just have a single train.py file to tune. But doing it is 'just engineering' and it's going to work."

Generalizes: **any metric you can efficiently evaluate** (or proxy through smaller models) is amenable to this treatment.

### Mar 11 — Agent Command Center IDE

> "tmux grids are awesome, but I feel a need to have a proper 'agent command center' IDE for teams of them — toggle, see who's idle, pop open related tools, stats, etc."

### Mar 20 — "Bigger IDE," not "no IDE"

Sparked by an oauth outage wiping his autoresearch labs:

> "Expectation: the age of the IDE is over. Reality: we're going to need a bigger IDE."

- Humans program at a higher level: **the basic unit is one agent, not one file.**
- Agentic orgs will be **forkable** (classical orgs like Microsoft are not).
- CEOs can't see into their companies in real time; agentic orgs could be "legible" — with implications for mobile/voice oversight.

Also introduces: **[[intelligence-brownouts]]** — "the planet losing IQ points when frontier AI stutters."

## The Claws arc (Mar 6, Mar 12)

### Mar 6 — "Claws" as the new layer

> "Just like LLM agents were a new layer on top of LLMs, Claws are now a new layer on top of LLM agents, taking the orchestration, scheduling, context, tool calls and a kind of persistence to a next level."

- Skeptical of running OpenClaw ("400K lines of vibe-coded monster being actively attacked at scale").
- Likes [[nanoclaw]] — "~4000 lines of code, fits in both my head and that of AI agents, runs everything in containers by default."
- **Novel design idea: config *via skills*, not config files.** `/add-telegram` is a skill that instructs the agent to modify the repo code to integrate Telegram. "The implied new meta is to write the most maximally forkable repo and then have skills that fork it into any desired more exotic configuration."

> "First there was chat, then there was code, now there is claw. Ez"

### Mar 12 — "Dobby the House Elf"

NVIDIA sends him a DGX system ("requires 20 amps"). The teaser: his home-automation Claw **"Dobby" runs his entire house over WhatsApp** — lights, shades, pool/spa, Sonos, security, HVAC. One of four unfinished blog posts.

Also references **NVIDIA GTC 2015** — when Jensen cited Karpathy's image-captioning PhD thesis to an audience of gamers as "Deep Learning is The Next Big Thing." (Context for the long relationship.)

## Why these nine posts belong together

They all push on the same abstraction move: **the unit of work is no longer one task, it's one team.** Karpathy is building the tooling, proving the results (real 11% speedup), naming the layer (Claws), and noting where existing infrastructure (Git, IDEs) buckles under the new load.

## Related

- [[autoresearch]]
- [[claws]]
- [[nanoclaw]]
- [[org-code]]
- [[intelligence-brownouts]]
- [[nanochat]]
- [[claude-code]], [[openai-codex]]
- [[agentic-engineering]]
