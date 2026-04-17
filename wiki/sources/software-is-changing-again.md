---
title: Software Is Changing (Again)
type: source-summary
created: 2026-04-17
updated: 2026-04-17
sources: [andrej-karpathy-software-is-changing-again/transcript.md]
tags: [software-3-0, llm-os, agents, autonomy-slider, vibe-coding, karpathy]
---

# Software Is Changing (Again)

**Speaker:** [[andrej-karpathy|Andrej Karpathy]]
**Venue:** Y Combinator AI Startup School (June 17, 2025)
**Original source:** `raw/youtube-transcript/y-combinator/andrej-karpathy-software-is-changing-again/transcript.md`
**Format:** keynote, ~40 min

## Thesis

Software has just undergone its second fundamental rewrite in 70 years, and we're living through the third. After decades of Software 1.0 (hand-written code) and a ~10-year phase of Software 2.0 (neural-net weights tuned by optimizers on datasets), LLMs introduce **[[software-3-0|Software 3.0]]**: programs written in English prompts. Because the substrate keeps changing, *everything has to be rewritten* — and students entering the field now are unusually well-positioned to do it.

## Key Claims

1. **Three software paradigms coexist.** Software 1.0 is code; 2.0 is neural-net weights ([[github]] has GitHub → Hugging Face as its 2.0 analog, and models like AlexNet/Tesla autopilot show 1.0 getting *eaten* by 2.0); 3.0 is English prompts over LLMs. Each runs on a different substrate and demands different skills. *(framing)*
2. **LLMs are best understood through three layered analogies.** (a) LLMs are **utilities** — capex-heavy training, opex metered inference, demands for low latency / high uptime / consistent quality; outages feel like a "brownout" of the world's intelligence. (b) LLMs are **semiconductor fabs** — enormous R&D capex, deep tech trees, the "Nvidia GPU clouds ↔ fabless / Google TPU ↔ Intel" mapping. (c) LLMs are **operating systems** — not a simple utility but a complex software ecosystem with closed-source leaders (Windows/macOS = GPT/Claude/Gemini) and an open-source competitor ([[llama]] ≈ Linux). See [[llm-os]]. *(single-source, but developed extensively)*
3. **We're in the "1960s of computing."** LLMs are centralized compute in the cloud, time-shared, streamed as tokens in a terminal — the personal-computing revolution has not happened yet. *(analogical)*
4. **LLMs are "[[people-spirits|people spirits]]."** Stochastic simulations of humans, trained on text, with super-human breadth of memory (Rain Man–like recall of SHA-256) but very human cognitive deficits — hallucinations, **[[jagged-intelligence|jagged intelligence]]** (PhD-level problem solving next to "9.11 > 9.9"), anterograde amnesia (no persistent learning from session to session, c.f. *Memento* and *50 First Dates*), and gullibility / prompt-injection vulnerability. *(coinage, developed further in [[summoning-ghosts-not-animals]])*
5. **The right product pattern is [[partial-autonomy-apps|partial-autonomy apps]] with an [[autonomy-slider|autonomy slider]].** [[cursor|Cursor]] and [[perplexity|Perplexity]] are canonical: they package model calls with a domain UI, let humans verify quickly (GUIs beat text for auditing), and expose a slider from tab-completion → agent-mode. Tesla Autopilot is the deep prior here: shipped 2013, "perfect drive" delivered on day one, yet 12 years later Karpathy still intervenes — **software is tricky**, so keep the human in the loop and grow autonomy conservatively. See [[march-of-nines]]. *(experiential claim)*
6. **Everyone is now a programmer.** [[software-3-0|Software 3.0]] is written in English — the hottest new programming language. [[vibe-coding|Vibe coding]] (Karpathy's viral X post; now a Wikipedia entry and a term Tom Wolf uses in front of high schoolers) means anyone can prototype apps in an afternoon. The non-obvious finding: writing the code is the easy part; the **"DevOps" of making it real** — Apple Developer IDs, Vercel configs, payments integrations, Google Auth — is a week of clicking. *(single-source, personal experience with MenuGen)*
7. **Build for agents, not just humans or crawlers.** A new category of consumer and manipulator of digital info has arrived. Concrete moves: (a) `lm.txt` as the agent-readable sibling of `robots.txt`; (b) Markdown-first docs instead of screenshot-heavy HTML; (c) Replace "click here" with explicit `curl` / API instructions; (d) [[model-context-protocol|MCP]] to expose structured capability; (e) `gitingest.com` and `deepwiki.org`-style ingestion to make codebases LLM-legible. Meeting agents halfway is cheap and compounds. *(call to action)*
8. **Iron Man suit > Iron Man robot.** The autonomy dial should stay left of full automation for a long time. The valuable product is augmentation with a verification UI — not a demo that runs overnight. *(framing, see [[iron-man-analogy]])*

## Structure of the Talk

1. **Software 1.0 → 2.0 → 3.0** — the substrate has been rewritten twice.
2. **LLMs as utilities / fabs / OS** — three layered analogies.
3. **LLMs as people spirits** — psychology, deficits, and what to design around.
4. **Opportunity #1: partial-autonomy apps** — Cursor/Perplexity, the autonomy slider, Tesla lessons.
5. **Opportunity #2: vibe coding** — English as the new programming language; DevOps is the hard part.
6. **Opportunity #3: build for agents** — make your digital infrastructure machine-readable.

## Notable Quotes

> "It's a remarkable time to enter the industry because we have to rewrite a ton of code."

> "LLMs are like operating systems... closed-source providers like Windows or macOS, and then there's an open-source alternative that looks a little bit like Linux — and I think with Llama, it's possibly going to grow into something like Linux."

> "We're in the 1960s of large language models. They are time-shared, over terminals, and the personal computing revolution for LLMs hasn't happened yet."

> "They have super-human memory. It's a bit like *Rain Man*... and then they also have all kinds of cognitive deficits. They hallucinate quite a bit. They have jagged intelligence."

> "Keep AI on the leash. We're not building *Iron Man* robots. We're building *Iron Man* suits."

> "I think this is actually really interesting. You can see that in my case, writing the code was the easy part... but making it real for actual users was the hard part. And it took a whole week — and most of it was not coding."

## Named Entities & Concepts (first appearance)

- [[andrej-karpathy|Andrej Karpathy]] — speaker
- [[openai]] — founding OpenAI member; co-founder in 2015
- [[tesla]] — five-year director of AI, [[tesla-autopilot]] (Software 2.0 exemplar)
- [[llama]] — as open-source "Linux" of the LLM stack
- [[cursor]], [[perplexity]] — canonical [[partial-autonomy-apps]]
- [[vibe-coding]] — viral X-post coinage, now dictionary-entry
- [[menugen]] — Karpathy's weekend vibe-coded app; showcase of DevOps pain
- [[model-context-protocol|MCP]] — Anthropic's protocol for agents to talk to services
- gitingest.com, deepwiki.org — URL-transform tools making repos LLM-legible
- Tom Wolf ([[hugging-face]]) — "vibe coding" slide in keynote
- Geoff Hinton — quoted on [[people-spirits]] framing
- George Hotz — cited on difficulty of shipping real software

## Concepts Introduced / Reinforced

- [[software-3-0]] — English as the new programming language
- [[llm-os]] — LLMs as a new operating system, ~1960s-era compute
- [[people-spirits]] — LLM psychology
- [[jagged-intelligence]] — peaky profile of LLM competence
- [[partial-autonomy-apps]] — the winning product shape
- [[autonomy-slider]] — product mechanic
- [[march-of-nines]] — self-driving lesson applied to AI products
- [[vibe-coding]] — prompting > coding for small apps
- [[build-for-agents]] — make docs and tools agent-legible
- [[iron-man-analogy]] — augmentation beats automation, for now

## Open Questions

- Is the Linux/Llama parallel load-bearing, or will a single closed leader dominate LLMs the way Windows did desktop?
- How far left-of-full-autonomy should the slider stay, and for how long? Karpathy says "decade of agents" here and repeats it in [[summoning-ghosts-not-animals]] — consistent across sources.
- What is the right generation-verification UX for non-code domains? Cursor works because diffs audit cleanly; writing/advice don't.

## My Reading (commentary)

The most durable contribution here is the three-layered analogy (utility / fab / OS) — it predicts product strategy more than any single metaphor does alone. The OS framing in particular explains *why* a startup can build a thin app layer on top of frontier models without being immediately crushed: you're building for the OS, not competing with it. The weakest part is the "everyone is a programmer now" claim — vibe-coded apps remain disposable demos; the DevOps-is-harder-than-code observation quietly undermines the democratization thesis.
