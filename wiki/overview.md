---
title: Overview
type: overview
created: 2026-04-15
updated: 2026-04-18
sources: [Andrej Karpathy.md, 4.10.md, andrej-karpathy-software-is-changing-again/transcript.md, andrej-karpathy-were-summoning-ghosts-not-building-animals/transcript.md, andrej-karpathy-berkeley-ai-hackathon-2024-keynote/transcript.md, andrej-karpathy-gpu-mode-irl-2024-keynote/transcript.md, 2025 corpus, 2026 corpus]
tags: [overview, karpathy, llm, agents, software-3-0, agentic-engineering, 2025, 2026]
---

# karpathy-wiki — Overview

> Top-level synthesis of the entire knowledge base.
> Revised as sources are ingested and understanding deepens.

## Scope

A research wiki built from Andrej Karpathy's self-bio, X posts (2024–2026), talks, and interviews. Covers the LLM era's pedagogy, product shape, reliability arc, engineering substrate, **the 2025 verifiability/RLVR paradigm shift**, and — with the 2026 corpus — the emergent practice of **agentic engineering**.

## Current State

**~31 sources ingested** spanning October 2024 → April 2026:

**Foundational (2024–early 2025):**
1. **GPU MODE IRL 2024** (Oct 2024) — systems / CUDA talk; [[llm-c|llm.c]] origin story.
2. **Berkeley SkyDeck Hackathon keynote** (2024) — "[[feel-the-agi]]", [[snowballs]], [[10000-hours]].
3. **April 10 2025 X post** — [[peaky-capability]], [[ai-psychosis]].
4. **karpathy.ai self-bio** — verified career timeline 2005–2024.

**2025 X-post corpus (16 thematic bundles, Apr–Dec 2025):**
5. **Apr 8 — [[power-to-the-people]]**: LLM diffusion inversion, individuals benefit more than orgs.
6. **Apr–Dec — [[karpathy-x-2025-ai-assisted-coding|AI-assisted coding]]**: seven-step inner loop, [[verification-gap]], ChatGPT router, [[code-post-scarcity]], "I've never felt this much behind."
7. **Apr–Nov — [[karpathy-x-2025-build-for-agents|Build for agents]]**: MenuGen, LLM GUI, horseless-carriage framing, [[context-engineering]] endorsement.
8. **Apr / Aug / Nov — [[karpathy-x-2025-evals-and-model-vibes|Evals & model vibes]]**: leaderboard illusion, OpenRouter rankings, model smell, llm-council.
9. **May–Aug — [[karpathy-x-2025-rl-and-learning-paradigms|RL & learning paradigms]]**: [[system-prompt-learning]] coinage, environments-as-new-data, [[rl-is-terrible]].
10. **Jul 3 / Jul 18 — [[karpathy-x-2025-video-gen|Video gen]]**: Veo 3, MirageLSD real-time diffusion.
11. **Jul 6 — [[karpathy-x-2025-bacterial-code-origin|Bacterial code origin]]**: the coinage that anchors the 2026 malleable-software arc.
12. **Jul 24 / Nov 13–14 — [[karpathy-x-2025-tesla-fsd|Tesla FSD]]**: HW4 Model X "no notes" drive, [[software-2-0|Software 2.0]] victory lap.
13. **Jul 27 — [[karpathy-x-2025-cognitive-core|Cognitive core spec]]**: multimodal, matryoshka, LoRA slots, delegates to cloud oracles.
14. **Jul 19 / Nov 17 / Dec 20 — [[karpathy-x-2025-software-paradigm|Software paradigm]]**: [[verifiability]], [[rlvr]] as #1 paradigm change of 2025.
15. **Oct 2 / Nov 22 / Dec 8 — [[karpathy-x-2025-ghosts-and-psychology|Ghosts & LLM psychology]]**: [[animals-vs-ghosts]] frame extended, [[people-spirits]] clarified.
16. **Oct 13–24 / Dec 9 — [[karpathy-x-2025-nanochat-saga|nanochat saga]]**: release, $1000 d32 scale-up, identity via synthetic data, SpellingBee capability graft.
17. **Oct 19 — [[karpathy-x-2025-dwarkesh-recap|Dwarkesh recap]]**: timeline clarifications, 5–10X pessimistic, critique of [[richard-sutton|Sutton]]'s pure-RL stance.
18. **Nov 18 / Dec 11 — [[karpathy-x-2025-llm-reading|LLM reading]]**: [[reader3|Reader3]] tool, [[hn-time-capsule|HN Time Capsule]], [[galaxy-brain-reasoning]].
19. **Nov 25 — [[karpathy-x-2025-education|Education]]**: AI detectors don't work, in-class grading, AI-capable + AI-free.
20. **Misc. (23 posts)** — digital hygiene, [[prompt-injection]], public goods, jobs/radiology, vibe-coding culture, one-liners.

