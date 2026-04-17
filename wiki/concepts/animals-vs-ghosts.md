---
title: Animals vs Ghosts
type: concept
created: 2026-04-17
updated: 2026-04-18
sources: [andrej-karpathy-were-summoning-ghosts-not-building-animals/transcript.md, 2025/10.2.md, 2025/11.22.md, 2025/12.8.md]
tags: [llm-psychology, agi, karpathy-coinage]
---

# Animals vs Ghosts

Karpathy's frame for the category error in comparing LLMs to biological intelligence. **Animals** arrive with billions of years of evolved, packaged hardware — instincts, body, motor control, species-specific priors. **Ghosts** are digital entities summoned by imitation of human text; they have no embodiment, no evolved instincts, and a different failure surface.

## Sources

- [Karpathy, Summoning Ghosts](../sources/summoning-ghosts-not-animals.md) — the podcast the frame is drawn from.
- [[karpathy-x-2025-ghosts-and-psychology|Oct 2 / Nov 22 / Dec 8 2025 X posts]] — Karpathy defends and refines the frame against pure-RL partisans (implicitly [[richard-sutton|Sutton]]): *we are not trying to build animals; we are summoning ghosts, and the engineering target is different.*

## The distinction

| Axis | Animal | Ghost (LLM) |
|------|--------|-------------|
| Origin | Evolution | Imitation of humans on internet text |
| Embodiment | Yes — body, sensors, motor loop | No — text in, text out |
| Priors | Species-level instinct, reflex | Statistical patterns from training data |
| Failure mode | Species-typical (hunger, fear, fatigue) | [[ai-psychosis\|Psychosis]], [[model-collapse\|collapse]], hallucination |
| Reward signal | Dense, multi-channel, evolved | Sparse, text-based, hand-engineered |

## Why it matters

- Building AGI by imitating biology (the "animal path") is not what's happening. We're not recreating zebras or octopi. We're summoning something with a different phenotype.
- [[people-spirits]] is the companion frame: ghosts are specifically *people-shaped* because they were trained on human output.
- Evaluations designed for animals (ARC-AGI-style physical reasoning, embodied tests) don't cleanly apply. Evaluations designed for people (exams, coding problems) fit better but expose [[jagged-intelligence|jagged]] performance.

## Implications

- Don't expect LLMs to develop self-preservation, hunger, or biological drives spontaneously. They won't — those aren't in the training distribution.
- Do expect [[llm-cognitive-deficits|cognitive deficits]] that no animal has: memory with no persistence across runs, confabulation under uncertainty, pattern collapse under self-consumption.
- The path to reliability runs through engineering ghost-specific infrastructure (context, tools, memory, verification), not through biological mimicry.

## Related

- [[people-spirits]]
- [[ai-psychosis]]
- [[model-collapse]]
- [[llm-cognitive-deficits]]
- [[cognitive-core]]
