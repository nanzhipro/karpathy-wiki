---
title: "2026-01 / 02 — nanochat GPT-2 Reproduction & Scaling Laws"
type: source-summary
created: 2026-04-17
updated: 2026-04-17
sources: [2026/1.8.md, 2026/1.29.md, 2026/2.2.md]
tags: [nanochat, scaling-laws, gpt-2, karpathy, systems]
---

# 2026-01 / 02 — nanochat GPT-2 Reproduction & Scaling Laws

## Sources

Three connected X posts tracking Karpathy's iterative cost-collapse of a GPT-2-grade LLM inside [[nanochat]].

- **Jan 8** — *nanochat miniseries v1* (scaling-law replication of Chinchilla).
- **Jan 29** — *<<$100 GPT-2* (600× cost reduction over 7 years).
- **Feb 2** — *fp8 speedup* (~$20 on spot H100s; "GPT-2 new MNIST").

## Core claim

> "The correct way to think about LLMs is that you are not optimizing for a single specific model but for a family of models controlled by a single dial (the compute you wish to spend) to achieve monotonically better results."

This is Karpathy's pedagogical restatement of Chinchilla-style scaling laws as a product principle.

## Key numbers

| Milestone | Time / cost | Hardware |
|-----------|-------------|----------|
| 2019 GPT-2 OpenAI | 168 h, ~$43,000 | 32× TPUv3 |
| Jan 2026 nanochat | 3.04 h, ~$73 | 1× 8×H100 node |
| Feb 2026 nanochat fp8 | 2.91 h, ~$20 spot | 1× 8×H100 node |

**Cost reduction: ~600× over 7 years ≈ 2.5× per year.** Karpathy thinks this is a low-ball estimate.

## Scaling-law findings on nanochat

- Reproduces Chinchilla-shape plots.
- Fitted exponents on parameters N and tokens D are both ≈0.5.
- Chinchilla's N/D ratio constant ≈ 20; **nanochat's is ~8** — smaller models + longer training give the best FLOPs-optimal frontier in this regime.
- Cost of the full miniseries: ~$100 / ~4 h on 8×H100.

## Winning components (per Karpathy)

- Flash Attention 3 kernels (+ window_size for alternating patterns)
- Muon optimizer (tried to remove, couldn't)
- Residual pathways + skip connections gated by learnable scalars
- Value embeddings
- fp8 training with **tensorwise** scaling (rowwise lagged)

## Caveats on fp8

- Paper headlines (~2× FLOPS, ~25% speedup on Llama3-8B) don't materialize at nanochat scale.
- Observed real speedup: ~5–7%, partly because GEMMs are too small at this scale.
- Scale conversions eat overhead; per-step quality drops; net speedup came from longer training horizons.

## Quotable

> "GPT-2 (7 years ago): too dangerous to release. GPT-2 (today): new MNIST! :)"

## Connection to [[modded-nanogpt]]

Many of the ingredients came from the modded-nanogpt community repo; [[nanochat]] is adopting its tricks and will host a public **"Time to GPT-2" leaderboard** to keep the iteration open.

## Related pages

- [[nanochat]]
- [[modded-nanogpt]]
- [[software-3-0]]
- [[llm-c]] — the engineering antecedent
