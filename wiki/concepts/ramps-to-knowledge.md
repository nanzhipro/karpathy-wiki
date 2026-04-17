---
title: Ramps to Knowledge
type: concept
created: 2026-04-17
updated: 2026-04-17
sources: [andrej-karpathy-were-summoning-ghosts-not-building-animals/transcript.md, andrej-karpathy-berkeley-ai-hackathon-2024-keynote/transcript.md]
tags: [pedagogy, education, karpathy]
---

# Ramps to Knowledge

Karpathy's pedagogical metaphor: good teaching is the construction of a **ramp** — a carefully graded path from where the learner stands to where the concept lives — not a cliff you drop material off of. His own course catalog is a concrete illustration.

## Sources

- [Karpathy, Summoning Ghosts](../sources/summoning-ghosts-not-animals.md) — the ramp framing in the context of his Eureka education project.
- [Karpathy, Berkeley SkyDeck Keynote](../sources/berkeley-ai-hackathon-2024-keynote.md) — the 10,000-hours context: ramps accelerate the climb.

## The ramp hierarchy Karpathy built

| Project | Audience | Line count | Purpose |
|---------|----------|-----------|---------|
| [[micrograd]] | Coding beginner | ~100 Python | "What is a gradient, mechanically?" |
| [[nanogpt]] | Novice ML | ~300 Python | "What is a transformer, mechanically?" |
| [[nanochat]] | Practitioner | ~8k | "What is a full training pipeline?" |
| [[llm-c]] | Systems/CUDA | ~3k C/CUDA | "What is the metal under PyTorch?" |

Each tier strips comfort and builds directly on the prior one. A learner who can read micrograd can read the loop in nanoGPT; a learner comfortable with nanoGPT can trace llm.c's kernels.

## Design principles (extracted from Karpathy's talks)

1. **Keep the prerequisite graph shallow.** The ramp dies if one step requires five unmet concepts.
2. **Minimize code, maximize fidelity.** Small enough to read end-to-end; real enough that finishing it teaches the thing.
3. **Expose the next ramp.** Each project points toward the next — not a dead end.
4. **Model the process, not just the artifact.** The lecture videos show the *writing*, not the finished code.

## Why ramps matter at scale

- AGI tutors ([[eureka|Eureka]]) are the long-term vision: an AI that constructs a ramp per student, per concept, in real time.
- [[10000-hours]] shapes the ceiling of what any learner can reach; ramps lower the cost per hour and raise the hours' information density.

## Related

- [[eureka]]
- [[micrograd]], [[nanogpt]], [[nanochat]], [[llm-c]]
- [[10000-hours]]
- [[zero-to-hero]] — Karpathy's YouTube series, the filmed form of the ramp
