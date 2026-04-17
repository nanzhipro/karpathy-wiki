---
title: Andrej Karpathy
type: entity
created: 2026-04-15
updated: 2026-04-17
sources: [Andrej Karpathy.md, 4.10.md, andrej-karpathy-software-is-changing-again/transcript.md, andrej-karpathy-were-summoning-ghosts-not-building-animals/transcript.md, andrej-karpathys-keynote-winner-pitches-at-uc-berkeley-ai-hackathon-2024-awards-ceremony/transcript.md, gpu-mode-irl-2024-keynotes/transcript.md, 2026/1.8.md, 2026/1.27.md, 2026/2.12.md, 2026/4.5.md]
tags: [person, researcher, educator, openai, tesla]
---

# Andrej Karpathy

**Type:** Person — researcher, educator, founding member of [[openai|OpenAI]], ex–[[tesla|Tesla]] director of AI, ex–Google Brain / DeepMind, "the reference human for ImageNet" (GPU MODE host intro).

Primary subject of this wiki — the wiki is seeded from his X posts, talks, interviews, and open-source projects.

Self-description (karpathy.ai bio):
> "I like to train deep neural nets on large datasets 🧠🤖💥"

## Career arc (verified dates from self-bio)

| Period | Role | Notes |
|--------|------|-------|
| 2005 – 2009 | **BSc, University of Toronto** | Double major CS + physics, math minor. First exposure to deep learning via **Geoff Hinton's class** and reading groups. |
| 2009 – 2011 | **MSc, University of British Columbia** | Adviser: Michiel van de Panne. Learned controllers for physically-simulated agile figures — ML-for-robotics in simulation. |
| 2011 – 2015 | **PhD, Stanford** | Adviser: **Fei-Fei Li** (Stanford Vision Lab). Thesis: convolutional / recurrent networks for CV, NLP, and their intersection. First-year rotations with Daphne Koller, Andrew Ng, Sebastian Thrun, Vladlen Koltun. |
| 2011, 2013, 2015 | **Internships** | Google Brain 2011 (unsup. video learning); Google Research 2013 (large-scale supervised YouTube video); DeepMind 2015 (deep RL, with Koray Kavukcuoglu & Vlad Mnih). |
| 2015 – 2017 | **OpenAI (founding)** | Research scientist, founding member. |
| 2017 – 2022 | **Tesla, Director of AI** | Led Autopilot computer-vision team; briefly Tesla Optimus. Owned in-house data labeling, training, deployment on Tesla's custom inference chip. |
| 2023 – 2024 | **OpenAI (return)** | Built a new team on **midtraining** and **synthetic data generation**. |
| 2024 – | **Independent educator, [[eureka|Eureka]] founder** | [[zero-to-hero|Zero to Hero]] technical track; general-audience videos ("Deep Dive into LLMs", "How I use LLMs", "Intro to Large Language Models"). Primary presence on X/Twitter and GitHub. |

## CS231n

- **Designer and primary instructor** of the first deep-learning course at Stanford, [[cs231n|CS231n]].
- Enrollment growth: **150 (2015) → 330 (2016) → 750 (2017)** — one of the largest classes at Stanford.
- Canonical reference for convolutional-networks pedagogy and the seed of his later [[ramps-to-knowledge|ramps-to-knowledge]] philosophy.

## Open-source ladder

From the self-bio pattern and the [[llm-knowledge-bases|wiki]] corpus:

- [[micrograd]] — scalar autograd engine.
- [[nanogpt]] — minimal GPT train/infer.
- [[microgpt]] — 200-LoC GPT.
- [[nanochat]] — full-stack ChatGPT clone, reproducible for under $100.
- [[llm-c]] — "assembly for Software 2.0."
- [[autoresearch]] — agent-driven ML research harness (2026).

## [[eureka|Eureka]]

Current AI-education venture framed as "Starfleet Academy" / "gym for the mind."

## Positions observed in this wiki

