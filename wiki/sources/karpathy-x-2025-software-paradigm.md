---
title: "2025 — Software Paradigm (YC Talk Drop + Nov Essay + Year-in-Review)"
type: source-summary
created: 2026-04-17
updated: 2026-04-17
sources: [2025/7.19.md, 2025/11.17.md, 2025/12.20.md]
tags: [software-3-0, year-review, verifiability, karpathy-essay]
---

# 2025 — Software Paradigm: YC Talk, Verifiability Essay, Year-in-Review

Three posts that together constitute Karpathy's public 2025 framing of the LLM era.

## Jul 19 — YC AI Startup School talk drops

Public release of *Software Is Changing (Again)* (already ingested as a standalone source — see [[software-is-changing-again]]). Chapter markers from the X post:

| Time | Topic |
|------|-------|
| 0:00 | Software 3.0 — you program LLMs in English |
| 6:06 | LLMs = utility + fab + OS; "computing circa ~1960s" |
| 14:39 | LLM psychology — [[people-spirits]] |
| 18:16 | [[partial-autonomy-apps]] |
| 29:05 | [[vibe-coding]] — English as programming language |
| 33:36 | [[build-for-agents]] |

Also a nod to OpenAI's origin: the name didn't exist when Karpathy joined — his first swag t-shirt says "YC AI Day 1".

## Nov 17 — The verifiability essay

A compact restatement of the Software 2.0 worldview.

> **Software 1.0 easily automates what you can specify.**
> **Software 2.0 easily automates what you can verify.**

Core argument: in Software 1.0 (1980s), the predictive feature of which jobs get automated was whether the algorithm was fixed (rote rules). In Software 2.0, the predictive feature is **verifiability** — whether there's a resettable, efficient, rewardable environment for the AI to practice in.

Verifiable → optimizable via [[reinforcement-learning|RL]] → neural nets learn to excel. Non-verifiable → hope for generalization, or imitation.

This is the mechanism behind [[jagged-intelligence]]: math/code/puzzles leap ahead, creative/strategic/common-sense tasks lag.

## Dec 20 — "Paradigm changes in 2025" (year-in-review)

Karpathy's six personally-notable "paradigm changes" of 2025, each presented as a new **layer** in the stack:

### 1. Reinforcement Learning from Verifiable Rewards (RLVR)
The 2025 capability-overhang story. Labs poured compute originally intended for pretraining into RLVR. This produced reasoning models with a new test-time-compute knob ("thinking time"). o1 (late 2024) showed it; **o3 (early 2025) was the inflection point**. See [[verifiable-rewards]].

### 2. Ghosts vs. Animals / Jagged Intelligence
"We're not evolving animals, we are summoning ghosts." The industry internalized the *shape* of LLM intelligence. Karpathy also admits a **general apathy and loss of trust in benchmarks** — training on the test set is "a new art form." See [[animals-vs-ghosts]], [[jagged-intelligence]].

### 3. Cursor / new layer of LLM apps
"[[cursor|Cursor]] for X" emerged as a product template — apps that do context engineering, orchestrate LLM call DAGs, provide domain GUIs, offer an [[autonomy-slider]]. Debate of the year: will labs capture all apps, or is this layer thick? Karpathy's view: **labs graduate the college student; apps animate the professional**.

### 4. [[claude-code|Claude Code]] / AI that lives on your computer
The first convincing LLM agent form factor — runs on *your* computer with *your* data. Contrast: OpenAI Codex initially went for cloud containers orchestrated from ChatGPT. "CC got this order of precedence correct."

### 5. Vibe coding
"Amusingly, I coined the term 'vibe coding' in this shower of thoughts tweet totally oblivious to how far it would go." The phrase hit Wikipedia and K-12 classrooms. See [[vibe-coding]].

### 6. Nano banana / LLM GUI
Google Gemini "Nano Banana" flagged as "one of the most incredible, paradigm-shifting models of 2025" — not for image quality but for being the **first hint of an LLM GUI**. Text-to-LLMs is like commanding a 1980s terminal; the GUI hasn't been invented yet. Vision is the "10-lane highway into brain." See [[llm-gui]].

## TLDR (Karpathy's own)

> "2025 was an exciting and mildly surprising year of LLMs. LLMs are emerging as a new kind of intelligence, simultaneously a lot smarter than I expected and a lot dumber than I expected… I don't think the industry has realized anywhere near 10% of their potential even at present capability."

## Related

- [[software-3-0]], [[llm-os]]
- [[animals-vs-ghosts]], [[jagged-intelligence]]
- [[verifiable-rewards]], [[rlvr]]
- [[cursor]], [[claude-code]]
- [[vibe-coding]], [[llm-gui]]
- [[decade-of-agents]]
