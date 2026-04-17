---
title: "2025-10 / 12 — The nanochat Saga"
type: source-summary
created: 2026-04-17
updated: 2026-04-17
sources: [2025/10.13.md, 2025/10.16.md, 2025/10.21.md, 2025/10.24.md, 2025/12.9.md]
tags: [nanochat, llm101n, pixels-as-input, diffusion-lm, nanogpt-in-space]
---

# 2025-10 / 12 — The nanochat Saga

Five posts across October–December tracking the `nanochat` release, its $1000 scale-up, identity customization, the SpellingBee capability graft, and the diffusion/pixel-input thought experiments it kicked off.

## Oct 13 — nanochat release

The release post:

> "Excited to release new repo: **nanochat**! (it's among the most unhinged I've written)."

Unlike [[nanogpt]] (pretraining only), nanochat is a full-stack, dependency-minimal training + inference pipeline for a ChatGPT clone in **~8,000 lines**. One script on a cloud GPU box, ~4 hours later you talk to your own LLM in a ChatGPT-style web UI.

What the single script does:
- Trains the tokenizer (new Rust implementation).
- Pretrains a Transformer on FineWeb, evaluates CORE score.
- Midtrains on user-assistant conversations (SmolTalk), multiple choice, tool use.
- SFT + evaluates on ARC-E/C, MMLU, GSM8K, HumanEval.
- Optional GRPO RL on GSM8K.
- Efficient inference (KV cache, prefill/decode, Python sandbox for tool use).
- Emits a **single markdown report card** gamifying the whole run.

Scaling waypoints:

| Budget | Time | Notes |
|---|---|---|
| $100 | 4h on 8×H100 | Can talk, write stories/poems, simple QA |
| ~$300 | 12h | Surpasses GPT-2 CORE metric |
| ~$1000 | 41.6h (depth 30) | ≈ GPT-3 Small (125M) FLOPs, 1/1000th of GPT-3. MMLU ~40s, ARC-Easy ~70s, GSM8K ~20s |

Stated goal: "the full **strong baseline** stack into one cohesive, minimal, readable, hackable, maximally forkable repo." Capstone of [[llm101n]].

Link: github.com/karpathy/nanochat, walkthrough: discussions/1.

## Oct 16 — d32 finished + "kindergarten child" framing

The $1000 depth-32 scaleup finished after ~33h. CORE 0.31 (above GPT-2's ~0.26). GSM8K jumped 8% → 20%.

Critical expectation-setting:

> "Talking to micro models you have to imagine you're talking to a **kindergarten child**. They say cute things, wrong things, they are a bit confused, a bit naive, sometimes a little non-sensical, they hallucinate a ton (but it's amusing)."

Why: $100 nanochat is 1/1000th of GPT-3 in params. "There is a reason frontier labs raise billions." Full report: discussions/8.

Side note in the thread (unrelated): observational complaint about modern TV — turn on, wait for 1.5GB update popup, then a 500MB app update, then an account screen. "TV in the 90s: you turn it on, you watch."

## Oct 21 — Identity grafting via synthetic data

nanochat now has a "primordial identity" — knows it's `nanochat d32`, cost $800, was built by Karpathy, can't speak non-English well and *why*.

How: synthetic data generation — ask a bigger LLM cousin to generate conversations matching a spec, then mix them into midtraining/SFT.

> "LLMs have no inherent personality or understanding of their own capabilities because they are not animal-like entities. They don't know what they are. All of it has to be **explicitly bolted on**."

Key engineering challenge: **diversity / entropy** in generated data. Without care, an LLM generates 1000 conversations that are too similar even with high temperature. Example diversity tricks: sampled starting messages, topic lists, few-shot examples for inspiration.

Amusement: nanochat refers to him as "King Andrej Karpathy" — illustrating the blank canvas. Follow-up: full discussion guide on *Infusing identity to your nanochat*.

### DeepSeek-OCR side thread — pixels as input

Same post continues into commentary on the DeepSeek-OCR paper:

> "The more interesting part for me is whether **pixels are better inputs to LLMs than text**. Whether text tokens are wasteful and just terrible, at the input."

Arguments for all-pixel input:
- Better compression → shorter context windows, more efficiency.
- More general information stream (bold, color, images, not just text).
- Bidirectional attention becomes default (more powerful).
- **Delete the tokenizer** — "ugly, separate, not end-to-end… imports all the ugliness of Unicode, byte encodings, security/jailbreak risk, two identical-looking characters as two different tokens."

> "Maybe the User message is images, but the decoder (Assistant) remains text. It's a lot less obvious how to output pixels realistically… or if you'd want to."
>
> "Now I have to fight the urge to side quest an image-input-only version of nanochat."

### Also in post — text diffusion commentary

Appreciation for a short post on discrete diffusion LMs:

> "Autoregression is doing an `.append(token)` to the tokens canvas while only attending backwards, while diffusion is refreshing the entire token canvas with a `.setitem(idx, token)` while attending bidirectionally."

"Human thought naively feels a bit more like autoregression but it's hard to say there aren't more diffusion-like components in some latent space of thought." Resists the urge to side-quest a diffusion nanochat.

## Oct 24 — SpellingBee: grafting capabilities

Karpathy taught nanochat d32 how to count 'r' in strawberry. Full guide at discussions/164.

Technique: a new synthetic task `SpellingBee` that generates user requests + ideal assistant solutions. Mix into midtraining/SFT; optional RL on top.

Key engineering details:
- Diversity in user prompts.
- Careful tokenization — for small models, whitespace matters, and **reasoning must be spread across many tokens**: standardize the word, spell it out (to break up tokens), iterate with explicit counter.
- Encourage two solution modes: manual in-head arithmetic AND Python tool use. Current synthetic data is "clean" — no mistakes/recovery; could simulate errors or use RL.

> "If nanochat was much bigger, you'd expect this capability to more easily 'pop out'. But because nanochat d32 'brain' is the size of a ~honeybee, we have to over-represent this in the data."

## Dec 9 — The random.seed() footgun

> "In the Python docs of `random.seed()` def, we're told 'If a is an int, it is used directly.' But if you seed with **3 or -3**, you actually get the exact same rng object, producing the same streams."

Full detective work:
- CPython `_randommodule.c` line 321: `n = PyNumber_Absolute(arg);` — drops the sign bit.
- Comment "This algorithm relies on the number being unsigned" is **wrong/misleading** — Mersenne Twister MT19937 has 19,937 bits of state; the sign bit could have been mixed in (e.g. `n → 2*abs(n) + int(n<0)`).
- Python's `random` contract: *same seed → same sequence*. But **no guarantee different seeds → different sequences** — a gap many ML codepaths implicitly assume.

In nanochat, Karpathy had been using the sign of seeds to separate train/test — which accidentally made `train == test`.

Thread also includes a preemptive clarification to Apr 25 (`4.25.md`) — he was NOT telling people to use old-style "you are an expert Swift programmer" prompting techniques.

## Through-line

nanochat evolved from release → scale-up → personality → capability grafting → real-world footgun. Each post is a working example of the [[agentic-engineering]] inner loop on a small enough substrate that a single person can own it end-to-end — which is exactly the [[ramps-to-knowledge|ramp]] pitch.

Side quests spawned but not (yet) taken:
- Image-only-input nanochat (pixels > tokens).
- Diffusion-trained nanochat.

## Related

- [[nanochat]] — the entity page
- [[nanogpt]]
- [[llm101n]]
- [[ramps-to-knowledge]]
- [[pixels-as-input]]
- [[discrete-diffusion]]
- [[microgpt]] (2026 continuation in miniature)
- [[andrej-karpathy]]
