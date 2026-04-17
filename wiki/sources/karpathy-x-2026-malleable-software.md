---
title: "2026-02 — Malleable Software: microGPT, Bacterial Code, App-Store Obsolescence, Token Tsunami"
type: source-summary
created: 2026-04-17
updated: 2026-04-17
sources: [2026/2.12.md, 2026/2.17.md, 2026/2.20.md, 2026/2.21.md]
tags: [software-malleability, bacterial-code, karpathy]
---

# 2026-02 — Malleable Software

Four Feb 2026 posts with a shared thread: **agents make software more liquid.** Libraries, app stores, even programming languages are feeling the pressure.

## Sources

- **Feb 12** — microGPT in 243 (then 200) lines + "DeepWiki MCP + GitHub CLI to yoink functionality" + **bacterial code**.
- **Feb 17** — Programming languages and LLMs; Rust is "nowhere near optimal for LLMs as a target language."
- **Feb 20** — *Bespoke software*: one-hour vibe-coded cardio dashboard; **app store obsolete**.
- **Feb 21** — *Tsunami of tokens*: memory+compute orchestration puzzle ([[matx|MatX]]); **build for agents via CLIs**.

## The microGPT achievement (Feb 12)

Reproduces [[nanogpt]]'s essentials in **200 lines of pure, dependency-free Python**. Karpathy's compression claim:

> "This is the *full* algorithmic content of what is needed. Everything else is just for efficiency. I cannot simplify this any further."

Structure (after the test-time-compute re-derivation): Column 1 — dataset / tokenizer / autograd; Column 2 — GPT model; Column 3 — training / inference.

## Bacterial code (Feb 12)

Introduces a new aesthetic for agent-consumable software:

- **less tangled**
- **more self-contained**
- **more dependency-free**
- **more stateless**
- **easier to rip out from the repo**

He uses DeepWiki + GitHub CLI to **yoink fp8 training** out of torchao into nanochat — a 150-line self-contained replacement that runs 3% faster. Quote:

> "Libraries are over, LLMs are the new compiler."

## Programming languages reconsidered (Feb 17)

> "LLMs are *especially* good at translation compared to de-novo generation because 1) the original code base acts as a kind of highly detailed prompt, and 2) as a reference to write concrete tests with respect to."

Implications:
- C → Rust ports gather momentum because the LLM can translate with tests as the oracle.
- **Rust itself is not optimal as an LLM target language.** What is? (Open question he flags.)
- "It feels likely that we'll end up re-writing large fractions of all software ever written many times over."

## App-store obsolescence (Feb 20)

Concrete example: he wants to lower his resting heart rate from 50 → 45 over 8 weeks. In an hour, Claude vibe-codes a **custom cardio dashboard** that reverse-engineers the Woodway treadmill cloud API, processes data, renders a web UI.

His thesis:

> "There will never be (and shouldn't be) a specific app on the app store for this kind of thing. I shouldn't have to look for, download and use some kind of a 'Cardio experiment tracker', when this thing is ~300 lines of code that an LLM agent will give you in seconds. The idea of an 'app store' of a long tail of discrete set of apps you choose from feels somehow wrong and outdated when LLM agents can improvise the app on the spot and just for you."

> "The future are services of AI-native sensors & actuators orchestrated via LLM glue into highly custom, ephemeral apps."

99% of products/services still don't have AI-native CLIs. His complaint: *"What am I a computer? You do it. Or have my agent do it."*

## Tsunami of tokens (Feb 21)

> "With the coming tsunami of demand for tokens, there are significant opportunities to orchestrate the underlying memory+compute *just right* for LLMs."

Two camps in hardware:

- **HBM-first (NVIDIA-adjacent).** Large off-chip DRAM capacity, limited bandwidth ("long straw").
- **SRAM-first (Cerebras/[[matx|MatX]]-adjacent).** Fast on-chip memory, low capacity.

The workflow hardest for both simultaneously: **long-context agentic inference decode.** He calls it "today's most interesting intellectual puzzle with the highest rewards."

## CLIs as agent-native legacy (Feb 21)

> "CLIs are super exciting precisely because they are a 'legacy' technology, which means AI agents can natively and easily use them, combine them, interact with them via the entire terminal toolkit."

Closes with: **"It's 2026. Build. For. Agents."**

## Related

- [[bacterial-code]]
- [[microgpt]]
- [[deepwiki]]
- [[app-store-outdated]]
- [[build-for-agents]]
- [[matx]]
- [[model-context-protocol]]
