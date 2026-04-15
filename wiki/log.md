# Log

> Append-only chronological record of all wiki operations.
> Each entry: `## [YYYY-MM-DD] operation | subject`
> Parse with: `grep "^## \[" wiki/log.md | tail -10`

## [2026-04-15] init | Wiki Created
- Scaffolded by llm-wiki-bootstrap
- Domain: Research on Andrej Karpathy's X posts, talks, and related source materials on neural networks, LLMs, and deep learning
- Source types: Web articles, PDFs / papers, Meeting notes / transcripts, Personal notes / journals
- Schema: CLAUDE.md
- Editor: Obsidian

## [2026-04-15] ingest | The Growing Gap in Understanding AI Capability
- Source: raw/4.10.md (Karpathy X post, 4/10)
- Summary: wiki/sources/ai-capability-gap.md
- New pages:
  - wiki/entities/andrej-karpathy.md
  - wiki/entities/openai-codex.md
  - wiki/entities/claude-code.md
  - wiki/concepts/agentic-models.md
  - wiki/concepts/verifiable-rewards.md
  - wiki/concepts/peaky-capability.md
  - wiki/concepts/ai-psychosis.md
  - wiki/methods/reinforcement-learning.md
- Updated: wiki/index.md, wiki/overview.md
- Contradictions: none (first substantive source)
