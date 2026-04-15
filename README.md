# karpathy-wiki

A research wiki built from Andrej Karpathy's X posts and talks. The goal of this repository is to study Karpathy by building a knowledge base around his ideas, then distill his worldview, methods, and recurring patterns.

The project follows Karpathy's [LLM Wiki](https://karpathy.ai/) pattern: an LLM-maintained, incrementally-compiled knowledge base grounded in primary-source notes and references.

Sources live in `raw/` (immutable). The wiki is written and curated by an LLM agent per the protocol in [`CLAUDE.md`](CLAUDE.md).

## Start here

- [**Overview**](wiki/overview.md) — current themes and open questions
- [**Index**](wiki/index.md) — catalog of all pages (sources, concepts, entities, methods)
- [**Log**](wiki/log.md) — chronological record of every ingest and edit
- [**CLAUDE.md**](CLAUDE.md) — the agent's operating protocol

## Layout

```
raw/     source documents (read-only)
wiki/    LLM-maintained pages
CLAUDE.md  agent instructions
```

Scaffolded with [`llm-wiki-bootstrap`](https://github.com/anthropics/claude-code).
