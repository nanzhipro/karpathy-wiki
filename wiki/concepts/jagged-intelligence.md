---
title: Jagged Intelligence
type: concept
created: 2026-04-17
updated: 2026-04-17
sources: [andrej-karpathy-software-is-changing-again/transcript.md]
tags: [llm-psychology, evaluation, karpathy-coinage]
---

# Jagged Intelligence

Karpathy's task-level framing of [[peaky-capability]]: an LLM solves a PhD-level problem on one request and then insists that 9.11 > 9.9 on the next. The profile isn't just peaky across *domains*; it's peaky across *tasks* in the same conversation.

## Source

- [Karpathy, Software Is Changing (Again)](../sources/software-is-changing-again.md) — "They can do PhD-level problem-solving, and then turn around and tell you 9.11 is bigger than 9.9."

## Relationship to other concepts

- **[[peaky-capability]]** is the macro version (writing < coding; advice < math).
- **Jagged intelligence** is the micro version — task-to-task unreliability within a domain.
- Both are symptoms of LLMs being [[people-spirits|people spirits]]: sampled distributions with different supports across different prompt regions.

## Product implication

You can't trust that a model's strength on Task A generalizes to Task B, even if B looks simpler. This is why [[partial-autonomy-apps]] with fast human verification beat full-automation demos.

## Related

- [[peaky-capability]]
- [[people-spirits]]
- [[autonomy-slider]]
