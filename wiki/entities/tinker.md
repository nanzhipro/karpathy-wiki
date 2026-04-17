---
title: Tinker
type: entity
created: 2026-04-18
updated: 2026-04-18
sources: [2025/10.19.md]
tags: [product, fine-tuning, thinking-machines]
---

# Tinker

Thinking Machines Lab's fine-tuning product, referenced by Karpathy in the [[karpathy-x-2025-dwarkesh-recap|Oct 19 2025]] Dwarkesh recap as an example of **the right shape for fine-tuning infrastructure** in the agentic era.

## What it offers

Hosted fine-tuning — LoRA and full-weight — over open-weight base models. Exposes a clean API so developers can ship custom fine-tunes without running GPU clusters.

## Why Karpathy flags it

- **Good ergonomics match agentic workflows.** Spinning up a fine-tune is now closer to "call an API" than "manage a training run."
- **Open-weight ecosystem needs this.** For open models to be useful beyond research, fine-tuning has to be push-button.
- **LoRA slot model fits [[cognitive-core]].** A small core + swappable LoRAs is exactly what Tinker makes practical.

## Related

- [[cognitive-core]]
- [[dwarkesh-patel]]
- [[byoai]]
