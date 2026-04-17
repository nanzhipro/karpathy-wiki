---
title: "2025-11 / 12 — Reading with LLMs & HN Time Capsule"
type: source-summary
created: 2026-04-17
updated: 2026-04-17
sources: [2025/11.18.md, 2025/12.11.md]
tags: [reader3, hn-time-capsule, llm-reading, galaxy-brain, writing-for-llms]
---

# 2025-11 / 12 — Reading with LLMs & HN Time Capsule

Two posts in which Karpathy makes explicit that he now reads everything *with an LLM in the loop*, and starts treating in-hindsight analysis over historical text as a serious research practice.

## Nov 18 — Reading with LLMs + reader3 + galaxy-brain reasoning

### The reading workflow

> "I'm starting to get into a habit of reading everything (blogs, articles, book chapters,…) with LLMs. Usually **pass 1 manual**, then **pass 2 'explain/summarize'**, **pass 3 Q&A**. I usually end up with a better/deeper understanding than if I moved on. Growing to among top use cases."

Flip side:

> "If you're a writer trying to explain/communicate something, we may increasingly see less of a mindset of 'I'm writing this for another human' and more 'I'm writing this for an LLM'. Because once an LLM 'gets it', it can then target, personalize and serve the idea to its user."

Writing **for LLMs** rather than for humans becomes a viable content strategy — the LLM becomes the universal translator/personalizer.

### reader3 — the tool

Released `reader3` (his third iteration): a simple repo for reading EPUBs with LLMs — chapter-by-chapter text extraction for copy-paste into your favorite LLM. Source Project Gutenberg works well. Link: `github.com/karpathy/reader3`.

Minimal, dependency-light — very much in the [[bacterial-code]] spirit.

### Galaxy-brain reasoning

> "Finally had time to read & process this great post. I run into the pattern quite often, it goes:
> '<something that sounds wrong> is good actually, because <galaxy brain reason>'
> **Galaxy brain reasoning is the best way to justify anything while looking / feeling good about it.**"

Illustration: the Ten Commandments as **constraints on actions** rather than utilities over states — "thou shalt not kill" curtails the flexibility of galaxy-brain arithmetic over when killing might serve some greater purpose. Not *Ten Objectives*.

Actionable takeaways from the linked post: (1) have principles, (2) hold the right bags — financially and socially.

Named as a recognizable failure mode useful for flagging flawed reasoning in LLM outputs and human arguments alike.

## Dec 11 — nanoGPT in space + HN Time Capsule

### nanoGPT in space

> "nanoGPT — the first LLM to train and inference in space 🥹. It begins."

Short — but part of the recurring "[[ramps-to-knowledge|ramp]] keeps compounding" arc.

### HN Time Capsule

The main event. Karpathy vibe-coded an in-hindsight grading system over **all 930 front-page Hacker News discussions from December 2015** using GPT 5.1 Thinking.

Cost / effort:
- ~**3 hours** to vibe code.
- ~**1 hour and $60** to run.

Setup context:
- Sparked by an HN article where Gemini 3 was asked to hallucinate HN front page *a decade forward*.
- Karpathy ran it *a decade backward* — grading actual past comments.

### Why it matters

> "1. In-hindsight analysis has always fascinated me as a way to **train your forward prediction model**.
> 2. It's worth contemplating what it looks like when LLM megaminds of the future can do this kind of work a lot cheaper, faster and better. **Every single bit of information you contribute to the internet can (and probably will be) scrutinized in great detail if it is 'free'**. Hence also my earlier tweet — 'be good, future LLMs are watching'."

The "future LLMs are watching" frame turns the standard privacy/speech tradeoff upside-down — your public record is training data for a retrospective judgment at lower cost and higher resolution each year.

### The top-10 HN commenters of Dec 2015

GPT 5.1 Thinking selected as most insightful/prescient: **pcwalton, tptacek, paulmd, cstross, greglindahl, moxie, hannob, 0xcde4c3db, Manishearth, johncolanduoni**.

Links:
- Blog: `karpathy.bearblog.dev/auto-grade-hn/`
- Repo: `github.com/karpathy/hn-time-capsule`
- Results: `karpathy.ai/hncapsule/`

## Why these posts matter

- **LLM-assisted reading** as a first-class practice — 2-3-pass workflow is cited by others throughout the 2026 corpus.
- **reader3** is another [[bacterial-code]] exemplar: tiny repo, dependency-light, copy-paste-able.
- **Galaxy-brain reasoning** gives a name to the pattern that shows up in LLM justifications and in human rationalizations — useful for [[agentic-engineering|review]] filters.
- **HN Time Capsule** is a concrete test-run of "Auto-Research" kind of retrospective grading — a near-cousin to [[autoresearch]] in the 2026 corpus.
- Cultural takeaway: in the ghost era, writing is increasingly an act of authoring training data.

## Related

- [[reader3]]
- [[hn-time-capsule]]
- [[galaxy-brain-reasoning]]
- [[writing-for-llms]]
- [[bacterial-code]]
- [[autoresearch]]
- [[llm-knowledge-bases]]
- [[andrej-karpathy]]
