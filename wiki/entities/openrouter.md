---
title: OpenRouter
type: entity
created: 2026-04-18
updated: 2026-04-18
sources: [2025/8.29.md]
tags: [platform, llm-routing, evals]
---

# OpenRouter

API aggregator for LLM providers. Referenced by Karpathy in [[karpathy-x-2025-evals-and-model-vibes|Aug 29 2025]] for its **usage-based model rankings** — a harder-to-game signal than leaderboard benchmarks.

## What it is

A single API endpoint that routes to every major LLM (OpenAI, Anthropic, Google, DeepSeek, Mistral, open-weight models via inference providers). Users pay through OpenRouter; OpenRouter publishes aggregate token usage per model.

## Why Karpathy highlights it

In a year of **[[karpathy-x-2025-evals-and-model-vibes|leaderboard illusion]]** — where headline benchmark scores had decoupled from real-world quality — the OpenRouter rankings offered a corrective:

> Which models do developers actually send tokens to when they're paying per token?

That's a revealed-preference signal — noisier but harder to game than a benchmark.

## Caveats

- Biased toward coding and developer workloads (its user base).
- Doesn't capture in-house API direct users (ChatGPT, Claude.ai, Gemini native apps).
- Still suggestive rather than definitive.

## Related

- [[karpathy-x-2025-evals-and-model-vibes|Leaderboard illusion]]
- [[verification-gap]]
