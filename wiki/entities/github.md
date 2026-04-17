---
title: GitHub
type: entity
created: 2026-04-17
updated: 2026-04-17
sources: [andrej-karpathy-software-is-changing-again/transcript.md, andrej-karpathy-gpu-mode-irl-2024-keynote/transcript.md]
tags: [platform, code-hosting]
---

# GitHub

The dominant code-hosting platform. Appears across the Karpathy corpus as (a) the distribution channel for his own pedagogical projects, and (b) the target of agent-native tooling like `gitingest` and the `llm.txt` pitch.

## In the corpus

- **YC talk** — GitHub is repeatedly used as the example of infrastructure that was built for humans and which now needs to be rethought for agent consumption (gitingest flattens repos for LLMs; MCP servers expose repo data; etc.).
- **GPU MODE talk** — [[llm-c]], [[nanogpt]], [[micrograd]], [[nanochat]] all live on GitHub; Karpathy's pedagogy is expressed through small, readable public repos.

## Why it matters

- GitHub is where [[snowballs|snowballs]] live. The reason a two-file project can compound into reputation is that GitHub gives it a URL and an issue tracker.
- It's also a **prime example of [[build-for-agents]]**: the UI is optimized for browsing humans, not for LLMs, which is why wrapper tools exist.

## Related

- [[build-for-agents]]
- [[llm-c]], [[nanogpt]], [[micrograd]], [[nanochat]]
- [[snowballs]]
