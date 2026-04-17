---
title: Autonomy Slider
type: concept
created: 2026-04-17
updated: 2026-04-17
sources: [andrej-karpathy-software-is-changing-again/transcript.md, andrej-karpathy-were-summoning-ghosts-not-building-animals/transcript.md]
tags: [product, ux, llm, karpathy]
---

# Autonomy Slider

A product mechanic: let the user pick, per task, how much autonomy to grant the AI. Low = tab-completion / suggest-and-accept. High = multi-step agent with tool use.

## Sources

- [Karpathy, Software Is Changing (Again)](../sources/software-is-changing-again.md) — canonical formulation. [[cursor|Cursor]] and [[perplexity|Perplexity]] both expose a slider; the user adjusts per task.
- [Karpathy, Summoning Ghosts](../sources/summoning-ghosts-not-animals.md) — the principle extended: agents can't yet reliably operate at the high end of the slider, and the [[march-of-nines]] predicts a decade of slow dial-up.

## Why it matters

- LLMs are [[people-spirits]] with [[jagged-intelligence]]. Automation costs (verification overhead, error recovery) don't scale linearly with task complexity — they explode. The slider lets users match autonomy to task difficulty and personal risk tolerance.
- The [[iron-man-analogy]]: we're building suits, not robots. The slider is how the suit lets the pilot pick their level of assistance.
- **Tesla is the deep prior.** 12 years of graduated autonomy on Autopilot — Karpathy still intervenes. Products should assume the same arc.

## Design heuristics (assembled from Karpathy's talks)

- Default the slider low.
- Make verification UI fast (diffs, highlights, citations).
- Failed autonomy at level N should degrade gracefully to level N-1, not fail outright.
- Don't ship the "full autonomy" setting until the [[march-of-nines]] supports it.

## Related

- [[partial-autonomy-apps]] — the product shape the slider lives inside
- [[iron-man-analogy]]
- [[march-of-nines]]
- [[tesla]], [[waymo]] — the empirical priors
