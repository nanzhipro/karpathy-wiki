---
title: Government Legibility
type: concept
created: 2026-04-17
updated: 2026-04-17
sources: [2026/4.5.md]
tags: [civic, llms, karpathy]
---

# Government Legibility

Karpathy's **Apr 5 2026** extension of the [[llm-knowledge-bases|LLM knowledge-base]] workflow to public institutions: **apply the same markdown-wiki-plus-LLM stack to government data** — laws, budgets, meeting transcripts, regulatory filings — so citizens can actually read and query what their government does.

## The pitch

Governments already publish vast amounts of text. What they don't publish is a *legible* index: summaries, cross-links, version diffs, plain-language explanations, claim-tracking. Build that as a public wiki, compile it with an LLM agent, query it with [[byoai|whatever model you trust]].

## Why this fits Karpathy's 2026 stack

- **File-over-app.** Markdown + Unix toolkit = durable, forkable, non-captured.
- **BYOAI.** Inspection power isn't locked to a single provider.
- **[[bacterial-code]]** for civic data — rippable, independently auditable.
- **[[slopacolypse]] resistant.** Source-anchored summaries with `raw/` provenance.

## Karpathy's framing

> Explicit. Yours. Universal format. Swappable AI. Apply to government, and the citizen has the same leverage over public information that the knowledge-base owner has over personal information.

## Related

- [[llm-knowledge-bases]]
- [[byoai]]
- [[bacterial-code]]
- [[slopacolypse]]
