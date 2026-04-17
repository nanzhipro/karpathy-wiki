---
title: Vibe Coding
type: concept
created: 2026-04-17
updated: 2026-04-18
sources: [andrej-karpathy-software-is-changing-again/transcript.md, 2025/4.22.md, 2025/11.23.md, 2025/12.27.md]
tags: [software-3-0, coding, karpathy-coinage]
---

# Vibe Coding

Karpathy's viral X-post coinage (early 2025): building software by describing what you want in natural language and letting an LLM emit the code, accepting imperfections on vibes rather than rigor. By the time of [[software-is-changing-again]] it's a Wikipedia entry and a term Tom Wolf of [[hugging-face|Hugging Face]] uses in front of high schoolers.

## 2025 arc

- **Apr 22** — [[karpathy-x-2025-build-for-agents|MenuGen blog post]] formalizes the "vibe code → DevOps crunch" pipeline.
- **Nov 23** — [[llm-council]] project published as a vibe-coded multi-model orchestration app.
- **Dec 27** — "[[karpathy-x-2025-ai-assisted-coding|I've never felt this much behind]]" post: vibe-coding culture has accelerated past the point any single practitioner can keep up, now a community phenomenon.
- By 2026 the term is partially superseded by [[agentic-engineering]] as the disciplined sibling.

## Source

[Karpathy, Software Is Changing (Again)](../sources/software-is-changing-again.md) — the YC keynote formalizes the frame and applies it to Karpathy's own weekend project [[menugen|MenuGen]].

## The non-obvious finding

Writing the code is the easy part. The hard part is the **DevOps of making it real**:

- Apple Developer IDs and provisioning
- Vercel / hosting configs
- Payments integrations (Stripe, etc.)
- Google Auth / OAuth wiring
- Domain and SSL setup

Karpathy's MenuGen — a weekend vibe-coded app — took **a week** to actually ship, with "most of it not being coding." The democratization story ("anyone can build apps") runs into the reality that production software is 90% plumbing.

## Product implication

- Vibe coding creates a huge class of prototypes that need the plumbing removed. Likely next product category: vibe-coded-app-to-production pipelines.
- The DevOps crunch is the real moat of the Software 3.0 era, not code generation itself.

## Related

- [[software-3-0]] — the paradigm vibe coding belongs to
- [[menugen]] — Karpathy's personal demo
- [[build-for-agents]] — the inverse problem: make infrastructure easy for machines to use
