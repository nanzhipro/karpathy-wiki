---
title: System Prompt Learning
type: concept
created: 2026-04-18
updated: 2026-04-18
sources: [2025/5.11.md, 2025/7.14.md, 2025/10.19.md]
tags: [learning-paradigms, meta-learning, karpathy-coinage]
---

# System Prompt Learning

Karpathy's proposed third learning paradigm for LLMs — alongside pretraining (weights, knowledge) and finetuning (weights, habits), a paradigm that updates the **system prompt / context** with explicit problem-solving strategies.

## The coinage

[[karpathy-x-2025-rl-and-learning-paradigms|May 11 2025]]:

> "We're missing (at least one) major paradigm for LLM learning. Not sure what to call it, possibly it has a name — **system prompt learning**?"

## The three paradigms

| Paradigm | Substrate | What updates |
|---|---|---|
| Pretraining | Weights | Knowledge |
| Finetuning (SFT/RL) | Weights | Habitual behavior |
| **System prompt learning** | Tokens / context | Explicit strategies ("lessons") |

## Triggering observation

Claude's ~17,000-word system prompt contains not just style preferences but **general problem-solving strategies** — e.g. "to count letters, assign a number to each and increment an explicit counter." This kind of knowledge should *not* be hand-written by engineers, and it's wasteful to bake into weights via RL when the model could just *remember it in text*.

> "LLMs are quite literally like the guy in Memento, except we haven't given them their scratchpad yet."

## Why it should work

- **Review/reflect extracts more bits per rollout than a reward scalar.** One explicit lesson beats one scalar across N tokens.
- **Matches human intellectual learning.** "It seems when I encounter this kind of problem, I should try this kind of approach."
- **Distillation to weights can happen separately**, like sleep — move from explicit text strategy to habitual weight.

## Example algorithm ([[karpathy-x-2025-rl-and-learning-paradigms|Jul 14]])

> Given a task, do a few rollouts, stuff them all into one context window with their rewards, use a meta-prompt to reflect on what went well, extract a "lesson" string, add it to the system prompt (or a lessons DB).

## Open questions

- How do the edits work? Can the edit policy itself be learned?
- How do you distill lessons → weights over time?
- How do you prevent context-window bloat as the lessons DB grows?

## Primordial deployed examples

Karpathy in the [[karpathy-x-2025-dwarkesh-recap|Dwarkesh recap]]:

> "ChatGPT memory is maybe a primordial version of this, though it is only used for customization not problem solving."

## Relation to other concepts

- **[[reinforcement-learning|RL]]** — the contrast. RL: dense scalar → weights. SPL: explicit lesson → context.
- **[[cognitive-core]]** — SPL is the mechanism that would keep a small core functional at many domains without memorizing everything.
- **[[rl-is-terrible]]** — the negative-space case for SPL.
- **[[context-engineering]]** — the manual version; SPL is the automated version.

## Related

- [[reinforcement-learning]]
- [[cognitive-core]]
- [[rl-is-terrible]]
- [[context-engineering]]
- [[verifiable-rewards]]
