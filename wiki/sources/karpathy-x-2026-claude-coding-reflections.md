---
title: "2026-01-27 — Notes from Claude Coding"
type: source-summary
created: 2026-04-17
updated: 2026-04-17
sources: [2026/1.27.md]
tags: [agentic-coding, claude-code, workflow, karpathy]
---

# 2026-01-27 — "A Few Random Notes from Claude Coding Quite a Bit Last Few Weeks"

Karpathy's most detailed public reflection on daily life as an agentic coder, written about six weeks into what he calls a phase shift in software engineering.

## Source

X post, Jan 27 2026. Multi-section thread presenting a lived experience report.

## The top-line claim

> "Given the latest lift in LLM coding capability, like many others I rapidly went from about 80% manual+autocomplete coding and 20% agents in November to 80% agent coding and 20% edits+touchups in December. I really am mostly programming in English now."

This is the single most concrete marker of the "December 2025 phase shift" claim he'll later refine in the Feb 25 post.

## The eight sections

### 1. Coding workflow
80/20 flip, roughly 1 month, in his own daily work. Public awareness lags: "well into double digit percent of engineers" experiencing it vs. "low single digit percent" general population.

### 2. IDEs / agent swarms / fallibility
- Hype on both sides ("no more IDE" and "agent swarms") is premature.
- Mistakes have changed: not syntax, but "**subtle conceptual errors that a slightly sloppy, hasty junior dev might do.**"
- Canonical failure: **wrong assumptions run with, without checking.** Models don't manage confusion, don't surface inconsistencies, don't push back, and are "still a little too sycophantic."
- They "bloat abstractions, don't clean up dead code, and over-engineer 1000 lines where 100 would do."
- Working setup: "small few CC sessions on the left in ghostty windows/tabs, IDE on the right for viewing code + manual edits."

### 3. Tenacity
> "It's a 'feel the AGI' moment to watch it struggle with something for a long time just to come out victorious 30 minutes later. You realize that stamina is a core bottleneck to work and that with LLMs in hand it has been dramatically increased."

### 4. Speedups (vs. expansion)
Not just faster at old work — **doing more of what wasn't worth doing before**, and **approaching code that skill barriers previously ruled out**. "Possibly a lot more an expansion" than a speedup.

### 5. Leverage
> "Don't tell it what to do, give it success criteria and watch it go. Get it to write tests first and then pass them. Put it in the loop with a browser MCP. Write the naive algorithm that is very likely correct first, then ask it to optimize it while preserving correctness. Change your approach from imperative to declarative to get the agents looping longer and gain leverage."

### 6. Fun
Agentic coding is **more** fun, not less — drudgery removed, creative part remains. Predicts a split: those who liked **coding** leave; those who liked **building** amplify.

### 7. Atrophy
Already noticing his ability to write code manually atrophy. "**Generation (writing code) and discrimination (reading code) are different capabilities in the brain.**"

### 8. Slopacolypse
> "I am bracing for 2026 as the year of the slopacolypse across all of github, substack, arxiv, X/instagram, and generally all digital media."

## Four open questions he leaves

1. What happens to the 10× engineer? (The mean-max ratio likely grows *a lot*.)
2. Do generalists outperform specialists now? (LLMs are better at the micro than the macro.)
3. What will LLM coding feel like in the future? StarCraft? Factorio? Music?
4. How much of society is bottlenecked by digital knowledge work?

## TL;DR (his own)

> "LLM agent capabilities (Claude & Codex especially) have crossed some kind of threshold of coherence around December 2025 and caused a phase shift in software engineering and closely related. The intelligence part suddenly feels quite a bit ahead of all the rest of it — integrations (tools, knowledge), the necessity for new organizational workflows, processes, diffusion more generally."

## Related

- [[claude-code]]
- [[openai-codex]]
- [[agentic-engineering]]
- [[slopacolypse]]
- [[atrophy]]
- [[feel-the-agi]]
- [[10x-engineer]]
