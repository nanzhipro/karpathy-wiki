---
title: LLM OS
type: concept
created: 2026-04-17
updated: 2026-04-17
sources: [andrej-karpathys-keynote-winner-pitches-at-uc-berkeley-ai-hackathon-2024-awards-ceremony/transcript.md, andrej-karpathy-software-is-changing-again/transcript.md]
tags: [llm, systems, metaphor, karpathy-coinage]
---

# LLM OS

Karpathy's metaphor: LLMs are not a utility or an API, they are the **kernel of a new operating system**. The analogy structures product strategy and investment logic in the frontier-model era.

## Three nested analogies (YC 2025)

In [[software-is-changing-again]], Karpathy layers three analogies for LLMs:

1. **LLMs as utilities.** Training = capex (like a power plant). Inference = opex metered per token. Users demand low latency, high uptime, consistent quality. An outage feels like a "brownout" of the world's intelligence.
2. **LLMs as fabs.** Enormous R&D capex, deep tech trees, tight coupling between hardware and software. Mapping: Nvidia-GPU clouds ↔ fabless designers, Google TPU ↔ Intel's integrated model.
3. **LLMs as operating systems.** Not just a utility — a complex software ecosystem with closed-source leaders (Windows/macOS = GPT / Claude / Gemini) and an open-source challenger (Linux = [[llama|Llama]]).

The OS frame is the one Karpathy leans on hardest because it predicts product strategy: startups build on the OS, not against it.

## "We're in the 1960s of LLM computing"

In both the [[berkeley-ai-hackathon-2024-keynote|Berkeley 2024 keynote]] (where he originally said "~1980s") and the 2025 [[software-is-changing-again|YC talk]] (revised to "~1960s"), Karpathy situates LLMs historically: centralized compute in the cloud, time-shared among users, streamed as tokens in a terminal. The personal-computing revolution for LLMs hasn't happened yet.

> ⚠️ Drift: Karpathy moves the date from ~1980s (Berkeley 2024) to ~1960s (YC 2025). Worth flagging — either he revised his estimate or the time-shared / token-in-terminal situation felt more 1960s-like by 2025.

## Related

- [[software-3-0]] — the authoring side
- [[llama]] — the Linux counterpart
- [[openai]] — the Windows/macOS counterpart
- [[build-for-agents]] — the "ship your docs in machine-readable form" implication