**2026 X-post corpus (10 thematic bundles):**
21. **Jan 1 — FSD coast-to-coast** (2,732 mi, zero interventions).
22. **Jan 8 / 29, Feb 2 — nanochat GPT-2 reproduction** ($20 on 8×H100).
23. **Jan 27 — Claude coding reflections** ([[agentic-engineering]], [[atrophy]]).
24. **Feb 5 / 25 — agentic engineering naming + phase-shift note**.
25. **Feb 12 / 17 / 20 / 21 — malleable software** ([[bacterial-code]], [[microgpt]], [[app-store-outdated]]).
26. **Feb 4 / 13 — agent networks** ([[simile-ai]], [[org-code]]).
27. **Feb 26 → Mar 20 — autoresearch + Claws + command-center IDE**.
28. **Mar 19 / Mar 31 — supply-chain attacks** (litellm, axios).
29. **Apr 3 / 5 — LLM knowledge bases + [[byoai|BYOAI]]**.
30. **Misc.** — point-vs-slope, memory overfit, "argue the opposite."

**Long-form talks/interviews:**
31. **YC AI Startup School keynote** (*Software Is Changing Again*, June 2025) — [[software-3-0]], [[llm-os]].
32. **Dwarkesh Patel interview** (Oct 2025) — [[animals-vs-ghosts]], [[march-of-nines]], [[cognitive-core]], [[rl-is-terrible]].

## Central Claims Across the Corpus

### 1. Verifiability is the Software 2.0 automation predicate

The **[[verifiability|Nov 17 2025]]** essay compressed a decade of Software 2.0 thinking: *Software 1.0 automates what you can specify; Software 2.0 automates what you can verify*. [[rlvr|RLVR]] (the 2025 paradigm change) was the training-side operationalization. [[jagged-intelligence]] is the observable surface.

### 2. Software 3.0 is now **agentic engineering**

The 2025 frame ([[software-3-0]]) evolved in 2026 into a named practice: [[agentic-engineering]]. LLMs are not just the new runtime — they are the new *collaborators*. The bottleneck shifts from writing code to reviewing what agents wrote ([[atrophy]], [[verification-gap]], [[10x-engineer]]).

### 3. The decade of agents has started — but the ceiling is human review

[[decade-of-agents]] + [[march-of-nines]] hold. **Jan 1 2026's Tesla FSD coast-to-coast** (zero interventions) is the first clean cash-out of the march-of-nines framing. Coding agents sit earlier on the same curve — see [[claws]], [[autoresearch]], [[atrophy]], [[verification-gap]].

### 4. Build **partial-autonomy apps** with an [[autonomy-slider]]

[[iron-man-analogy|Suits, not robots.]] [[cursor|Cursor]], [[perplexity|Perplexity]], [[claude-code|Claude Code]], [[openai-codex|Codex]] converge. 2025's layered tool stack (Cursor tab 75% / highlight / CC / GPT-5 Pro) is the explicit evidence. By 2026, Karpathy generalizes: entire application categories collapse into [[app-store-outdated|ephemeral agent-built apps]].

### 5. LLMs are [[people-spirits|people spirits]], not animals

[[animals-vs-ghosts]] is the stable psychological frame, defended multiple times in 2025. Their [[llm-cognitive-deficits|deficits]] — no persistent memory, [[ai-psychosis|psychosis]] under long runs, [[model-collapse|collapse]] under self-consumption — are explicit constraints on product design and [[byoai|personalization strategy]].

### 6. Capability is peaky; [[verifiable-rewards]] concentrate the spikes

[[peaky-capability]] + [[rl-is-terrible|"RL is terrible"]] + [[verifiability]] are three views of one fact: gains concentrate where rewards are clean. The 2025 paradigm ([[rlvr]]) turned this into product surface (reasoning models, test-time-compute dial). 2026's [[autoresearch]] pushes verifiability into ML research itself.

### 7. The right model is a [[cognitive-core]]

Small reasoning core, retrieval, tools. **Jul 27 2025** crystallized the spec (multimodal, matryoshka, LoRA slots, tool-using). 2026 adds nuance: the cognitive core should live *on your side of the network* — locally runnable, [[byoai|swappable across providers]], resistant to [[intelligence-brownouts]].

### 8. Products and code must be [[build-for-agents|built for agents]]

