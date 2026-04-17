---
title: "2025-07-27 — Cognitive Core (Full Spec)"
type: source-summary
created: 2026-04-17
updated: 2026-04-17
sources: [2025/7.27.md]
tags: [cognitive-core, on-device, personal-computing, karpathy-coinage]
---

# 2025-07-27 — The Cognitive Core (Full Spec)

The canonical Karpathy post defining [[cognitive-core]] — the always-on, on-device LLM kernel of personal computing.

## The thesis

> "The race for LLM **cognitive core** — a few billion param model that maximally sacrifices encyclopedic knowledge for capability. It lives always-on and by default on every computer as the kernel of LLM personal computing."

## The crystallizing feature set

1. **Natively multimodal** — text / vision / audio at both input and output.
2. **Matryoshka-style architecture** — a capability dial at test time.
3. **Reasoning, also with a dial** (system 2).
4. **Aggressively tool-using.**
5. **On-device finetuning LoRA slots** for test-time training, personalization, and customization.
6. **Delegates and double-checks** with cloud oracles when internet is available — not as a crutch, as a specialist referral.

## Knowledge vs. capability tradeoff

> "It doesn't know that William the Conqueror's reign ended in September 9 1087, but it vaguely recognizes the name and can look up the date. It can't recite the SHA-256 of empty string, but it can calculate it quickly."

The point is not amnesia — it's **a different storage strategy**. Encyclopedia → retrieval. Identity + reasoning + tool use → weights.

## Why on-device matters

What it gives up in raw capability and world knowledge it gets back in:

- Low interaction latency (critical for multimodal).
- Direct / private access to local data and state.
- Offline continuity.
- **Sovereignty** — "not your weights, not your brain."

> "Many of the same reasons we like, use and buy personal computers instead of having thin clients access a cloud via remote desktop."

## Why this post matters

- Turns [[cognitive-core]] from a passing phrase (present in earlier 2024–25 talks) into a spec engineers can build toward.
- The matryoshka + tool-use + LoRA-slot shape **directly anticipates** the 2026 [[byoai|BYOAI]] stance — locally runnable, swappable across providers.
- The "delegate to cloud oracles" pattern is the same autonomy-slider logic ([[autonomy-slider]]) applied to the model itself.
- Feeds into [[intelligence-brownouts]] (a personal cognitive core is one answer).

## Related

- [[cognitive-core]] — concept page
- [[byoai]] — the 2026 continuation
- [[matryoshka-representation-learning]]
- [[llm-os]]
- [[intelligence-brownouts]]
- [[andrej-karpathy]]
