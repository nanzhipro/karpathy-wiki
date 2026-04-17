---
title: HN Time Capsule
type: entity
created: 2026-04-18
updated: 2026-04-18
sources: [2025/12.11.md]
tags: [karpathy-project, evals, vibe-coded]
---

# HN Time Capsule

Karpathy's [[karpathy-x-2025-llm-reading|Dec 11 2025]] side project: **930 Hacker News front-page posts from December 2015**, re-graded a decade later by GPT-5.1 Thinking.

## What it does

For each 2015 HN submission, GPT-5.1 evaluates what actually happened to the claim, product, or prediction — how well it aged, what it got right/wrong, whether the referenced company/tech survived.

A built-in evaluator for "how well do confident internet takes hold up?" that only becomes possible once:
1. You have ten years of ground truth (which HN does), **and**
2. You have a model patient enough to judge 930 posts (which [[rlvr|reasoning models]] are).

## Why it's interesting

- **Cheap retrospective at scale.** Hand-grading 930 posts was always feasible but never worth it. LLMs flip the calculus.
- **Vibe-coded artifact.** Fits the [[code-post-scarcity]] thesis — a one-off app that exists because it's now cheap to make.
- **Evaluator pattern for the future.** "Re-grade old predictions years later" generalizes to research papers, industry analyst reports, policy predictions.

## Related

- [[reader3]]
- [[code-post-scarcity]]
- [[galaxy-brain-reasoning]]
- [[andrej-karpathy]]
