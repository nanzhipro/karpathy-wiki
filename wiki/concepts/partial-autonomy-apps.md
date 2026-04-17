---
title: Partial-Autonomy Apps
type: concept
created: 2026-04-17
updated: 2026-04-17
sources: [andrej-karpathy-software-is-changing-again/transcript.md]
tags: [product, llm, ux, karpathy]
---

# Partial-Autonomy Apps

Karpathy's proposed product shape for the LLM era: a domain app that wraps frontier model calls with a custom UI and an [[autonomy-slider]], so humans stay in the verification loop while the model does the generation.

## Source

[Karpathy, Software Is Changing (Again)](../sources/software-is-changing-again.md) — the talk's central product recommendation.

## Canonical examples

- **[[cursor|Cursor]]** — coding. Tab-completion → inline edit → composer → agent-mode. Diffs make verification fast.
- **[[perplexity|Perplexity]]** — research. Answer with citations → multi-step research → deep agent investigation.

## Shared properties

1. **Domain UI, not raw chat.** The model is the engine, not the product surface.
2. **Fast human verification.** GUIs beat text for auditing; diffs > prose; citations > free-form answers.
3. **[[autonomy-slider|Autonomy slider]].** Users dial in how much rope to give the model per task; defaults sit low.
4. **Task-narrow.** Each app is good at a specific thing. Generality is the OS's job ([[llm-os]]), not the app's.

## Why this shape wins (for now)

- LLMs are [[people-spirits]] with [[jagged-intelligence]] — products must surface failures, not hide them.
- The [[march-of-nines]] means full autonomy is a decade away; the path there runs through slider-controlled partial autonomy.
- [[iron-man-analogy|Iron Man suits beat Iron Man robots]].

## Related

- [[autonomy-slider]]
- [[iron-man-analogy]]
- [[cursor]], [[perplexity]]
- [[march-of-nines]]
