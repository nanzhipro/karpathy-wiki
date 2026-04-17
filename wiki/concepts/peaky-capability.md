---
title: Peaky Capability
type: concept
created: 2026-04-15
updated: 2026-04-17
sources: [4.10.md, andrej-karpathy-software-is-changing-again/transcript.md, andrej-karpathy-were-summoning-ghosts-not-building-animals/transcript.md]
tags: [capability, evaluation]
---

# Peaky Capability

The observation that frontier AI capability is **not uniform** across tasks — it spikes dramatically in some domains while remaining flat or embarrassing in others. Karpathy's later coinage **[[jagged-intelligence]]** names the same pattern at the task level (a model that solves a PhD-quality problem and then insists 9.11 > 9.9).

## Definitions across sources

- [Karpathy, AI Capability Gap](../sources/ai-capability-gap.md) — "a lot of the capabilities are relatively 'peaky' in highly technical areas. Typical queries around search, writing, advice, etc. are *not* the domain that has made the most noticeable and dramatic strides in capability."
- [Karpathy, Software Is Changing (Again)](../sources/software-is-changing-again.md) — reintroduced as **jagged intelligence**: "PhD-level problem solving on one request, and then insisting 9.11 is greater than 9.9 on the next."
- [Karpathy, Summoning Ghosts](../sources/summoning-ghosts-not-animals.md) — frames the peak as a *distillation* artifact: LLMs are shaped by imitation of human text, inheriting the shape of the training distribution rather than a generalist reasoning core. Implies the peak will persist until there's a [[cognitive-core]].

## Karpathy's causal story for the peak

1. **[[verifiable-rewards]]** — technical domains have mechanical reward signals that suit [[reinforcement-learning]].
2. **B2B value concentration** — these domains are where the money is, so the biggest fraction of frontier research teams focuses there.
3. **(New in 2025)** Models are distilled human text, not reasoning cores — the shape of the peak reflects what humans wrote most of.

## Observed manifestations

| Domain | Capability signal |
|--------|------------------|
| Programming (agentic, hour-long tasks) | Very strong — "melting" problems. See [[openai-codex]], [[claude-code]]. |
| Math, research | Very strong (asserted) |
| Personal advice ("should I walk or drive?") | Weak — viral failure examples |
| Writing | Weak — hard to judge with verifiable rewards |
| Arithmetic reliability (9.11 vs 9.9) | Jagged — sporadic trivial failures inside strong overall performance |

## Related

- [[jagged-intelligence]] — Karpathy's 2025 renaming / task-level framing
- [[ai-psychosis]] — the perceptual gap this peak creates between casual and professional users
- [[agentic-models]] — where the peak is most visible today
- [[cognitive-core]] — proposed architectural response (Dwarkesh 2025)
