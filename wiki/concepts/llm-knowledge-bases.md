---
title: LLM Knowledge Bases
type: concept
created: 2026-04-17
updated: 2026-04-17
sources: [2026/4.3.md, 2026/4.5.md]
tags: [knowledge-base, personalization, karpathy-coinage]
---

# LLM Knowledge Bases

Karpathy's Apr 3 2026 formulation of a personal workflow: **use an LLM to compile, maintain, and query a file-based knowledge base** from your own source materials. Obsidian-style markdown wikis, but the LLM is the author.

**Note:** this wiki (karpathy-wiki) is itself an instance of this pattern.

## The workflow

1. **Raw data** into `raw/` — articles, papers, repos, datasets, images.
2. **Compiled wiki** in `.md` files — summaries, backlinks, concept pages, category indexes, all LLM-authored.
3. **IDE = Obsidian** — read raw data, compiled wiki, and derived visualizations (Marp slides, matplotlib images).
4. **Q&A against the wiki** — at ~400K words / ~100 articles, no fancy RAG needed; the LLM auto-maintains index files and navigates.
5. **Outputs file back** — queries produce markdown/slides/images that return to the wiki.
6. **Lint** — LLM health-checks for inconsistencies, missing data, new article candidates.
7. **Extras** — a vibe-coded search engine over the wiki, usable as CLI tool for agents.

> "As the repo grows, the natural desire is to also think about synthetic data generation + finetuning to have your LLM 'know' the data in its weights instead of just context windows."

## Why this shape

See [[byoai]] for the four philosophical properties: **Explicit, Yours, File-over-app, BYOAI.**

## Quiet architectural properties

- **No vendor lock-in.** Markdown + images are portable. Any LLM can operate on them.
- **Audit-friendly.** Every claim is in a file you can read. Compare with opaque provider-side memory.
- **Composable with the Unix toolkit.** `grep`, `rg`, `find`, git, CLIs — all apply.
- **Minimal RAG complexity.** For sub-1M-word corpora, LLMs are good enough with plain directory walks.
- **Linting substitutes for synchronization.** Health-check passes replace "is my DB consistent?" maintenance.

## Why it resists the [[slopacolypse]]

The KB is **source-anchored** (every summary has a canonical `raw/` file behind it), so it's robust to LLM-generated noise. Karpathy's pedagogy is visible here: a KB with intact provenance is a form of [[bacterial-code|bacterial code]] for knowledge — rippable, auditable, contextualized.

## The idea-file corollary (Apr 5)

Karpathy packages the KB idea as a gist rather than code:

> "In this era of LLM agents, there is less of a point/need of sharing the specific code/app, you just share the idea, then the other person's agent customizes & builds it for your specific needs."

Gist: `gist.github.com/karpathy/442a6bf555914893e9891c11519de94f`.

## Extensions Karpathy foreshadows

- **Personal fine-tunes.** Train an open-weights model on your KB so "knowing you" lives in weights, not context.
- **Synthetic data generation.** Use the KB to seed training data for domain-specific research agents.
- **Civic version.** Apply the KB workflow to public government data — legibility from the bottom up.

## Related

- [[byoai]]
- [[bacterial-code]]
- [[build-for-agents]]
- [[slopacolypse]]
- [[government-legibility]]
