---
title: Overview
type: overview
created: 2026-04-15
updated: 2026-04-17
sources: [Andrej Karpathy.md, 4.10.md, andrej-karpathy-software-is-changing-again/transcript.md, andrej-karpathy-were-summoning-ghosts-not-building-animals/transcript.md, andrej-karpathy-berkeley-ai-hackathon-2024-keynote/transcript.md, andrej-karpathy-gpu-mode-irl-2024-keynote/transcript.md, 2026/1.1.md, 2026/1.8.md, 2026/1.27.md, 2026/2.5.md, 2026/2.12.md, 2026/2.20.md, 2026/3.6.md, 2026/3.8.md, 2026/3.19.md, 2026/4.3.md, 2026/4.5.md]
tags: [overview, karpathy, llm, agents, software-3-0, agentic-engineering]
---

# karpathy-wiki — Overview

> Top-level synthesis of the entire knowledge base.
> Revised as sources are ingested and understanding deepens.

## Scope

A research wiki built from Andrej Karpathy's self-bio, X posts (2024–2026), talks, and interviews, covering the LLM era's pedagogy, product shape, reliability arc, engineering substrate, and — with the 2026 corpus — the emerging practice of **agentic engineering**.

## Current State

**~15 sources ingested** spanning October 2024 → April 2026:

**Foundational (2024–2025):**
1. **GPU MODE IRL 2024** (Oct 2024) — systems / CUDA talk; [[llm-c|llm.c]] origin story.
2. **Berkeley SkyDeck Hackathon keynote** (2024) — "[[feel-the-agi]]", [[snowballs]], [[10000-hours]].
3. **April 10 2025 X post** — [[peaky-capability]], [[ai-psychosis]].
4. **YC AI Startup School keynote** (*Software Is Changing Again*, June 2025) — [[software-3-0]], [[llm-os]], [[partial-autonomy-apps]], [[vibe-coding]].
5. **Dwarkesh Patel interview** (Oct 2025) — [[animals-vs-ghosts]], [[march-of-nines]], [[cognitive-core]], [[rl-is-terrible]].
6. **karpathy.ai self-bio** — verified career timeline 2005–2024.

**2026 X-post corpus (10 thematic bundles):**
7. **Jan 1 — FSD coast-to-coast** (2,732 mi, zero interventions).
8. **Jan 8 / 29, Feb 2 — nanochat GPT-2 reproduction** ($20 on 8×H100).
9. **Jan 27 — Claude coding reflections** ([[agentic-engineering]], [[atrophy]]).
10. **Feb 5 / 25 — agentic engineering naming + phase-shift note**.
11. **Feb 12 / 17 / 20 / 21 — malleable software** ([[bacterial-code]], [[microgpt]], [[app-store-outdated]]).
12. **Feb 4 / 13 — agent networks** ([[simile-ai]], [[org-code]]).
13. **Feb 26 → Mar 20 — autoresearch + Claws + command-center IDE**.
14. **Mar 19 + Mar 31 — supply-chain attacks** (litellm, axios).
15. **Apr 3 / 5 — LLM knowledge bases + [[byoai|BYOAI]]**.
16. **Misc.** — point-vs-slope, memory overfit, "argue the opposite."

## Central Claims Across the Corpus

### 1. Software 3.0 is now **agentic engineering**

The 2025 frame ([[software-3-0]]) evolves in 2026 into a named practice: [[agentic-engineering]]. LLMs are not just the new runtime — they are the new *collaborators*. The bottleneck shifts from *writing* code to *reviewing* what agents wrote ([[atrophy]], [[10x-engineer]]).

### 2. The decade of agents has started — but the ceiling is human review

[[decade-of-agents]] + [[march-of-nines]] still hold. **Jan 1 2026's Tesla FSD coast-to-coast** (zero interventions) is the first clean cash-out of the march-of-nines framing. Coding agents sit somewhere earlier on the same curve — see [[claws]], [[autoresearch]], [[atrophy]].

### 3. Build **partial-autonomy apps** with an [[autonomy-slider]]

[[iron-man-analogy|Suits, not robots.]] [[cursor|Cursor]], [[perplexity|Perplexity]], [[claude-code|Claude Code]], [[openai-codex|Codex]] converge on the same shape. By 2026, Karpathy generalizes: entire *application categories* collapse into [[app-store-outdated|ephemeral agent-built apps]].

