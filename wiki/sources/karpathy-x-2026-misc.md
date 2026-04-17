---
title: "2026 Q1–Q2 — Karpathy X Posts (Miscellaneous)"
type: source-summary
created: 2026-04-17
updated: 2026-04-17
sources: [2026/1.7.md, 2026/1.31.md, 2026/2.1.md, 2026/3.25.md, 2026/3.27.md, 2026/3.28.md]
tags: [misc, karpathy]
---

# 2026 Q1–Q2 — Miscellaneous Karpathy Posts

Short posts that didn't warrant standalone source summaries but contain ideas referenced elsewhere in the wiki.

## Jan 7 — Point vs Slope

> "The majority of the ruff ruff is people who look at the current point and people who look at the current slope."

**Idea:** most public disagreement about AI capability collapses to this. Karpathy invokes it again in the Feb 4 post on agent networks. It's his explanation for why the [[ai-capability-gap|capability gap]] debate never lands.

## Jan 31 — Bring back RSS

> "Finding myself going back to RSS/Atom feeds a lot more recently. There's a lot more higher quality longform and a lot less slop intended to provoke. Any product that happens to look a bit different today but that has fundamentally the same incentive structures will eventually converge to the same black hole at the center of gravity well. We should bring back RSS — it's open, pervasive, hackable."

**Links to:** [[slopacolypse]] (the slop prediction), [[build-for-agents]] (RSS is already agent-friendly), [[llm-knowledge-bases]] (RSS as ingestion source).

## Feb 1 — Bet on research-focused startups

A launch-congratulations post for a new research-focused startup. Thesis:

> "A conventional narrative you might come across is that AI is too far along for a new, research-focused startup to outcompete and outexecute the incumbents of AI. This is exactly the sentiment I listened to often when OpenAI started… and 1) it was very wrong, and then 2) it was very wrong again with a whole another round of startups who are now challenging OpenAI in turn, and imo it still continues to be wrong today."

Key argument: the gap between frontier LLMs and "a mind running on 20 watts" is still large; **10× research breakthroughs (not 10%) remain plausible.**

## Mar 25 — Project Hail Mary

Movie review; off-topic for the wiki's core concerns, but worth noting that Karpathy flags scientific-detail-rich fiction (Andy Weir's book, underlying spreadsheets) as a preferred cultural form. Connects obliquely to his [[ramps-to-knowledge|ramp pedagogy]] — show the work.

## Mar 27 — LLM memory overfit

> "One common issue with personalization in all LLMs is how distracting memory seems to be for the models. A single question from 2 months ago about some topic can keep coming up as some kind of a deep interest of mine with undue mentions in perpetuity."

**Hypothesis:** training bias — "a lot of the information in the context window is relevant to the task, so the LLMs develop a bias to use what is given," which at test time overfits to retrieved memory entries. Connects to [[llm-cognitive-deficits]].

**Also connects to** [[byoai]] — another argument for the Apr 5 "explicit, inspectable" memory philosophy: you can *see* what the system thinks you care about.

## Mar 28 — Argue the opposite

> "Drafted a blog post. Used an LLM to meticulously improve the argument over 4 hours. Wow, feeling great, it's so convincing! Fun idea let's ask it to argue the opposite. LLM demolishes the entire argument and convinces me that the opposite is in fact true. lol"

**Takeaway:** LLMs are very good at arguing *any* direction. Useful technique: **always ask for both sides.** Watch for sycophancy. Links to [[people-spirits]] (the LLM as population simulator, not an opinion-holder).

## Related

- [[slopacolypse]]
- [[ai-capability-gap]]
- [[llm-cognitive-deficits]]
- [[people-spirits]]
- [[build-for-agents]]
