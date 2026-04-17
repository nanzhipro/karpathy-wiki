---
title: In-Context Learning
type: concept
created: 2026-04-17
updated: 2026-04-17
sources: [andrej-karpathy-were-summoning-ghosts-not-building-animals/transcript.md]
tags: [llm-capabilities, learning, method]
---

# In-Context Learning

The emergent capability of large language models to pick up new patterns, instructions, or tasks from examples placed in the prompt — without weight updates. Karpathy flags it as one of the most surprising and under-theorized properties of modern LLMs.

## Source

[Karpathy, Summoning Ghosts](../sources/summoning-ghosts-not-animals.md) — used as evidence that LLMs are doing something qualitatively richer than next-token prediction in the narrow sense.

## Why it's remarkable

- No gradient steps, yet task performance measurably improves with more examples.
- Works across tasks the model was never explicitly trained for.
- Mechanism is not fully understood — likely some combination of meta-learned amortized Bayesian inference and retrieval-like attention patterns.

## Why it's fragile

- Format-sensitive: small prompt perturbations shift accuracy dramatically.
- Subject to [[jagged-intelligence|jagged performance]] across tasks.
- Gains saturate after a handful of examples; it's not a cheap substitute for fine-tuning on hard distributional shifts.

## Product relevance

- Few-shot prompting is the leanest way to adapt a frontier model to a domain.
- Agent systems rely on it implicitly: tool specs, personas, and examples are all packed into context.
- The [[cognitive-core]] vision depends heavily on strong in-context learning: if the core is small, most specialization happens through context, not weights.

## Related

- [[cognitive-core]]
- [[people-spirits]]
- [[agentic-models]]
