---
title: "2025 — AI-Assisted Coding Workflow Evolution"
type: source-summary
created: 2026-04-17
updated: 2026-04-17
sources: [2025/4.25.md, 2025/7.5.md, 2025/7.26.md, 2025/8.25.md, 2025/10.27.md, 2025/12.27.md, 2025/12.28.md, 2025/12.29.md]
tags: [ai-assisted-coding, verification-gap, agentic-engineering, code-post-scarcity]
---

# 2025 — The AI-Assisted Coding Workflow (Year-Long Arc)

Eight posts tracing Karpathy's real coding practice across 2025 — from the Apr "over-eager junior intern" workflow to the Dec "I've never felt this much behind" grief-cycle post. Together they map the ground truth that becomes [[agentic-engineering]] in 2026.

## Apr 25 — The seven-step inner loop

Karpathy's personal rhythm for code he *actually cares about* (contrast: vibe coding):

1. Stuff everything relevant into context (`files-to-prompt . -e ts -e tsx ...`).
2. Describe the next **single, concrete** incremental change. Don't ask for code — ask for **approaches with pros/cons**.
3. Pick one approach, ask for first-draft code.
4. **Review / learning phase** — manually pull API docs side-by-side, ask for explanations, wind back and retry.
5. Test. 6. Git commit. 7. Ask for next-step suggestions. Repeat.

> "The emphasis is on keeping a very tight leash on this new **over-eager junior intern savant** with encyclopedic knowledge of software, but who also bullshits you all the time, has an over-abundance of courage and shows little to no taste for good code."

Also proposes replacement terminology — "real coding" as counterpoint to vibe coding. Credits "AI assisted coding" to [[simon-willison]]'s post on vibe coding.

## Jul 5 — Products must expose text, or die

> "Products with extensive/rich UIs, lots of sliders, switches, menus, with no scripting support, and built on opaque binary formats are **ngmi** in the era of heavy human+AI collaboration."

Risk tiers:

| Risk | Examples |
|---|---|
| **High risk** (binary, no text DSL) | Every Adobe product, DAWs, CAD/3D |
| **Medium-high** (partially scriptable) | Blender, Unity |
| **Medium-low** (mostly text, automation ecosystem) | Excel |
| **Low risk** (already all text) | VS Code, Figma, Jupyter, Obsidian |

AI will eventually master human UIs (Operator etc.), but products that wait instead of meeting the tech halfway won't have a good time.

## Jul 5 (cont.) — The verification gap

Core distinction borrowed from GAN terminology:
- **(1) Generation** — make a brush stroke, write a line.
- **(2) Discrimination** — look at the result, judge it.

Discrimination cost by medium:
- **Images**: cheap — grids let your visual GPU parallelize.
- **Text**: expensive — semantic, discrete, precise, must be reasoned about.
- **Audio**: hardest — forced time axis, no parallelization.

> "In coding, LLMs have collapsed (1) to ~instant, but have done very little to address (2). The LLM has to actively work with you to break down problems into little incremental steps, each more easily verifiable. It has to anticipate the computational work of (2) and reduce it as much as possible."

And the punchline for non-coders:

> "The biggest misunderstanding non-coders have about coding: they think coding is about *writing* the code (1). It's not. **It's about staring at the code** (2)."

## Jul 5 (cont.) — ChatGPT model router

Karpathy's own "router" between ChatGPT variants (rare explicit use-case breakdown):

| Model | Use case | Share |
|---|---|---|
| 4o | Simple daily queries | 40% |
| o3 | Hard/important — reasoning model, "if you're not using o3 professionally you're ngmi" | 40% |
| 4.1 | Vibe coding | 10% |
| Deep Research (o3-based) | 10-minute multi-source summaries — **not in the model picker, it's a toggle in Tools** | 10% |

Personal stack bounces across ChatGPT + Claude + Gemini + Grok + Perplexity depending on task.

## Jul 26 — "RLHF to slop"

Single-line aphorism on reward hacking:

> "May your regularizer be strong, lest you RLHF to slop."

## Aug 25 — "Too agentic by default"

Benchmarkmaxxing on long-horizon tasks is pushing LLMs past Karpathy's average use case:

> "In coding, the models now tend to reason for a fairly long time, they have an inclination to start listing and grepping files all across the entire repo, they do repeated web searches, they over-analyze and over-think little rare edge cases even in code that is knowingly incomplete and under active development."

He finds himself stopping them with "*Stop, you're way overthinking this. Look at only this single file. Do not use any tools. Do not over-engineer*." Calls for better mechanisms to signal **stakes/intent**, from "quick spot check" to "go off for 30 minutes, come back when certain."

