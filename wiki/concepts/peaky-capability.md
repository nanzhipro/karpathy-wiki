---
title: Peaky Capability
type: concept
created: 2026-04-15
updated: 2026-04-15
sources: [4.10.md]
tags: [capability, evaluation]
---

# Peaky Capability

The observation that frontier AI capability is **not uniform** across tasks — it spikes dramatically in some domains while remaining flat or embarrassing in others.

## Definition from source

- [Karpathy, "AI Capability Gap"](../sources/ai-capability-gap.md) — "a lot of the capabilities are relatively 'peaky' in highly technical areas. Typical queries around search, writing, advice, etc. are *not* the domain that has made the most noticeable and dramatic strides in capability."

## Karpathy's causal story for the peak

1. **[[verifiable-rewards]]** — technical domains have mechanical reward signals that suit [[reinforcement-learning]].
2. **B2B value concentration** — these domains are where the money is, so the biggest fraction of frontier research teams focuses there. (Not prioritized: search, writing, personal advice.)

## Observed manifestations

| Domain | Capability signal |
|--------|------------------|
| Programming (agentic, hour-long tasks) | Very strong — "melting" problems. See [[openai-codex]], [[claude-code]]. |
| Math, research | Very strong (asserted) |
| Personal advice ("should I walk or drive?") | Weak — viral failure examples |
| Writing | Weak — hard to judge with verifiable rewards |

## Related

- [[ai-psychosis]] — the perceptual gap this peak creates between casual and professional users
- [[agentic-models]] — where the peak is most visible today
