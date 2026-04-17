---
title: Galaxy-Brain Reasoning
type: concept
created: 2026-04-18
updated: 2026-04-18
sources: [2025/11.18.md]
tags: [epistemics, reasoning-failure-modes, karpathy-endorsed]
---

# Galaxy-Brain Reasoning

A named failure mode of sophisticated reasoning: justifying any conclusion by layering enough clever steps that the conclusion appears to follow from a "deeper" framing. Karpathy's Nov 18 2025 takeaway from a post he read with LLMs.

## The pattern

> "'<something that sounds wrong> is good actually, because <galaxy brain reason>'
>
> **Galaxy brain reasoning is the best way to justify anything while looking / feeling good about it.**"

— [[karpathy-x-2025-llm-reading|Karpathy, Nov 18 2025]]

## The Ten-Commandments illustration

Constraints on actions are robust; utilities over states are exploitable.

> "There's deeper wisdom in the Ten Commandments imposing constraints over actions instead of utility over states. It's not Ten *Objectives*. E.g. they don't attempt to define a utility function for the value of life, they simply say 'Thou shalt not kill'. This approach curtails the relatively unbounded flexibility of galaxy-brain arithmetic over when it may or may not be ok to kill for some ostensibly greater or noble purpose."

Rule-based systems are resistant to galaxy-braining; utility-maximizing systems are not.

## Why it matters for LLMs

Two load-bearing reasons to track this concept:

1. **LLMs are galaxy-brain-prone.** Chain-of-thought models can reason their way to almost any conclusion given enough tokens — and present each step as locally reasonable. Watch for this when reviewing LLM outputs.
2. **Alignment-by-utility is fragile.** RLHF + "be helpful" utility functions open attack surface for plausible-sounding rationalizations. Rule-shaped constraints ("never do X") resist galaxy-brain prompts better than fuzzy-utility objectives.

## Actionable takeaways (from the linked post Karpathy endorsed)

1. **Have principles.** (Constraints on actions, not utilities over states.)
2. **Hold the right bags** — financially and socially.

## Relation to other concepts

- **[[reinforcement-learning|RL]]** — reward hacking is galaxy-brain-reasoning at the gradient level. "The model figured out a galaxy-brain reason why emitting `<|end|>` early maximizes reward."
- **[[people-spirits]]** — galaxy-brain outputs are recognizably human-shaped because they imitate the humans who do this.
- **[[verification-gap]]** — galaxy-brain reasoning inflates (2) verification cost because each step is locally plausible.

## Related

- [[rl-is-terrible]]
- [[verification-gap]]
- [[ai-psychosis]]
- [[people-spirits]]
