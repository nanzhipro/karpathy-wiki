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

## [2026-04-17] ingest | Karpathy X posts 2026 — FSD Coast-to-Coast
- Source: raw/2026/1.1.md
- Summary: wiki/sources/karpathy-x-2026-fsd-coast-to-coast.md
- Updated: wiki/concepts/march-of-nines.md, wiki/entities/tesla-autopilot.md, wiki/entities/tesla.md
- Contradictions: none

## [2026-04-17] ingest | Karpathy X posts 2026 — nanochat & GPT-2 Reproduction
- Sources: raw/2026/1.8.md, 1.29.md, 2.2.md
- Summary: wiki/sources/karpathy-x-2026-nanochat-gpt2-reproduction.md
- Updated: wiki/entities/nanochat.md
- New pages: wiki/entities/modded-nanogpt.md
- Contradictions: none

## [2026-04-17] ingest | Karpathy X posts 2026 — Claude Coding Reflections
- Source: raw/2026/1.27.md
- Summary: wiki/sources/karpathy-x-2026-claude-coding-reflections.md
- Updated: wiki/entities/claude-code.md, wiki/concepts/vibe-coding.md, wiki/concepts/build-for-agents.md
- New pages: wiki/concepts/atrophy.md, wiki/concepts/10x-engineer.md
- Contradictions: none

## [2026-04-17] ingest | Karpathy X posts 2026 — Agentic Engineering
- Sources: raw/2026/2.5.md, 2.25.md
- Summary: wiki/sources/karpathy-x-2026-agentic-engineering.md
- New pages: wiki/concepts/agentic-engineering.md, wiki/concepts/slopacolypse.md
- Contradictions: Karpathy pivots "vibe coding" → "agentic engineering" as primary frame — flagged in wiki/concepts/vibe-coding.md

## [2026-04-17] ingest | Karpathy X posts 2026 — Malleable Software
- Sources: raw/2026/2.12.md, 2.17.md, 2.20.md, 2.21.md
- Summary: wiki/sources/karpathy-x-2026-malleable-software.md
- New pages: wiki/concepts/bacterial-code.md, wiki/concepts/app-store-outdated.md, wiki/entities/microgpt.md, wiki/entities/deepwiki.md, wiki/entities/matx.md
- Contradictions: none

## [2026-04-17] ingest | Karpathy X posts 2026 — Agent Networks
- Sources: raw/2026/2.4.md, 2.13.md
- Summary: wiki/sources/karpathy-x-2026-agent-networks.md
- New pages: wiki/entities/simile-ai.md, wiki/concepts/org-code.md
- Contradictions: none

## [2026-04-17] ingest | Karpathy X posts 2026 — autoresearch & Claws
- Sources: raw/2026/2.26.md, 2.28.md, 3.6.md, 3.8.md, 3.9.md, 3.10.md, 3.11.md, 3.12.md, 3.20.md
- Summary: wiki/sources/karpathy-x-2026-autoresearch-and-claws.md
- New pages: wiki/concepts/claws.md, wiki/concepts/autoresearch.md, wiki/concepts/intelligence-brownouts.md, wiki/entities/autoresearch.md, wiki/entities/nanoclaw.md
- Contradictions: none

## [2026-04-17] ingest | Karpathy X posts 2026 — Supply Chain Attacks
- Sources: raw/2026/3.19.md, 3.31.md
- Summary: wiki/sources/karpathy-x-2026-supply-chain.md
- New pages: wiki/concepts/supply-chain-attacks.md
- Updated: wiki/concepts/bacterial-code.md (stronger "Why this matters in 2026" section)
- Contradictions: none

## [2026-04-17] ingest | Karpathy X posts 2026 — LLM Knowledge Bases & BYOAI
- Sources: raw/2026/4.3.md, 4.5.md
- Summary: wiki/sources/karpathy-x-2026-llm-wiki.md
- New pages: wiki/concepts/llm-knowledge-bases.md, wiki/concepts/byoai.md, wiki/concepts/government-legibility.md
- Note: karpathy-wiki itself is an instance of the LLM Knowledge Base pattern described Apr 3 / Apr 5.
- Contradictions: none

## [2026-04-17] ingest | Karpathy X posts 2026 — Miscellaneous
- Sources: raw/2026/1.7.md, 1.31.md, 2.1.md, 3.25.md, 3.27.md, 3.28.md
- Summary: wiki/sources/karpathy-x-2026-misc.md
- Updated: wiki/concepts/ai-psychosis.md (memory-overfit note)
- Contradictions: none

## [2026-04-17] ingest | Andrej Karpathy self-bio (karpathy.ai)
- Source: raw/Andrej Karpathy.md
- Summary: merged directly into wiki/entities/andrej-karpathy.md (no new source page — it is a bio reference)
- Updated: wiki/entities/andrej-karpathy.md (added verified career-date table, CS231n growth numbers, internship list, advisers)
- Contradictions: none

## [2026-04-17] bulk-update | index.md reflow
- Added: 10 source pages, 7 entity pages (autoresearch, deepwiki, matx, microgpt, modded-nanogpt, nanoclaw, simile-ai), 14 concept pages (10x-engineer, agentic-engineering, app-store-outdated, atrophy, autoresearch, bacterial-code, byoai, claws, government-legibility, intelligence-brownouts, llm-knowledge-bases, org-code, slopacolypse, supply-chain-attacks)
- Source counts updated across: andrej-karpathy (10+), claude-code (3), cursor (2), github (3), cs231n (2), nanochat (5), tesla (3), tesla-autopilot (3), modded-nanogpt (3), openai-codex (3), model-context-protocol (2), march-of-nines (3), nanogpt (3), vibe-coding (2), build-for-agents (2), agentic-engineering (4), bacterial-code (3), claws (2), autoresearch (3), supply-chain-attacks (3), app-store-outdated (2), atrophy (2), slopacolypse (2), org-code (2), 10x-engineer (3)
