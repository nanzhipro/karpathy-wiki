---
title: "2025 — Build for Agents: Ergonomics, Context Engineering, LLM GUI"
type: source-summary
created: 2026-04-17
updated: 2026-04-17
sources: [2025/4.22.md, 2025/5.1.md, 2025/7.20.md, 2025/7.25.md, 2025/11.24.md]
tags: [build-for-agents, context-engineering, llm-gui, vibe-coding, agent-ergonomics]
---

# 2025 — Build for Agents: Ergonomics, Context Engineering, LLM GUI

Five posts across the year naming the shift: **the primary audience of your product is now an LLM, not a human** — and the still-missing LLM-native GUI.

## Apr 22 — "PSA: new era of ergonomics"

> "The primary audience of your thing (product, service, library, …) is now an **LLM, not a human**.
> LLMs don't like to navigate, they like to **scrape**.
> LLMs don't like to see, they like to **read**.
> LLMs don't like to click, they like to **curl**."

Concrete prescriptions:
- **Tired:** elaborate docs pages with branding, dark mode, animations.
- **Wired:** one single docs .md file and a "copy to clipboard" button.
- Docs content too: instead of "go to this page and click top-right," show **curl commands**.
- Adding a Supabase DB to a Vercel app shouldn't be clicks — it should be curls.

The canonical statement of what later becomes [[build-for-agents]]. "Felt like a neanderthal" reading a 2024-style docs page in 2025.

## May 1 — MenuGen: vibe-coding a full web app (+ LLM GUI)

Karpathy's first-person vibe-coding report. Built [menugen.app](http://menugen.app) at a hackathon — you photograph a menu, it generates images for each dish (helpful for identifying Pâté, Tagine, Cavatappi, Sweetbread).

He wrote **none** of the code directly (Cursor + Claude / o3 did). Full writeup: `karpathy.bearblog.dev/vibe-coding-menugen/`.

TL;DR from the blog:

> "Vibe coding menugen was exhilarating and fun as a local demo, but a bit of a painful slog as a deployed, real app. Building a modern app is like assembling IKEA furniture — services, docs, API keys, configurations, dev/prod deployments, team and security features, rate limits, pricing tiers... the LLMs have slightly outdated knowledge of everything, make subtle but critical design mistakes, sometimes hallucinate or gaslight you about solutions."
>
> "Most interesting — I didn't spend much time in the code editor. I spent most of it **in the browser, moving between tabs, configuring and gluing a monster**. All of this work and state is not even accessible or manipulatable by an LLM — how are we supposed to be automating society by 2027 like this?"

### LLM GUI — the prediction

Second half of the post is the **first public sketch of what an LLM-native GUI looks like**:

1. **Visual** — vision is the 10-lane highway into the brain (~1/3 of brain compute).
2. **Generative + input-conditional** — GUI rendered on demand, specifically for your prompt. Everything reconfigured with immediate purpose in mind.
3. **Degree of procedural is open** — one extreme: one big diffusion model dreams the entire canvas. Other: a page of procedural React components (charts, images, diagrams). Likely a mix, with procedural as the skeleton.

> "Some fluid, magical, ephemeral, interactive 2D canvas written from scratch and just for you is the limit as capability goes to ∞."

Seeds already: code blocks, LaTeX blocks, markdown, Artifacts tab, Mermaid charts. Cultural shoutout: Iron Man, Star Trek, Minority Report.

Becomes the Dec 20 year-in-review's "Nano Banana / LLM GUI" paradigm change.

## Jul 20 — GUI-for-LLMs demo commentary

Short post on a demo of a generative GUI for LLMs:

> "Obviously it has a bit silly feel of a 'horseless carriage' in that it exactly replicates conventional UI in the new paradigm, but the high-level idea is to generate a completely ephemeral UI on demand depending on the specific task at hand."

The "horseless carriage" framing — transitional forms that copy the old medium before finding their native shape — is a useful dev-signpost for the whole [[llm-gui]] space.

## Jul 25 — "Context engineering" over "prompt engineering"

The definitive coinage endorsement:

> "+1 for **context engineering** over **prompt engineering**. People associate prompts with short task descriptions. In every industrial-strength LLM app, context engineering is the delicate art and science of filling the context window with just the right information for the next step."

What's in the context window:

> "Task descriptions and explanations, few shot examples, RAG, related (possibly multimodal) data, tools, state and history, compacting..."

Too little / wrong form → poor performance. Too much / irrelevant → cost up, performance down. **Science** because of the mechanics; **art** because of [[people-spirits|LLM psychology]].

And — critically — context engineering is only one piece of an "emerging thick layer":

- Break problems into control flows.
- Pack context windows.
- Dispatch to LLMs of the right kind and capability.
- Handle generation-verification UIUX.
- Guardrails, security, evals, parallelism, prefetching.

> "The term '**ChatGPT wrapper**' is tired and really, really wrong."

Directly rebuts the "labs will eat all apps" thesis — the app layer is thick, and one of its names is context engineering.

## Nov 24 — Gemini 3 Nano Banana Pro as LLM GUI proof

Playing with Google's Gemini 3 Nano Banana Pro:

> "[It] can solve exam questions **in** the exam page image. With doodles, diagrams, all that."

Also: asked for a personalized weekly workout plan → got printable **posters** to tape to the wall. "Tuesday looks more intense because I asked for 'more testosterone.'"

> "Imo this is along the lines of how talking to an LLM via text is like typing into a DOS Terminal and 'GUI hasn't been invented yet'."

First clean sighting of the multimodal-output GUI Karpathy predicted in May — still basically poster/worksheet-shaped, not yet ephemeral interactive canvas.

## The through-line

| Axis | Apr 22 | May 1 | Jul 20 | Jul 25 | Nov 24 |
|---|---|---|---|---|---|
| Ergonomics | Docs = markdown | Config-glue bottleneck | Horseless UIs | Thick app layer | Visual output |
| Audience | LLM, not human | LLM can't reach browser state | UI for LLM use | LLM as primary reader | LLM as illustrator |
| Missing thing | curl-first products | LLM-accessible auth/config | Ephemeral procedural UI | Named craft: ctx-eng | Diagram-native answers |

Together they sketch the 2026 [[build-for-agents]] / [[llm-gui]] / [[agentic-engineering]] stack.

## Related

- [[build-for-agents]]
- [[context-engineering]]
- [[llm-gui]]
- [[vibe-coding]]
- [[people-spirits]]
- [[iron-man-analogy]]
- [[partial-autonomy-apps]]
- [[app-store-outdated]]
- [[cursor]]
- [[andrej-karpathy]]
