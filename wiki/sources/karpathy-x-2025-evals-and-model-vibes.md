---
title: "2025 — Evals, Leaderboards & Model Vibes"
type: source-summary
created: 2026-04-17
updated: 2026-04-17
sources: [2025/4.30.md, 2025/8.29.md, 2025/11.19.md, 2025/11.23.md]
tags: [evals, benchmarks, model-vibes, leaderboard-illusion, llm-council]
---

# 2025 — Evals, Leaderboards & Model Vibes

Four posts across the year on *how to actually know if a model is good* — as the published benchmark ecosystem visibly decays.

## Apr 30 — The Leaderboard Illusion

Response to ["The Leaderboard Illusion"](https://arxiv.org/abs/2504.20879) — a paper looking at LM Arena ranking pathologies.

Karpathy's own priors-confirmation:

> "At one point a Gemini model scored #1 way above second best, but when I tried to switch for a few days it was worse than what I was used to. Conversely, Claude 3.5 was a top tier model in my personal use but it ranked very low on the arena."

Diagnosis: different labs place different internal focus on Arena scores. "They are not getting better models overall but better **LM Arena models**, whatever that is. Possibly something with a lot of nested lists, bullet points and emoji."

Alludes to Bezos: *"When the data and the anecdotes disagree, the anecdotes are usually right."*

### Proposed replacement: OpenRouter rankings

> "[@openrouter](https://openrouter.ai/rankings) allows people/companies to quickly switch APIs between LLM providers. All of them have real use cases (not toy problems), their own private evals, and direct incentive to get their choices right, so by choosing one LLM over another they are directly voting for **capability + cost**."

Not there yet on quantity/diversity, but structurally much harder to game than single-point human-preference rankings. → becomes a recurring reference throughout 2025 and 2026.

## Aug 29 — "LLMification" of textbooks

Less about evals than about **what a real training data stream should look like**:

> "Transforming human knowledge, sensors and actuators from human-first and human-legible to **LLM-first and LLM-legible** is a beautiful space with so much potential and so much can be done."

For each textbook PDF/epub, the ideal transformation:

- **Exposition** → markdown (LaTeX, tables, lists, figures as images).
- **Worked problems** → SFT examples.
- **Practice problems** → RL environments + answer keys for LLM judges.
- **Synthetic expansion** — infinite problem generators per template (e.g., "angle between clock hands at 9am" → any arbitrary time).
- **Indexed + embedded** → RAG DB + MCP servers.

> "Then just as a human student could take a high school physics course, an LLM could take it in the same way. This would be a significantly richer source of legible information than pdf-to-text (current prevailing practice), which simply asks the LLM to predict the textbook content top-to-bottom token by token — *lame*."

Seeds [[llm-knowledge-bases]] / [[microgpt]] / [[autoresearch]] lines of thought.

## Nov 19 — The benchmark-gaming apathy

Short post on Gemini 3 early-access experience. Starts with a caveat:

> "I usually urge caution with public benchmarks because they can be quite possible to game. It comes down to discipline and self-restraint of the team (who is meanwhile strongly incentivized otherwise) to not overfit test sets via elaborate gymnastics over test-set-adjacent data in the document embedding space."

Prescription: **go talk to the model. Talk to the other models.** Ride the "LLM Cycle" — use a different LLM every day. Positive Gemini 3 first impression (personality, writing, vibe coding, humor — tier-1 daily driver). Curious about **ensemble over private evals**.

### The "model smell" anecdote

An early Gemini 3 version, given a stale system prompt, *refused to believe* Karpathy that it was 2025:

> "I kept giving it images and articles from 'the future' and it kept insisting it was all fake. It accused me of using generative AI to defeat its challenges… It highlighted tiny details when I gave it Google Image Search results, arguing why the thumbnails were AI generated. I then realized later that I forgot to turn on the 'Google Search' tool. Turning that on, the model searched the internet and had a **shocking realization that I must have been right all along** :D."

> "It's in these unintended moments where you are clearly **off the hiking trails** and somewhere in the generalization jungle that you can best get a sense of **model smell**."

Off-trail = good eval. Central tool for reading LLM character in the [[animals-vs-ghosts|ghosts]] era.

## Nov 23 — LLM Council (vibe-coded)

Saturday project: `llm-council` — a ChatGPT clone that fans queries to multiple models via [[openrouter|OpenRouter]], lets them review each other's responses, then has a "Chairman LLM" synthesize.

Default council:
- `openai/gpt-5.1`
- `google/gemini-3-pro-preview`
- `anthropic/claude-sonnet-4.5`
- `x-ai/grok-4`

Observation: **models are surprisingly willing to rank another LLM above themselves**, making this an interesting eval strategy.

> "Reading book chapters with my LLM Council, the models consistently praise GPT-5.1 as best and consistently select Claude as worst. But I'm not 100% convinced this aligns with my own qualitative assessment. Qualitatively I find GPT-5.1 a little too wordy and sprawled, Gemini 3 more condensed and processed, Claude too terse in this domain."

Released: `github.com/karpathy/llm-council`.

Thesis: "construction of LLM ensembles seems **under-explored**." Foreshadows multi-agent orchestration in 2026 corpus.

## The through-line

Three distinct eval strategies emerge across 2025:

| Strategy | Why | Example |
|---|---|---|
| **Market-revealed** (OpenRouter) | Incentive-aligned, real use cases | Apr 30 |
| **Private evals** | Org-specific, hard to leak | Nov 19 |
| **Off-trail probing** (model smell) | Reveals generalization character | Nov 19 |
| **LLM-on-LLM council** | Cross-judge ensemble | Nov 23 |

Meanwhile, pretraining data itself should become LLM-first, LLM-legible (Aug 29). "Training on the test set is a new art form" (Dec 20 year-in-review, see [[karpathy-x-2025-software-paradigm]]).

## Related

- [[openrouter]]
- [[llm-council]]
- [[model-smell]]
- [[leaderboard-illusion]]
- [[llm-knowledge-bases]]
- [[llm-gui]]
- [[andrej-karpathy]]
