---
title: The Growing Gap in Understanding AI Capability
type: source-summary
created: 2026-04-15
updated: 2026-04-15
sources: [4.10.md]
tags: [capability, agentic, rl, verifiable-rewards, karpathy]
---

# The Growing Gap in Understanding AI Capability

**Author:** [[andrej-karpathy|Andrej Karpathy]]
**Original source:** `raw/4.10.md` (X post, dated 4/10)
**Format:** short essay / thread

## Thesis

Public discourse about AI capability has split into two groups that speak past each other, because perceived capability depends heavily on (a) which model tier the viewer has used, and (b) whether the domain they've tested has received frontier RL attention.

## Key Claims

1. **Recency & tier mismatch.** Many people formed their opinion on the free tier of ChatGPT last year and extrapolate from quirks, hallucinations, and viral failures (e.g. Advanced Voice Mode fumbling "should I drive or walk to the carwash"). These free/deprecated models do **not** reflect the current state of the art.  *(single-source)*
2. **Peaky capability.** Even at paid frontier tiers ($200/mo), gains are not uniform across tasks — they are concentrated in highly technical domains (programming, math, research). Typical queries (search, writing, advice) have **not** made the most dramatic strides. See [[peaky-capability]]. *(single-source)*
3. **Two drivers of the peak.**
   - *Verifiable rewards*: programming/math/research offer explicit, machine-checkable reward signals (unit tests pass y/n) that suit [[reinforcement-learning]] training. Writing and advice don't. See [[verifiable-rewards]].
   - *B2B value concentration*: these technical domains are where the money is, so the biggest fraction of research teams focuses there.
4. **"AI Psychosis" in group 2.** Professionals who (1) pay for frontier agentic models ([[openai-codex|OpenAI Codex]], [[claude-code|Claude Code]]) and (2) use them in programming/math/research assign much greater gravity to capability gains and cyber repercussions, because they watch the models "melt" problems that would take humans days/weeks. *(Karpathy's coinage; opinion)*
5. **Simultaneity.** It is *simultaneously* true that OpenAI's Advanced Voice Mode fumbles trivial questions in viral reels, *and* that Codex can autonomously restructure entire codebases or find and exploit vulnerabilities over ~1 hour of uninterrupted work.

## Notable Quotes

> "When you hand a computer terminal to one of these models, you can now watch them melt programming problems that you'd normally expect to take days/weeks of work."

> "these domains offer explicit reward functions that are verifiable meaning they are easily amenable to reinforcement learning training (e.g. unit tests passed yes or no, in contrast to writing, which is much harder to explicitly judge)"

## Named Entities

- [[andrej-karpathy|Andrej Karpathy]] — author
- [[openai-codex|OpenAI Codex]] — cited as frontier agentic model, "highest-tier and paid"
- [[claude-code|Claude Code]] — cited as frontier agentic model (Anthropic)
- ChatGPT free tier — cited as the source of outdated public impressions
- Advanced Voice Mode — cited as a viral failure case; Karpathy describes it as "slightly orphaned (?)"

## Concepts Introduced / Reinforced

- [[agentic-models]] — models handed a terminal that act over long horizons
- [[verifiable-rewards]] — prerequisite for RL-driven capability gains
- [[peaky-capability]] — capability is not uniform across domains
- [[ai-psychosis]] — Karpathy's label for the heightened gravity professional users assign to frontier capability gains
- [[reinforcement-learning]] — the training mechanism behind the recent peak

## Open Questions

- Is the "peak" permanent or will non-verifiable domains catch up as reward modeling improves?
- What is the actual distribution of Codex / Claude Code wins vs. failures on hour-long agentic tasks? (Karpathy asserts "melting" but gives no base rate.)
- Karpathy says Advanced Voice Mode is "slightly orphaned (?)" — is this confirmed or speculation?

## My Reading (commentary — distinct from source)

Karpathy's framing is itself a claim that merits tracking: that *verifiability* of rewards is the causal lever behind the recent agentic-coding capability jump. If true, this predicts that domains adjacent to programming with good eval harnesses (theorem proving, sysadmin, data analysis) will be the next to jump. This is testable against future sources.
