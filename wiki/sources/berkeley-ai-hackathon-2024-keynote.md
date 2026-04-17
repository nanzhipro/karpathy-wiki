---
title: Berkeley SkyDeck AI Hackathon 2024 — Karpathy Keynote
type: source-summary
created: 2026-04-17
updated: 2026-04-17
sources: [andrej-karpathys-keynote-winner-pitches-at-uc-berkeley-ai-hackathon-2024-awards-ceremony/transcript.md]
tags: [llm-os, snowballs, 10000-hours, projects, feel-the-agi, karpathy]
---

# Berkeley SkyDeck AI Hackathon 2024 — Keynote

**Speaker:** [[andrej-karpathy|Andrej Karpathy]]
**Venue:** UC Berkeley AI Hackathon Awards Ceremony (Berkeley SkyDeck, July 2024)
**Original source:** `raw/youtube-transcript/berkeley-skydeck/andrej-karpathys-keynote-winner-pitches-at-uc-berkeley-ai-hackathon-2024-awards-ceremony/transcript.md`
**Format:** keynote (~18 min) followed by student team pitches (~65 min)

## Thesis

Karpathy addresses ~350 student hackers who just shipped 371 projects in 36 hours. His framing: we're in the **~1980s of LLM computing**, a transitional era structurally similar to early personal computing. The practical advice distills to three messages — **feel the AGI** (enumerate what's newly possible), **build project snowballs** (small projects compound into large careers), and **10,000 hours** (only top-of-funnel work builds expertise).

## Key Claims

1. **LLMs are ~1980s-era computing.** LLMs today rhyme with mainframes → minicomputers → PCs. We're early; the "personal LLM" revolution hasn't happened. The tokens-in-a-terminal UX is the 1970s-teletype analog. Students entering now are in the same position as programmers in the early 1980s: a reshaped landscape, everything to be built. *(framing, expanded further in [[software-is-changing-again]])*
2. **["Feel the AGI"]] is the posture hackers should adopt.** Karpathy contrasts *Her* (1-on-1 partnership with AI) and *I, Robot* (ubiquitous AI infrastructure) as two complementary visions — not WALL·E, where humans are atrophied on recliners. The right picture: humans and nature thriving with the AI layer largely invisible. Imagine what's now possible; build accordingly. *(vision framing)*
3. **Build [[snowballs|project snowballs]].** The talk's most concrete career advice: small public projects accrete into bigger ones. Karpathy walks through his own chain — Rubik's cube videos (~2007) → CS231n (Stanford, 2015) → [[zero-to-hero|Zero to Hero]] YouTube series → [[llm101n|LLM101n]] course; and separately, a Reddit chatbot hack → GPT-4o conversations. Each project is the ramp for the next. *(autobiographical)*
4. **The [[10000-hours|10,000-hour rule]] is real.** Expertise requires an enormous amount of top-of-funnel work. Publishing projects creates feedback loops (dopamine, collaborators, invitations) that make the long grind sustainable. The hackathon itself is a node in that loop. *(motivational claim)*
5. **LLM-OS is coming into view.** Karpathy previews what will become the [[llm-os]] thesis in [[software-is-changing-again]]: LLMs as the kernel of a new operating system, with orchestration, memory, tools, multi-agent coordination, and a UX layer. The Berkeley talk is where this framing is introduced publicly; by June 2025 it's the central metaphor. *(proto-framing)*
6. **Side projects compound.** Karpathy flags his [[awesomemovies-life|awesomemovies.life]] weekend project (movie recommender via embeddings) and the 2017 Tesla PyTorch rewrite as examples of one-weekend efforts that matter. The Tesla rewrite in particular: swapping the entire autopilot codebase from Lua/Torch to PyTorch was "a weekend project" that became load-bearing infrastructure. *(single-source anecdote)*

## Structure of the Talk

1. **Welcome** — SkyDeck GM Caroline Winnett opens (371 projects, 8 finalists, ~$100K prizes).
2. **Karpathy keynote (~18 min):**
   - *Where we are:* ~1980s of LLM computing, the "LLM-OS" view.
   - *Feel the AGI:* *Her* / *I, Robot* / not-WALL·E.
   - *Project snowballs:* his own stack, from Rubik's videos to LLM101n.
   - *10,000 hours:* the non-glamorous part.
   - *Dopamine via publishing:* projects pay you in feedback.
3. **Student pitches** (less central to Karpathy's corpus; summarized below for completeness).

## Notable Quotes (Karpathy keynote)

> "It's roughly the 1980s of computing for large language models."

> "I don't want the WALL·E world. I want the world where humans and nature are thriving, and the intelligence layer is largely invisible."

> "Projects are snowballs. You start rolling something small and it picks up mass — and before you know it, the next project is bigger than the last one, because it stands on the first."

> "Publishing your work is the cheat code for the 10,000 hours. You're going to do it anyway — you might as well have people watching."

## Student Pitches (context only — not core to Karpathy's positions)

Eight finalist teams pitched 36-hour builds, judged by a SkyDeck panel. Winners for cross-referencing: **Dispatch AI** (AI 911 operator, grand prize + $25K + $2.5K OpenAI credits); **Greenwise** (carbon-footprint RAG-adjacent tool, SkyDeck Climate Tech track); **ScamScanner**, **Bloom Buddy**, **lock in** (Hume empathic-AI prizes); **Frodo** (Reach Capital edtech prize); **Transparify**, **Eventsdash.ai** (You.com prizes); **ASL Bridgify** (AIC AI-for-Good prize). Karpathy did not comment on individual projects in the recorded segment.

## Named Entities & References (Karpathy keynote)

- [[andrej-karpathy|Andrej Karpathy]] — speaker
- [[openai]] — founding member context
- [[tesla]] — 2017 PyTorch rewrite anecdote
- [[cs231n]] — Stanford course Karpathy built
- [[zero-to-hero]] — YouTube series
- [[llm101n]] — course project (announced-but-unfinished at the time)
- [[awesomemovies-life|awesomemovies.life]] — Karpathy weekend demo
- [[nanogpt]], [[micrograd]] — referenced as teaching artifacts

## Concepts Introduced / Reinforced

- [[llm-os]] — first public appearance in Karpathy's talks (proto-form)
- [[snowballs]] — project-compounding philosophy
- [[10000-hours]] — the long-tail of skill
- [[feel-the-agi]] — the imaginative posture
- [[ramps-to-knowledge]] — implicit here, formalized in [[summoning-ghosts-not-animals]]

## Open Questions

- Is the "1980s" dating stable? By [[software-is-changing-again]] (2025), Karpathy has shifted to "~1960s" — worth tracking the drift.
- How does the snowball model handle the survivor-bias problem (projects that never land)? Karpathy doesn't address it.

## My Reading (commentary)

This is the **template keynote** Karpathy gives to early-career audiences: `feel the AGI + snowballs + 10,000 hours`. The frames that later become load-bearing ([[llm-os]], [[ramps-to-knowledge]]) appear here in proto-form. The ~1980s → ~1960s drift between this talk and the 2025 YC talk is interesting: either Karpathy revised his estimate of how early we are, or the time-shared-terminal + centralized-compute situation felt more 1960s-like by mid-2025. Worth flagging as a position that shifted.
