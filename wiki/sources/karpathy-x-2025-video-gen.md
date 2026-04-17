---
title: "2025-07 — Video Generation (Veo 3 & MirageLSD)"
type: source-summary
created: 2026-04-17
updated: 2026-04-17
sources: [2025/7.3.md, 2025/7.18.md]
tags: [video-generation, veo-3, decart, real-time-diffusion, llm-gui]
---

# 2025-07 — Video Generation: Veo 3 and MirageLSD

Two posts in July 2025 on why video generation is a bigger deal than it looks — especially once it becomes **real-time** and **directly optimizable**.

## Jul 3 — Veo 3 + "video is directly optimizable"

### The macro argument (four points)

> "Very impressed with Veo 3 and all the things people are finding on r/aivideo etc. Makes a big difference qualitatively when you add audio."

1. **Video is the highest-bandwidth input to the brain** — not just for entertainment but also for work/learning (diagrams, charts, animations).
2. **Video is the most easy/fun** — most people don't like reading/writing, it's effortful. Anyone can and wants to engage with video.
3. **The barrier to creating videos is → 0.**
4. **For the first time, video is directly optimizable.**

### Why (4) is the real deal

Until now, video has been: humans expensively create → ranking algorithms decide which to serve.

> "Collectively, 'human creators learning what people like and then ranking algorithms learning how to best show a video to a person' is a very, very poor optimizer. Ok, people are already addicted to TikTok so clearly it's pretty decent, but it's imo nowhere near what is possible in principle."

Veo-class models emit a **differentiable process**. You can now:
- Take arbitrary objectives (engagement, pupil dilation, ad click conversion).
- Crush them with gradient descent.
- Or iteratively optimize prompts via humans or AIs (with parameters frozen) — likely still strong enough.

> "**Why index a finite set of videos when you can generate them infinitely and optimize them directly.**"

### Both promise and alarm

> "I think video has the potential to be an incredible surface for AI → human communication, future AI GUIs etc. Think about how much easier it is to grok something from a really great diagram or animation instead of a wall of text. And an incredible medium for human creativity."

Flip side:

> "But this native, high bandwidth medium is also becoming directly optimizable. Imo, TikTok is nothing compared to what is possible. And **I'm not so sure that we will like what 'optimal' looks like.**"

The darker rhyme with the Jul 2 post ("doesn't it all converge to funny panda videos? — it's the supermassive black hole at the center of the universe").

## Jul 18 — MirageLSD: real-time diffusion video

The companion post — what changes when diffusion video goes **real-time**.

> "Simple video filters are real-time but can only do basic re-coloring and styles. Video diffusion models (Veo and friends) are magic, but they take many seconds/minutes to generate. MirageLSD is **real-time magic**."

Unlike simple filters, diffusion models actually *understand* the feed — they can put hats on heads, light sabers in hands, etc. And they're arbitrarily steerable via text prompts.

### Ideas unlocked

Karpathy's own enumeration:
- Transform camera feeds into alternate realities.
- Direct and shoot your own movies, acting scenes out with props. Real-time → instant feedback/review.
- Vibe-code games around simple spheres/blocks, then use real-time diffusion to texture them into beauty.
- Style any video feed: Skyrim but "MORE EPIC"; DOOM II but modern Unreal quality via prompt; horror movie but "cute, pink, bunnies only."
- Zoom call backgrounds ++.
- Real-time virtual try-on.
- Glasses that cartoonify your vision in real time.
- **Harry Potter Mirror of Erised** — raw feed augmented with your deepest desires as inferred by the AI.

> "I don't know, I'm probably missing the biggest one, so many things!"

### Disclosure

Karpathy is a (very small) angel investor in [[decart|Decart]]. The technology will get very good very fast — "feels general, powerful but it's also technically very difficult."

### Also in the post

Separate thread: Karpathy confirms the YC AI Startup School talk will be released publicly "in the coming weeks" (it drops Jul 19 — see [[karpathy-x-2025-software-paradigm]]). Fun fact: "the name OpenAI didn't exist when I joined — my very first swag t-shirt says 'YC AI Day 1'."

## Why these posts matter

- First serious articulation that video → differentiable → **optimizable** — which makes it a fundamentally new product category, not a better TikTok.
- Seeds the 2025 Nov/Dec [[llm-gui]] argument — video is a component of the missing LLM GUI.
- The "alternate realities" / "Mirror of Erised" framing foreshadows immersive AI interfaces that Apple/Meta headsets gesture at but don't yet deliver.
- Honest about risk: "I'm not sure we will like what 'optimal' looks like" — rare explicit nod to alignment concerns outside the LLM frame.

## Related

- [[video-generation]]
- [[decart]]
- [[miragelsd]]
- [[llm-gui]]
- [[partial-autonomy-apps]]
- [[software-is-changing-again]] (YC talk)
- [[andrej-karpathy]]