### 4. LLMs are [[people-spirits|people spirits]], not animals

[[animals-vs-ghosts]] remains the psychological frame. Their [[llm-cognitive-deficits|deficits]] — no persistent memory, [[ai-psychosis|psychosis]] under long runs, [[model-collapse|collapse]] under self-consumption — are explicit constraints on product design and [[byoai|personalization strategy]].

### 5. Capability is peaky; [[verifiable-rewards]] concentrate the spikes

[[peaky-capability]] + [[rl-is-terrible|"RL is terrible"]] are two views of one fact: gains concentrate where rewards are clean. 2026's [[autoresearch]] is an attempt to make **ML research itself** one of those domains.

### 6. The right model is a [[cognitive-core]]

Small reasoning core, retrieval, tools. 2026 adds nuance: the cognitive core should live *on your side of the network* — locally runnable, [[byoai|swappable across providers]], resistant to [[intelligence-brownouts]].

### 7. Products and code must be [[build-for-agents|built for agents]]

2026 reinforces: products need CLI / API / MCP, docs in markdown, Skills; code should be [[bacterial-code|bacterial]] (small, dependency-free, rippable). The cost/benefit of `pip install` has flipped after the 2026 [[supply-chain-attacks|supply-chain attacks]].

### 8. Pedagogy is a [[ramps-to-knowledge|ramp]], and the ramp now runs through the wiki

Karpathy's stack — [[cs231n]], [[zero-to-hero]], [[micrograd]], [[nanogpt]], [[microgpt]], [[llm-c]], [[nanochat]] — is graded climbs. 2026's meta-move: the *knowledge base itself* is a ramp (see [[llm-knowledge-bases]]) and the wiki you are reading is an instance.

### 9. The Dec 2025 phase shift

Feb 25 2026 explicitly marks a qualitative transition: "something shifted in December 2025." Frontier agentic coding crossed a threshold — long-horizon coherence, autonomous dev loops, review-as-bottleneck became real. Multiple later posts cite this inflection.

## Open Questions

- Does [[byoai]] stay a hobbyist stance, or become the default for serious research workflows?
- Does [[autoresearch]] become a public "SETI@home for ML" or stay single-operator?
- How do [[claws]] and [[model-context-protocol|MCP]] merge or compete?
- What happens to discrete apps when [[app-store-outdated]] plays out — who runs the long tail of ephemeral agent-built software?
- Does [[cognitive-core]] emerge first on open-weights ([[deepseek-v3-2|DeepSeek]], [[llama|LLaMA]]) or frontier labs?
- Is [[eureka|Eureka]]'s curriculum still the center of Karpathy's impact, or has the wiki-as-teacher pattern overtaken it?
- The "1960s" (YC 2025) vs "1980s" (Berkeley 2024) [[llm-os]] dating — still unresolved.

## Navigating the Wiki

- **Entry point:** [[andrej-karpathy]] — career arc + table of every Karpathy coinage in the corpus.
- **By era:**
  - *2024 foundation* → [[llm-c]], [[feel-the-agi]], [[snowballs]].
  - *2025 framing* → [[software-3-0]], [[animals-vs-ghosts]], [[march-of-nines]].
  - *2026 practice* → [[agentic-engineering]], [[bacterial-code]], [[claws]], [[autoresearch]], [[byoai]].
- **By theme:**
  - *Product mechanics* → [[partial-autonomy-apps]], [[autonomy-slider]], [[iron-man-analogy]], [[app-store-outdated]].
  - *Reliability arc* → [[march-of-nines]], [[decade-of-agents]], [[tesla-autopilot]], [[waymo]].
  - *LLM psychology* → [[people-spirits]], [[animals-vs-ghosts]], [[jagged-intelligence]], [[llm-cognitive-deficits]], [[ai-psychosis]].
  - *Research direction* → [[cognitive-core]], [[rl-is-terrible]], [[autoresearch]], [[in-context-learning]].
  - *Engineering substrate* → [[bacterial-code]], [[supply-chain-attacks]], [[build-for-agents]], [[claws]], [[intelligence-brownouts]].
  - *Personal computing* → [[byoai]], [[llm-knowledge-bases]], [[government-legibility]].
  - *Pedagogy* → [[ramps-to-knowledge]], [[zero-to-hero]], [[10000-hours]], [[snowballs]], [[cs231n]].
- **By source:** `wiki/sources/*.md` — each source summary links out to every page it touches.
