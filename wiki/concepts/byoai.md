---
title: BYOAI (Bring Your Own AI)
type: concept
created: 2026-04-17
updated: 2026-04-17
sources: [2026/4.5.md]
tags: [personalization, data-sovereignty, karpathy-coinage]
---

# BYOAI — Bring Your Own AI

Karpathy's Apr 5 2026 stance on personalization: rather than letting AI providers silently accumulate memory about you in their systems, **keep your data in your own files and plug any AI you want into it.**

## The four properties

> "This approach to personalization puts *you* in full control. The data is yours. In Universal formats. Explicit and inspectable."

— Karpathy, Apr 5 2026

1. **Explicit.** The memory artifact (your wiki) is navigable. You can see exactly what the AI does and does not know about you.
2. **Yours.** Data on your local computer. No provider has exclusive access; nothing is locked in.
3. **File over app.** Universal formats — markdown, images. Unix toolkit applies. Any tool / LLM / CLI / fine-tune can operate on them.
4. **BYOAI.** Plug Claude, Codex, OpenCode — or an open-weights fine-tune on your wiki — into the same data. Swap freely. "Keep the AI companies on their toes."

## Why it beats provider-side memory

From his Mar 27 observation on LLM memory overfit:

> "A single question from 2 months ago about some topic can keep coming up as some kind of a deep interest of mine with undue mentions in perpetuity."

With BYOAI, you can **see exactly which markdown file encoded that "interest,"** edit it, delete it, reweight it. With provider-side memory, you can't.

## What counts as "knowing you"

- **Context-level knowing** — the LLM reads your wiki per query.
- **Weight-level knowing** — fine-tune an open-weights model on your wiki so personalization lives in parameters. Karpathy flags this as the natural next step.

## The systemic bet

> "'Agent proficiency' is a CORE SKILL of the 21st century. These are extremely powerful tools — they speak English and they do all the computer stuff for you. Try this opportunity to play with one."

BYOAI is the stance that agent proficiency should be **portable across providers** and **inspectable by the user**, not a walled-garden accumulation.

## Tensions

- **Simplicity.** BYOAI requires users to manage directories and files. Karpathy concedes this but argues agents themselves can absorb most of the operational cost.
- **Security.** Your local data is your attack surface — see [[supply-chain-attacks]]. Local-first isn't automatically safer; it needs hygiene.
- **Model quality.** An open-weights model fine-tuned on your wiki may lag a frontier lab's latest. BYOAI relies on open weights staying close to the frontier ([[deepseek-v3-2|DeepSeek]], [[llama|LLaMA]]).

## Related

- [[llm-knowledge-bases]]
- [[cognitive-core]]
- [[bacterial-code]]
- [[build-for-agents]]
- [[deepseek-v3-2]], [[llama]]
