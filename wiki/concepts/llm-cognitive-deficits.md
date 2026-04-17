---
title: LLM Cognitive Deficits
type: concept
created: 2026-04-17
updated: 2026-04-17
sources: [andrej-karpathy-were-summoning-ghosts-not-building-animals/transcript.md, andrej-karpathy-software-is-changing-again/transcript.md]
tags: [llm-psychology, evaluation, karpathy]
---

# LLM Cognitive Deficits

Karpathy's catalog of the systematic *non-human* failure modes of current LLMs — the problems that make them [[people-spirits|people-shaped but not people]]. These aren't bugs in individual models; they're structural consequences of how the system is built.

## Sources

- [Karpathy, Summoning Ghosts](../sources/summoning-ghosts-not-animals.md) — most detailed taxonomy.
- [Karpathy, Software Is Changing (Again)](../sources/software-is-changing-again.md) — the product-side consequences (why UIs must absorb the deficits).

## The deficits

1. **No persistent memory.** Each conversation starts fresh. Whatever was learned yesterday is gone. Contrast: a human colleague who slowly builds context.
2. **Anterograde amnesia analog.** Even *within* a session, fine-grained episodic memory fades as the context fills. Models don't know they've forgotten.
3. **Confabulation under uncertainty.** When lacking a grounded answer, the model generates a plausible one. It lacks the human reflex to flag "I don't know."
4. **[[jagged-intelligence|Jagged performance]].** PhD-level one moment, 9.11 > 9.9 the next. No meta-cognitive reliability.
5. **Pattern lock-in / [[model-collapse|collapse]].** Repeated fine-tuning on own outputs narrows the distribution.
6. **[[ai-psychosis|Psychosis]] under long runs.** Confident drift, no self-correction, amplification of its own errors.
7. **No sense of time or causality of its own state.** A model doesn't know which of its weights came from which update, or why its last answer was wrong.

## Why the list matters

These deficits are what the product stack has to absorb:

- [[partial-autonomy-apps]] make them visible (diffs, citations, fast verification).
- [[autonomy-slider]] adjusts risk per task because deficits are non-uniform.
- [[march-of-nines]] is the long-run response: each deficit is a nine.

## Contrast with human deficits

Humans forget too, hallucinate too, get confident too. The difference is that human cognitive deficits are *correlated with tiredness, domain, emotional state* — we have theories about them. LLM deficits are **uncorrelated with anything the model can introspect on.** A model can't tell you when it's about to confabulate.

## Related

- [[animals-vs-ghosts]]
- [[people-spirits]]
- [[ai-psychosis]]
- [[jagged-intelligence]]
- [[model-collapse]]
