---
title: People Spirits
type: concept
created: 2026-04-17
updated: 2026-04-17
sources: [andrej-karpathy-software-is-changing-again/transcript.md]
tags: [llm-psychology, karpathy-coinage]
---

# People Spirits

Karpathy's coinage: LLMs are **stochastic simulations of people**, trained on text, inheriting specific strengths and specific cognitive failure modes from that training. The frame sits between "magical AI" and "just autocomplete" and drives product decisions.

## Source

- [Karpathy, Software Is Changing (Again)](../sources/software-is-changing-again.md) — "I think of LLMs as people spirits. They have emergent psychology." Quotes Geoff Hinton in support.
- Extended in [[summoning-ghosts-not-animals]] under the related framing [[animals-vs-ghosts]] — the "ghost" is the digital cousin of a people-spirit.

## Strengths (inherited from human text)

- Super-human breadth of memory. Karpathy's *Rain Man* analogy: instant SHA-256 recall, long tables of facts.
- Compositional language fluency.
- Useful priors across most human knowledge.

## Deficits (that product design must absorb)

- **Hallucinations.** Confident assertions that are wrong.
- **[[jagged-intelligence]].** PhD-grade problem solving on one request, "9.11 > 9.9" on the next.
- **Anterograde amnesia.** No persistent learning session-to-session. *Memento* and *50 First Dates* are Karpathy's go-to analogies.
- **Gullibility / prompt-injection vulnerability.** Text is both data and instruction; models can't reliably distinguish.

## Design implications

- Build GUIs that surface model output for fast human verification — see [[partial-autonomy-apps]].
- Keep the [[autonomy-slider]] low until verification is robust.
- Prefer [[iron-man-analogy|augmentation over automation]].

## Related

- [[animals-vs-ghosts]] — the 2025 extension of this frame
- [[jagged-intelligence]]
- [[llm-cognitive-deficits]]
