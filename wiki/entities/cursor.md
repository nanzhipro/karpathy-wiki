---
title: Cursor
type: entity
created: 2026-04-17
updated: 2026-04-17
sources: [andrej-karpathy-software-is-changing-again/transcript.md]
tags: [product, ide, coding, partial-autonomy]
---

# Cursor

**Type:** Product — AI-augmented code editor (fork of VS Code).

## Relevance to this wiki

Karpathy's canonical example of a [[partial-autonomy-apps|partial-autonomy app]]. In [[software-is-changing-again]] he uses Cursor to illustrate:

- **LLM orchestration as feature, not implementation.** Cursor calls frontier models under the hood; the user experiences a coherent product.
- **[[autonomy-slider|Autonomy slider]].** Cursor's tab-complete → inline edit → composer → agent-mode is the paradigmatic slider: the user picks how much rope to give the model for each task.
- **Verification UI as the moat.** Diffs are human-auditable in seconds; this is why code is the frontier of [[software-3-0|Software 3.0]] before writing/advice catches up.

## Related

- [[perplexity]] — the parallel partial-autonomy example for research
- [[partial-autonomy-apps]], [[autonomy-slider]]
