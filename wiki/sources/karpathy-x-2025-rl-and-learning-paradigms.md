---
title: "2025 — RL, System Prompt Learning & Environments"
type: source-summary
created: 2026-04-17
updated: 2026-04-17
sources: [2025/5.11.md, 2025/7.14.md, 2025/7.15.md, 2025/7.21.md, 2025/7.30.md, 2025/8.28.md]
tags: [rl, system-prompt-learning, environments, learning-paradigms, karpathy-coinage]
---

# 2025 — RL, System Prompt Learning & Environments

Six posts across May–August in which Karpathy lays out why RL is a big upgrade over SFT *and* why it is not the end of the story — naming the missing paradigm ([[system-prompt-learning]]) and reframing the data economy around **environments**.

## May 11 — "System Prompt Learning" (the coinage)

> "We're missing (at least one) major paradigm for LLM learning… possibly it has a name — **system prompt learning**?"

| Paradigm | Substrate | What it updates |
|---|---|---|
| Pretraining | Weights | Knowledge |
| Finetuning (SFT/RL) | Weights | Habitual behavior |
| **System prompt learning** (proposed) | **Tokens / context** | **Explicit problem-solving strategies** |

Triggered by reading Claude's ~17,000-word system prompt, full of explicit strategies like *"count letters by assigning a number to each"* to solve the 'r in strawberry' problem. Karpathy's argument: this knowledge should **not** come from engineers hand-authoring prompts, nor (immediately) from RL baking it into weights. It should come from the LLM itself writing lessons for its future self — an explicit, higher-bandwidth feedback channel than a reward scalar. "LLMs are quite literally like the guy in Memento, except we haven't given them their scratchpad yet."

Open design questions:
- How do the edits work? Can the edit policy itself be learned?
- How are lessons distilled from context → weights over time (analogous to sleep)?
- How do you prevent context-window bloat as the lesson database grows?

## Jul 14 — "RL is leveraged, but not the full story"

> "RL is basically 'hey this happened to go well, let me slightly increase the probability of every action I took'."

Two asymptotic problems:
1. As rollouts grow to minutes/hours of interaction, it's suspicious to distill all that work into a single end-of-rollout scalar.
2. Humans don't learn most intellectual tasks this way. They do a **review/reflect stage** — "what went well? what didn't? what should I try next?" — producing explicit lessons (many bits per rollout, not one).

Same argument for [[system-prompt-learning]], now with a concrete example algorithm:

> Given a task, do a few rollouts, stuff them all in one context along with rewards, use a meta-prompt to reflect and extract a "lesson" string, add it to the system prompt (or a lessons DB).

No analogue exists for Atari-style RL because those domains have no LLMs and no in-context learning. Shout-out to [[simon-willison]] on 23 years of blogging in the same post.

## Jul 15 — "RL restricts the field of view"

Short clarifier: the bullishness is on **agentic interactions**, not RL specifically. Review/reflect can build tools for later use, tune the distribution for what to try next (vs. independent sampling from policy), or run in environments with no rewards at all.

## Jul 21 — Micromodels & "perfect pretraining data"

Thought experiment: what does the *highest-grade* pretraining data stream look like if you drop quantity and max quality?

> "Something textbook-like, in markdown? Or possibly samples from a really giant model? Curious what the most powerful e.g. 1B param model trained on 10B tokens looks like."

Current reality: even textbooks in pretraining mixes are "all messed up — weird formatting, OCR bugs, figure text interspersed." No existing stream feels *perfect*. This premise anticipates [[microgpt]] (Feb 2026).

## Jul 30 — nanoGPT as self-improvement benchmark

Karpathy's framing of `nanoGPT` now being a **recursive self-improvement benchmark**:

1. Wrote it to teach GPT training basics.
2. Became the target/baseline for the [[llm-c|llm.c]] port.
3. [[nanogpt#community-evolution|Keller Jordan et al.]] modded it into a research harness — reproducing GPT-2 (124M) dropped from 45 min to 3 min.
4. **Now**: use "how fast can an LLM agent re-optimize training from 45 min → 3 min?" as a coding-agent benchmark. Spoiler: current models do poorly even with strong hints.

Core thesis: **recursive self-improvement is not an event**. It has been under way for decades, smoothly — every IDE, every search engine, every code-completion feature is a rung on that ladder. LLM code assistance is the next rung, not a discontinuity.

## Aug 28 — Environments as the new data

> "Pretraining era → internet text. SFT era → conversations. RL era → **environments**."

Environments let the LLM take actions and see outcomes — statistical expert imitation is no longer the ceiling. But the same fundamental bottleneck applies: need a large, diverse, high-quality collection. Parallels OpenAI's original `gym` project (cartpole, Atari) — now modernized for LLMs by [[prime-intellect|Prime Intellect]]'s environments hub + `verifiers` repo. Once the skeleton exists, the community can parallelize across domains.

Closes with the long-term position:

> "Personally and long-term, I am **bullish on environments and agentic interactions** but **bearish on reinforcement learning specifically**. Reward functions are super sus, and humans don't use RL to learn intellectual problem-solving tasks."

→ Eventually becomes the 2026 [[rl-is-terrible|"RL is terrible"]] tweet.

## Thesis track

These six posts form a single arc:
- **RL is leveraged** (better than SFT, will keep yielding gains)
- **But asymptotically thin** (one scalar for an hour of work)
- **Missing paradigm:** review/reflect → explicit lessons → eventual weight distillation
- **Implementation substrate:** environments, not just more text or RLHF

## Related

- [[system-prompt-learning]] — the named paradigm
- [[reinforcement-learning]], [[rl-is-terrible]]
- [[verifiable-rewards]]
- [[cognitive-core]] — the inference-time side of the same picture
- [[nanogpt]], [[llm-c]]
- [[prime-intellect]]
- [[simon-willison]]
