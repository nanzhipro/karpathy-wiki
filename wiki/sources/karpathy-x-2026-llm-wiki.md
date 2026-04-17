---
title: "2026-04-03 & 04-05 — LLM Knowledge Bases"
type: source-summary
created: 2026-04-17
updated: 2026-04-17
sources: [2026/4.3.md, 2026/4.5.md]
tags: [knowledge-base, personalization, byoai, karpathy]
---

# 2026-04 — LLM Knowledge Bases

Two posts that together describe Karpathy's personal workflow for using LLMs to **compile and maintain knowledge bases**, and the broader "BYOAI" philosophy behind it.

**Direct relevance: this wiki (karpathy-wiki) is itself an instance of the pattern Karpathy describes here.**

## Sources

- **Apr 3** — *LLM Knowledge Bases* — the workflow description.
- **Apr 5** — The idea file + BYOAI + government legibility thread.

## The workflow (Apr 3)

### Data ingest

- Source documents (articles, papers, repos, datasets, images) indexed into a **`raw/`** directory.
- LLM incrementally **"compiles" a wiki** — a collection of `.md` files organized by topic.
- Includes: summaries of everything in `raw/`, backlinks, category pages, articles.
- Web articles ingested via Obsidian Web Clipper; a hotkey downloads linked images locally.

### IDE

- Obsidian is the "frontend": view raw data, compiled wiki, derived visualizations.
- LLM writes and maintains the wiki; Karpathy rarely edits it directly.
- Plugins like Marp render slides from the same markdown.

### Q&A

- Once the wiki is ~100 articles / ~400K words, LLM can answer complex cross-document questions.
- **No fancy RAG needed** at that scale: LLM auto-maintains index files and brief summaries; reads the related data itself.

### Output

- Answers rendered as markdown, Marp slides, matplotlib images — all viewed in Obsidian.
- Outputs get filed back into the wiki, enhancing it for future queries. "My own explorations and queries always 'add up' in the knowledge base."

### Linting

- LLM health-checks the wiki for inconsistencies, missing data (with web search), new article candidates, integrity fixes.

### Extra tools

- A vibe-coded search engine over the wiki, usable both as a web UI and as a CLI tool for LLM agents.

### Further explorations

- Synthetic data generation + fine-tuning so the LLM "knows" the data *in weights*, not just context.

## The idea file (Apr 5)

Karpathy packages the wiki-LLM idea as a GitHub gist — intentionally abstract — to be handed to agents:

> "In this era of LLM agents, there is less of a point/need of sharing the specific code/app, you just share the idea, then the other person's agent customizes & builds it for your specific needs."

Repo: `gist.github.com/karpathy/442a6bf555914893e9891c11519de94f`

## BYOAI — four philosophical properties (Apr 5)

1. **Explicit.** The memory artifact is navigable and inspectable (the wiki itself).
2. **Yours.** Data on your local computer, not in an AI provider's system.
3. **File over app.** Universal formats (markdown, images) — the whole Unix toolkit applies.
4. **BYOAI.** Use any model you want over the same wiki: Claude, Codex, OpenCode, or a fine-tune of an open-weights model on your own wiki.

> "So this approach to personalization puts *you* in full control. The data is yours. In Universal formats. Explicit and inspectable."

## Government legibility (Apr 5, tangential)

Karpathy extends the pattern to civic data:

> "Historically, it is the governments that act to make society legible… but with AI, society can dramatically improve its ability to do this in reverse. Government accountability has not been constrained by access… it has been constrained by intelligence — the ability to process a lot of raw data, combine it with domain expertise and derive insights."

Examples: 4,000-page omnibus bills (nominally transparent, practically opaque), lobbying graphs, procurement and contracting, local-government decisions on zoning / policing / schools / utilities. He leans optimistic: "added participation, transparency and accountability will improve democratic, free societies."

## Why these two posts belong together (and are flagged for the wiki)

- They **describe the exact system this wiki uses**. The Karpathy-wiki was scaffolded via `llm-wiki-bootstrap`, following the pattern above almost literally.
- They formalize a **personal-data philosophy** that's complementary to the [[build-for-agents]] thesis — not just agents on APIs, but agents on *your own files*.
- BYOAI is a response to both the [[model-collapse]] worry (keep human-authored data in the loop) and the [[ai-psychosis]] worry (keep the context surface explicit and inspectable).

## Related

- [[llm-knowledge-bases]]
- [[byoai]]
- [[build-for-agents]]
- [[bacterial-code]]
- [[people-spirits]]
