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

## [2026-04-17] ingest | Software Is Changing (Again) — YC AI Startup School Keynote
- Source: raw/youtube-transcript/andrej-karpathy-software-is-changing-again/transcript.md
- Summary: wiki/sources/software-is-changing-again.md
- Updated:
  - wiki/entities/andrej-karpathy.md (fully rewritten as hub page)
  - wiki/entities/claude-code.md
  - wiki/entities/openai-codex.md
- New pages:
  - wiki/concepts/software-3-0.md
  - wiki/concepts/llm-os.md
  - wiki/concepts/people-spirits.md
  - wiki/concepts/jagged-intelligence.md
  - wiki/concepts/partial-autonomy-apps.md
  - wiki/concepts/autonomy-slider.md
  - wiki/concepts/vibe-coding.md
  - wiki/concepts/iron-man-analogy.md
  - wiki/concepts/build-for-agents.md
  - wiki/entities/openai.md
  - wiki/entities/cursor.md
  - wiki/entities/perplexity.md
  - wiki/entities/tesla.md
  - wiki/entities/tesla-autopilot.md
  - wiki/entities/hugging-face.md
  - wiki/entities/menugen.md
  - wiki/entities/model-context-protocol.md
  - wiki/entities/llama.md
- Contradictions: YC talk places current LLM era at "1960s of computing"; Berkeley 2024 keynote places it at "1980s." Flagged in wiki/concepts/llm-os.md.

## [2026-04-17] ingest | We're Summoning Ghosts, Not Building Animals — Dwarkesh Interview
- Source: raw/youtube-transcript/andrej-karpathy-were-summoning-ghosts-not-building-animals/transcript.md
- Summary: wiki/sources/summoning-ghosts-not-animals.md
- Updated:
  - wiki/concepts/peaky-capability.md
  - wiki/concepts/verifiable-rewards.md
  - wiki/concepts/ai-psychosis.md
  - wiki/concepts/agentic-models.md
  - wiki/methods/reinforcement-learning.md
- New pages:
  - wiki/concepts/animals-vs-ghosts.md
  - wiki/concepts/cognitive-core.md
  - wiki/concepts/march-of-nines.md
  - wiki/concepts/decade-of-agents.md
  - wiki/concepts/rl-is-terrible.md
  - wiki/concepts/model-collapse.md
  - wiki/concepts/llm-cognitive-deficits.md
  - wiki/concepts/in-context-learning.md
  - wiki/concepts/agi-blends-into-2-percent-growth.md
  - wiki/entities/dwarkesh-patel.md
  - wiki/entities/waymo.md
  - wiki/entities/eureka.md
  - wiki/entities/deepseek-v3-2.md
- Contradictions: none new; Tesla/Waymo contrast now articulated as complementary priors rather than competing claims.

## [2026-04-17] ingest | Berkeley SkyDeck AI Hackathon 2024 — Keynote
- Source: raw/youtube-transcript/andrej-karpathy-berkeley-ai-hackathon-2024-keynote/transcript.md
- Summary: wiki/sources/berkeley-ai-hackathon-2024-keynote.md
- New pages:
  - wiki/concepts/feel-the-agi.md
  - wiki/concepts/snowballs.md
  - wiki/concepts/10000-hours.md
  - wiki/concepts/ramps-to-knowledge.md
  - wiki/entities/cs231n.md
  - wiki/entities/zero-to-hero.md
  - wiki/entities/llm101n.md
  - wiki/entities/awesomemovies-life.md
- Contradictions: "1980s of computing" framing here vs. "1960s" in YC 2025 talk — noted in wiki/concepts/llm-os.md as reflecting the speed of reframing in Karpathy's own thinking.

## [2026-04-17] ingest | GPU MODE IRL 2024 — Karpathy on llm.c
- Source: raw/youtube-transcript/andrej-karpathy-gpu-mode-irl-2024-keynote/transcript.md
- Summary: wiki/sources/gpu-mode-irl-2024-keynote.md
- New pages:
  - wiki/entities/llm-c.md
  - wiki/entities/micrograd.md
  - wiki/entities/nanogpt.md
  - wiki/entities/nanochat.md
  - wiki/entities/pytorch.md
  - wiki/entities/github.md
- Contradictions: none (llm.c is a systems topic with few overlapping claims to the other sources).

## [2026-04-17] bulk-update | index.md reflow
- Added: 5 sources, 23 entities, 22 concepts (alphabetically sorted)
- Methods source count: reinforcement-learning → 2
- No content changes to existing pages beyond cross-reference backfills
