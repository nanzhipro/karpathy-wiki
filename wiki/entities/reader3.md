---
title: Reader3
type: entity
created: 2026-04-18
updated: 2026-04-18
sources: [2025/11.18.md]
tags: [tool, karpathy-project, llm-reading]
---

# Reader3

Karpathy's personal reader tool for working through books and papers alongside an [[llm-os|LLM]]. Announced [[karpathy-x-2025-llm-reading|Nov 18 2025]].

## What it is

A minimal local reader with three panes: original text, an LLM-generated companion (explanation, background, summary), and a chat window anchored to the current selection.

## The workflow Karpathy uses

Three passes:
1. **Own read** — form your own understanding first.
2. **LLM pass** — ask the LLM to explain, summarize, fill gaps.
3. **Chat pass** — interrogate specific passages, compare to adjacent ideas.

The design guards against [[atrophy]]: the LLM is a *second* reader, not the first.

## Why it exists

Karpathy is a [[karpathy-x-2025-llm-reading|serial reader]] and wanted a workflow that leveraged LLMs without collapsing into "just ask the LLM what it says." Reader3 makes the own-read step structurally primary.

## Related

- [[galaxy-brain-reasoning]]
- [[atrophy]]
- [[hn-time-capsule]]
- [[andrej-karpathy]]