- [AI Capability Gap](../sources/ai-capability-gap.md) (X post, 2025) — capability is [[peaky-capability|peaky]]; [[verifiable-rewards]] is the lever; [[ai-psychosis]] describes the perceptual split between casual and professional users.
- [Software Is Changing (Again)](../sources/software-is-changing-again.md) (YC AI Startup School, June 2025) — three-paradigm framing ([[software-3-0|Software 1.0/2.0/3.0]]); LLMs as utilities / fabs / OS ([[llm-os]]); [[people-spirits]] psychology; [[partial-autonomy-apps]] as the winning product shape; [[iron-man-analogy]] for augmentation over automation; [[vibe-coding]] and [[build-for-agents]].
- [Summoning Ghosts, Not Animals](../sources/summoning-ghosts-not-animals.md) (Dwarkesh, October 2025) — [[animals-vs-ghosts]]; [[rl-is-terrible|RL is "sucking supervision through a straw"]]; [[cognitive-core]] as the right target; [[decade-of-agents]] timeline; [[march-of-nines]] explaining self-driving and agents; [[ramps-to-knowledge]] pedagogy via [[eureka]].
- [Berkeley AI Hackathon 2024 Keynote](../sources/berkeley-ai-hackathon-2024-keynote.md) — [[feel-the-agi]], [[snowballs]], [[10000-hours]]; proto-[[llm-os]] framing.
- [GPU MODE IRL 2024 — llm.c](../sources/gpu-mode-irl-2024-keynote.md) — [[llm-c]] as "assembly for Software 2.0"; prediction that LLMs become compilers writing custom low-level code.

## Recurring themes across the corpus

- **The autonomy slider.** Tesla/Waymo → Cursor/Perplexity → agents. Keep humans in the loop; grow autonomy conservatively. See [[autonomy-slider]].
- **Decade, not year.** Agents are a decade away. First stated in the Berkeley keynote, reinforced in [[software-is-changing-again]], made central in [[summoning-ghosts-not-animals]]. See [[decade-of-agents]].
- **Build ramps, not moats.** [[ramps-to-knowledge|Ramps to knowledge]] — micrograd, nanoGPT, nanochat, llm.c — small, readable, strong baselines that take a learner from 0 to operational understanding.
- **Publish your work.** Snowballs + 10,000 hours + dopamine feedback. Cross-source (Berkeley keynote, implicit in GPU MODE talk).
- **LLMs as new stack.** Utilities / fabs / OS, with a Linux/[[llama]] wing and a Windows/GPT wing.

## Karpathy's coinages tracked in this wiki

| Coinage | Source | Page |
|---|---|---|
| Software 3.0 | [[software-is-changing-again]] | [[software-3-0]] |
| LLM OS | Berkeley 2024, YC 2025 | [[llm-os]] |
| People spirits | YC 2025 | [[people-spirits]] |
| Vibe coding | 2025 X post | [[vibe-coding]] |
| Summoning ghosts, not building animals | Dwarkesh 2025 | [[animals-vs-ghosts]] |
| Cognitive core | Dwarkesh 2025 | [[cognitive-core]] |
| March of nines | Dwarkesh 2025 (older usage in Tesla era) | [[march-of-nines]] |
| Sucking supervision through a straw (RL) | Dwarkesh 2025 | [[rl-is-terrible]] |
| AI psychosis | 4.10 X post | [[ai-psychosis]] |
| Jagged intelligence | YC 2025 | [[jagged-intelligence]] |
| Iron Man suit vs robot | YC 2025 | [[iron-man-analogy]] |
| Feel the AGI | Berkeley 2024 | [[feel-the-agi]] |
| Agentic engineering | Feb 5 2026 X post | [[agentic-engineering]] |
| Slopacolypse | 2026 X posts | [[slopacolypse]] |
| Bacterial code | Feb 12 2026 | [[bacterial-code]] |
| Claws | Mar 6 2026 | [[claws]] |
| Autoresearch | Feb 28 / Mar 8 2026 | [[autoresearch]] |
| BYOAI | Apr 5 2026 | [[byoai]] |
| Intelligence brownouts | Mar 20 2026 | [[intelligence-brownouts]] |
| App store outdated | Feb 20 2026 | [[app-store-outdated]] |
| Org code | 2026 | [[org-code]] |

## 2026 arc (corpus-specific)

The early-2026 X post corpus shows Karpathy consolidating a full stack around **agentic engineering**:

- **Jan 1 FSD coast-to-coast** (2,732 mi, zero interventions) — the [[march-of-nines]] milestone cashes out.
- **Jan 8 + Jan 29 + Feb 2** — [[nanochat]] reproduces GPT-2 for under $100 (600× cost reduction).
- **Jan 27** — long "Claude coding notes" post crystallizes [[agentic-engineering]] and [[atrophy]].
- **Feb 12** — [[microgpt]] + [[bacterial-code]] + the "yoink" workflow.
- **Feb 20** — [[app-store-outdated]]: apps become ephemeral.
- **Feb 28 – Mar 10** — [[autoresearch]] evolves from demo to public repo to 11% loss improvements.
- **Mar 6** — [[claws]]: orchestration above agents.
- **Mar 19 + Mar 31** — [[supply-chain-attacks]] posts (litellm, axios).
- **Mar 20** — [[intelligence-brownouts]].
- **Apr 3 + Apr 5** — [[llm-knowledge-bases]] + [[byoai]] — the stack this very wiki instantiates.