2025 named the frontier (MenuGen blog, [[llm-gui|LLM GUI]], [[context-engineering]]). 2026 reinforces: products need CLI / API / MCP, docs in markdown, Skills; code should be [[bacterial-code|bacterial]] (small, dependency-free, rippable). The cost/benefit of `pip install` flipped after the 2026 [[supply-chain-attacks|supply-chain attacks]] — which the [[prompt-injection|Jul 11 2025]] "wild-west" post had anticipated.

### 9. Pedagogy is a [[ramps-to-knowledge|ramp]], and the ramp runs through the wiki

Karpathy's stack — [[cs231n]], [[zero-to-hero]], [[micrograd]], [[nanogpt]], [[microgpt]], [[llm-c]], [[nanochat]] — is graded climbs. The Oct 2025 **[[karpathy-x-2025-nanochat-saga|nanochat release]]** is the 2025 rung on that ladder. 2026's meta-move: the knowledge base itself is a ramp (see [[llm-knowledge-bases]]) and this wiki is an instance.

### 10. Individuals benefit disproportionately — for now

**[[power-to-the-people|Apr 8 2025]]** made the economic thesis explicit: LLMs *invert* the usual top-down technology diffusion. Individuals adopt faster than orgs because the capability shape (quasi-expert across many domains) fits them. The 2026 [[byoai|BYOAI]] stance is the logical next step. The risk: dynamic range re-opens and the elite can buy better models.

### 11. The Dec 2025 phase shift

The Feb 25 2026 post explicitly marks a qualitative transition: "something shifted in December 2025." Frontier agentic coding crossed a threshold — long-horizon coherence, autonomous dev loops, review-as-bottleneck became real. The Dec 20 2025 [[karpathy-x-2025-software-paradigm|year-in-review]] catalogues the inputs: [[rlvr]] inflection, environment-as-data, Meta's Llama stumble, Grok's lab emergence, China's open-weight surge.

## Open Questions

- Does [[byoai]] stay a hobbyist stance, or become the default for serious research workflows?
- Does [[autoresearch]] become a public "SETI@home for ML" or stay single-operator?
- How do [[claws]] and [[model-context-protocol|MCP]] merge or compete?
- What happens to discrete apps when [[app-store-outdated]] plays out?
- Does [[cognitive-core]] emerge first on open-weights ([[deepseek-v3-2|DeepSeek]], [[llama|LLaMA]]) or frontier labs?
- Does the Apr 2025 "flat dynamic range" prediction hold, or does test-time-scaling re-open the elite gap?
- Does [[verification-gap]] close (better discrimination tooling) or widen (agents scale faster than reviewers)?
- The "1960s" (YC 2025) vs "1980s" (Berkeley 2024) [[llm-os]] dating — still unresolved.

## Navigating the Wiki

- **Entry point:** [[andrej-karpathy]] — career arc + table of every Karpathy coinage in the corpus.
- **By era:**
  - *2024 foundation* → [[llm-c]], [[feel-the-agi]], [[snowballs]].
  - *2025 framing* → [[power-to-the-people]], [[verifiability]], [[rlvr]], [[software-3-0]], [[animals-vs-ghosts]], [[march-of-nines]], [[cognitive-core]], [[code-post-scarcity]].
  - *2026 practice* → [[agentic-engineering]], [[bacterial-code]], [[claws]], [[autoresearch]], [[byoai]].
- **By theme:**
  - *Product mechanics* → [[partial-autonomy-apps]], [[autonomy-slider]], [[iron-man-analogy]], [[app-store-outdated]], [[llm-gui]].
  - *Reliability arc* → [[march-of-nines]], [[decade-of-agents]], [[tesla-autopilot]], [[waymo]].
  - *LLM psychology* → [[people-spirits]], [[animals-vs-ghosts]], [[jagged-intelligence]], [[llm-cognitive-deficits]], [[ai-psychosis]], [[galaxy-brain-reasoning]].
  - *Research direction* → [[cognitive-core]], [[rl-is-terrible]], [[rlvr]], [[verifiability]], [[autoresearch]], [[system-prompt-learning]], [[in-context-learning]].
  - *Engineering substrate* → [[bacterial-code]], [[supply-chain-attacks]], [[prompt-injection]], [[build-for-agents]], [[context-engineering]], [[claws]], [[intelligence-brownouts]].
  - *Work-on-code loop* → [[verification-gap]], [[atrophy]], [[code-post-scarcity]], [[10x-engineer]], [[vibe-coding]], [[agentic-engineering]].
  - *Personal computing* → [[power-to-the-people]], [[byoai]], [[llm-knowledge-bases]], [[government-legibility]].
  - *Pedagogy* → [[ramps-to-knowledge]], [[zero-to-hero]], [[10000-hours]], [[snowballs]], [[cs231n]].
- **By source:** `wiki/sources/*.md` — each source summary links out to every page it touches.
