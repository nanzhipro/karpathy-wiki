---
title: "App Store Outdated"
type: concept
created: 2026-04-17
updated: 2026-04-17
sources: [2026/2.20.md, 2026/4.5.md]
tags: [product, ui, karpathy]
---

# "App Store Outdated"

Karpathy's thesis (Feb 20 2026) that the discrete-app paradigm — a finite catalog of pre-built apps to choose from — is obsolete once agents can improvise custom software on the spot.

## The founding anecdote

Karpathy wants to lower his resting heart rate from 50 → 45 over 8 weeks. In **one hour**, Claude vibe-codes him a custom cardio dashboard: reverse-engineered the Woodway treadmill cloud API, built the data pipeline, rendered a web UI. It's ~300 lines of code.

## The claim

> "There will never be (and shouldn't be) a specific app on the app store for this kind of thing. I shouldn't have to look for, download and use some kind of a 'Cardio experiment tracker', when this thing is ~300 lines of code that an LLM agent will give you in seconds. The idea of an 'app store' of a long tail of discrete set of apps you choose from feels somehow wrong and outdated when LLM agents can improvise the app on the spot and just for you."

— Karpathy, Feb 20 2026

## The future shape

> "The future are services of **AI-native sensors & actuators** orchestrated via LLM glue into highly custom, ephemeral apps."

Key reframings:

- **Treadmill = sensor** that turns physical state into digital knowledge.
- **Smart lights = actuators** that turn digital intent into physical state.
- **Apps are ephemeral glue** — not artifacts to be discovered, but outputs to be generated.

## What has to be in place

From his Feb 20 frustration:

> "99% of products/services still don't have an AI-native CLI yet. 99% of products/services maintain .html/.css docs like I won't immediately look for how to copy paste the whole thing to my agent to get something done."

- Products expose **CLI / API / MCP** interfaces (not just web UIs with buttons).
- Docs are available as **markdown** or other agent-friendly formats.
- Services ship **Skills** for use with agents.

## The 1-hour → 1-minute ambition

> "Today I am impressed that this random thing took 1 hour (it would have been ~10 hours 2 years ago). But what excites me more is thinking through how this really should have been 1 minute tops. What has to be in place so that it would be 1 minute? So that I could simply say 'Hi can you help me track my cardio over the next 8 weeks', and after a very brief Q&A the app would be up."

**What's needed:** personal context, agent access to sensors/actuators, reusable skill libraries, ongoing maintenance of per-user automations.

## Relation to the Apr 5 "idea file" post

Karpathy generalizes the pattern: instead of sharing apps, **share ideas as text artifacts** — the recipient's agent customizes and builds the specific version. Apps collapse into prompts.

## Related

- [[build-for-agents]]
- [[vibe-coding]]
- [[agentic-engineering]]
- [[llm-knowledge-bases]]
- [[byoai]]
- [[claws]]
