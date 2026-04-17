---
title: LLM GUI
type: concept
created: 2026-04-18
updated: 2026-04-18
sources: [2025/5.1.md, 2025/7.20.md, 2025/11.24.md, 2025/12.20.md]
tags: [ui, llm-product, karpathy-coinage]
---

# LLM GUI

The still-unbuilt graphical user interface for LLMs. Chatting with an LLM via text is, in Karpathy's metaphor, "like typing into a DOS terminal" — the GUI hasn't been invented yet.

## The prediction

Originated in the [[karpathy-x-2025-build-for-agents|May 1 2025]] MenuGen blog-post / tweet. Three predicted properties:

1. **Visual** — vision is the 10-lane highway into the brain (~1/3 of brain compute). Highest input-information bandwidth.
2. **Generative + input-conditional** — GUI rendered on demand, specifically for *your* prompt. Everything reconfigured with the immediate purpose in mind.
3. **Procedural to some degree** — open question whether one big diffusion model dreams the whole canvas, or a page of procedural React components (images, charts, animations). Likely a mix, with procedural as the skeleton.

> "Some fluid, magical, ephemeral, interactive 2D canvas written from scratch and just for you is the limit as capability goes to ∞."

Cultural shoutouts: Iron Man, Star Trek, Minority Report.

## Already-deployed precursors

- Code blocks with syntax highlighting
- LaTeX blocks
- Markdown (bold, italic, lists, tables, even emoji)
- [[claude-code|Artifacts tab]] with Mermaid charts / full apps
- Video-generation for "diagrams, charts, animations" ([[karpathy-x-2025-video-gen|Jul 3]])

## The horseless-carriage phase

[[karpathy-x-2025-build-for-agents|Jul 20 2025]] on a demo of a GUI-for-LLMs:

> "Obviously it has a bit silly feel of a 'horseless carriage' in that it exactly replicates conventional UI in the new paradigm, but the high-level idea is to generate a completely ephemeral UI on demand depending on the specific task at hand."

Current forms copy the old medium before finding their native shape.

## Dec 2025 paradigm-change milestone

From the [[karpathy-x-2025-software-paradigm|year-in-review]]: Google Gemini 3 "**Nano Banana**" — solves exam questions *on the exam page image*, emits printable workout-plan **posters**, generates diagrams on demand.

> "Gemini Nano Banana is one of the most incredible, paradigm-shifting models of 2025 — not for image quality but for being the **first hint of an LLM GUI**."

## Why it's underestimated

Text-first LLMs are capability-bottlenecked by the channel. Once the channel is high-bandwidth visual output:
- Explanations become charts/animations.
- Tutoring becomes custom visualizations per question.
- Commerce becomes ephemeral custom store layouts.
- Gaming becomes real-time MirageLSD-style diffusion on simple primitives.

## Relation to other concepts

- **[[partial-autonomy-apps]]** — each will need its own GUI tailored by an LLM.
- **[[build-for-agents]]** — parallel axis: products speak to agents (text), but agents speak to users (visual).
- **[[app-store-outdated]]** — if a GUI is on-demand and ephemeral, what is the "app"?
- **[[decart]]** / **[[miragelsd]]** — real-time video diffusion is one track.

## Related

- [[video-generation]]
- [[build-for-agents]]
- [[iron-man-analogy]]
- [[partial-autonomy-apps]]
- [[app-store-outdated]]
- [[miragelsd]]
- [[decart]]