This is the prehistory of the [[autonomy-slider|autonomy slider]] being pulled *down*, not up.

## Oct 27 — Layered tool stack

A four-layer stack of LLM coding assistance, with usage shares:

| Layer | Tool | Share | Role |
|---|---|---|---|
| 1 | Cursor tab-complete | **~75%** | Bread & butter. High-bandwidth *task specification* — writing code in the right place communicates intent faster than prose. |
| 2 | Highlight + ask for modification | | Surgical edits. |
| 3 | [[claude-code|Claude Code]] / [[openai-codex|Codex]] running alongside | | Larger chunks easy to specify in a prompt. Doesn't run in YOLO mode — ESCs often. |
| 4 | GPT-5 Pro | | Final layer of defense — 10-min runs on the hardest bugs. |

Key observations:
- Agents "don't have a sense of taste" — they over-use try/catch, over-abstract, duplicate instead of factoring helpers.
- Agents won't teach — "it really wants to just write code a lot more than it wants to explain anything along the way."
- Agents are **indispensable** for unfamiliar stacks (Karpathy mentions recently writing some Rust, SQL).
- **Code post-scarcity** is named here:

> "It's the **code post-scarcity era** — you can just create and then delete thousands of lines of super custom, super ephemeral code now, it's ok, it's not this precious costly thing anymore."

## Dec 27 — Debugging detective stories

Appreciation for a longread that "starts with a suspicious loss curve and ends in the Objective-C++ depths of PyTorch MPS backend of `addcmul_` that silently fails on non-contiguous output tensors."

> "I wonder how long before an LLM can do all of this."

The implicit March-of-Nines benchmark for agentic debugging — not synthetic puzzles, actual frame-by-frame investigation across layers of abstraction.

## Dec 28 — The Lutron home-automation vibe

Concrete demonstration of agentic workflow beyond a code editor:

- [[claude-code|Claude Code]] found his Lutron controllers on the local wifi, scanned ports, identified devices.
- Searched the internet, found the system PDF, instructed him which button to press to pair.
- Connected, enumerated all devices (lights, shades, HVAC, motion sensors).
- Turned lights on/off to verify.

> "I am now vibe coding the home automation master command center, the potential is 🔥. And I'm throwing away the crappy, janky, slow Lutron iOS app."

Foreshadows the 2026 [[app-store-outdated|"App Store is outdated"]] argument — ephemeral agent-built replacements for canonical apps.

## Dec 29 — "I've never felt this much behind"

Year-end confessional / PSA:

> "The profession is being dramatically refactored as the bits contributed by the programmer are increasingly sparse and between. I have a sense that I could be 10X more powerful if I just properly string together what has become available over the last ~year and a failure to claim the boost feels decidedly like **skill issue**."

Enumerates the new stack layer that must be mastered **in addition to** the usual ones:

> "agents, subagents, their prompts, contexts, memory, modes, permissions, tools, plugins, skills, hooks, MCP, LSP, slash commands, workflows, IDE integrations — and a need to build an all-encompassing mental model for strengths and pitfalls of fundamentally stochastic, fallible, unintelligible and changing entities suddenly intermingled with what used to be good old fashioned engineering."

> "Some powerful alien tool was handed around except it comes with no manual and everyone has to figure out how to hold it and operate it, while the resulting magnitude 9 earthquake is rocking the profession."

Advice: "experienced devs have a real advantage but only if they rapidly progress through their **grief cycle** and adapt." Rejecting the new layer is a mistake.

This post is the direct emotional precursor to Feb 5 / 25 2026's naming of [[agentic-engineering]] and the "phase shift" observation.

## Synthesis

| Axis | 2025 arc |
|---|---|
| **Workflow** | Tight leash (Apr) → layered tools (Oct) → agentic + humbled (Dec) |
| **Bottleneck** | Generation cheap, **discrimination expensive** ([[verification-gap]]) |
| **Model shape** | Over-agentic by default (Aug) — needs intent signaling |
| **Ergonomics** | Code is text or it's ngmi (Jul) |
| **Mental model** | LLM = over-eager junior intern savant (Apr) → requires grief cycle (Dec) |
| **Economics** | Code post-scarcity (Oct) — ephemeral, throw-away |

## Related

- [[agentic-engineering]] (2026 continuation)
- [[atrophy]]
- [[autonomy-slider]]
- [[verification-gap]]
- [[code-post-scarcity]]
- [[vibe-coding]]
- [[claude-code]], [[openai-codex]], [[cursor]]
- [[build-for-agents]]
- [[simon-willison]]
