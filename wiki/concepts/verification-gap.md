---
title: Verification Gap
type: concept
created: 2026-04-18
updated: 2026-04-18
sources: [2025/7.5.md, 2025/10.4.md, 2025/10.19.md, 2025/11.25.md]
tags: [coding, llm-product, cognitive-load, karpathy-endorsed]
---

# Verification Gap

The asymmetric cost of **generation** vs **discrimination** in AI-assisted work. LLMs have collapsed generation to ~instant while doing very little to address discrimination — and discrimination is where most of the cognitive work actually lives.

## The frame ([[karpathy-x-2025-ai-assisted-coding|Jul 5 2025]])

Borrowing GAN terminology:
- **(1) Generation** — make a brush stroke, write a line of code.
- **(2) Discrimination** — look at the result, judge whether it improved things.

> "These two stages are interspersed in pretty much all creative work."

## Discrimination cost by medium

| Medium | Cost | Why |
|---|---|---|
| **Images** | Cheap | The brain has a giant GPU built for images; grids can parallelize comparison |
| **Text** | Expensive | Semantic, discrete, precise; must be read and reasoned about |
| **Audio** | Hardest | Forced time axis — can't parallelize, all serial compute |

## The coding corollary

> "In coding, LLMs have collapsed (1) to ~instant, but have done very little to address (2). A person still has to stare at the results and discriminate if they are good."

**Amdahl's law** applies: if generation goes to zero but verification stays constant, total speedup has a hard ceiling.

## Karpathy's prescription

> "The LLM has to actively work with you to break down problems into little incremental steps, each more easily verifiable. It has to anticipate the computational work of (2) and reduce it as much as possible. It has to really care."

**The biggest misunderstanding non-coders have about coding:**

> "They think coding is about *writing* the code (1). It's not. **It's about staring at the code** (2). Loading it all into your working memory. Pacing back and forth. Thinking through all the edge cases."

## The generator-discriminator gap (Oct 4)

A corollary: evaluating LLMs against each other works because **discrimination is easier than generation**:

> "Have all models generate something, then give it back to all of them and ask them to rank all outputs. I thought models might have a bias to prefer their own outputs, but this doesn't seem to be too strong of an issue. I think it's the generator-discriminator gap on display. That is, it's really hard to write something good, but it's much easier to recognize something good, and the models seem to do it well."

## In education ([[karpathy-x-2025-education|Nov 25]])

The verification-gap argument ported to schools:

> "The verification ability is especially important in the case of AI, which is presently a lot more fallible in a great variety of ways compared to calculators."

Students should be able to verify AI outputs even if they don't generate from scratch every time.

## Why this matters structurally

- Explains [[atrophy]] — if you never exercise (2), you lose the ability to do (1) at all.
- Explains why [[autonomy-slider]] sweet spot stays in the middle — pushing (1) up is cheap; reducing (2) work is the actual product.
- Frames [[claude-code|Claude Code]]'s and [[cursor|Cursor]]'s UX job — not "emit more code" but "emit less-to-verify code."
- Makes Karpathy's "too agentic by default" complaint ([[karpathy-x-2025-ai-assisted-coding|Aug 25]]) structural, not aesthetic — agents blast past verification budgets.

## Related

- [[atrophy]]
- [[autonomy-slider]]
- [[agentic-engineering]]
- [[ramps-to-knowledge]]
- [[vibe-coding]]
- [[code-post-scarcity]]
