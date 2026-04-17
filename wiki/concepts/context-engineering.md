---
title: Context Engineering
type: concept
created: 2026-04-18
updated: 2026-04-18
sources: [2025/7.25.md]
tags: [prompting, app-layer, karpathy-endorsed]
---

# Context Engineering

The "delicate art and science of filling the context window with just the right information for the next step." Karpathy's preferred term over **prompt engineering** — the latter evokes short task descriptions, the former acknowledges everything real LLM apps actually do.

## The endorsement

[[karpathy-x-2025-build-for-agents|Jul 25 2025]]:

> "+1 for **context engineering** over **prompt engineering**. People associate prompts with short task descriptions you'd give an LLM in your day-to-day use. In every industrial-strength LLM app, context engineering is the delicate art and science of filling the context window with just the right information for the next step."

## What goes in a context window

- Task descriptions and explanations
- Few-shot examples
- RAG — retrieved documents / snippets
- Related multimodal data
- Tools and their schemas
- State and history (and how to **compact** them)

## Too little vs too much

- **Too little / wrong form** → LLM lacks the right context for optimal performance.
- **Too much / irrelevant** → cost up, performance down.

Getting this right is *non-trivial*.

## Science + art

- **Science:** task descriptions, RAG, compaction, tool schemas — measurable craft.
- **Art:** guided by intuition around [[people-spirits|LLM psychology]].

## Part of a thick app layer

Context engineering is **one piece** of an emerging thick layer of LLM-app software that also has to:

- Break up problems into control flows.
- Dispatch calls to LLMs of the right kind and capability.
- Handle generation-verification UIUX flows ([[verification-gap]]).
- Provide guardrails, security, evals, parallelism, prefetching.

## The anti-"ChatGPT wrapper" argument

> "The term 'ChatGPT wrapper' is tired and really, really wrong."

Context engineering is the specific craft that rebuts the thesis "labs will eat all apps." The app layer is **thick** precisely because of what context engineering requires.

## Relation to other concepts

- **[[prompting]]** — the narrower, older term.
- **[[system-prompt-learning]]** — the self-updating, automated frontier of context engineering.
- **[[partial-autonomy-apps]]** — the app layer where context engineering is most load-bearing.
- **[[llm-gui]]** — what context engineering produces for the user is increasingly visual, not textual.

## Related

- [[partial-autonomy-apps]]
- [[verification-gap]]
- [[system-prompt-learning]]
- [[build-for-agents]]
- [[people-spirits]]
