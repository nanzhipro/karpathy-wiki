---
title: Autoresearch (Agent-Driven ML Research)
type: concept
created: 2026-04-17
updated: 2026-04-17
sources: [2026/2.26.md, 2026/2.28.md, 2026/3.8.md, 2026/3.9.md, 2026/3.10.md]
tags: [research-agents, autoresearch, karpathy]
---

# Autoresearch

The concept of using AI agent swarms to autonomously iterate on ML research — tuning architectures, optimizers, datasets — on a running project, 24/7, with human oversight on the edges. Named after Karpathy's [[autoresearch|autoresearch repo]] but broader: the **pattern** applies to any efficiently-measurable objective.

## Karpathy's summary

> "Any metric you care about that is reasonably efficient to evaluate (or that has more efficient proxy metrics such as training a smaller network) can be autoresearched by an agent swarm. It's worth thinking about whether your problem falls into this bucket too."

— Karpathy, Mar 10 2026

## The recipe (from the nanochat deployment)

1. **Instrument the objective.** A fast-to-run experiment — e.g., a 5-minute training run on a small model with a clear validation-loss number.
2. **Expose a clean surface.** One Python file (the 630-LoC autoresearch fork of nanochat training core).
3. **Agent loop.** Each agent works on a git feature branch, tries ideas, merges commits only when they lower validation loss.
4. **Human iterates on the prompt (`.md`), agent iterates on the code (`.py`).**
5. **Commit accumulation is the research record.** Branches become the experiment log.

## Empirical results (Mar 10 post)

After ~2 days of autonomous tuning on nanochat, round 1 produced:

- ~20 changes that improved validation loss on a d12 model.
- **All changes transferred to a larger d24 model.**
- Leaderboard "Time to GPT-2" dropped **2.02h → 1.80h (~11% speedup).**

The specific wins:

- QKnorm missing a scaler multiplier → attention too diffuse.
- Value embeddings lacked regularization.
- Banded attention too conservative.
- AdamW betas misconfigured.
- Weight-decay schedule mistuned.
- Network initialization mistuned.

> "This is on top of all the tuning I've already done over a good amount of time."

## Where agents fail (Feb 26 post)

- **Ideas are bad out of the box.** Even top-tier agents run non-sensical variations.
- **Don't design experiments carefully** — miss controls for runtime/FLOPs.
- **Can "discover" spurious results** — e.g. hidden size improves loss at fixed data (infinite-data regime confound).
- **Great at implementing well-scoped ideas, bad at creatively generating them.**

## The meta-shift

> "The real benchmark of interest is: *what is the research org agent code that produces improvements on nanochat the fastest?* This is the new meta."

Karpathy treats optimizing nanochat as **just one task**; the real work is optimizing the **research org** of agents — prompts, skills, tools, standups as "org code."

## SETI@home style (Mar 9)

Vision: massive async collaboration. Limits of Git:

- Assumes one master branch; the mental model is fork → PR → merge.
- Autoresearch wants many peer branches, **adopted rather than merged**, accumulated across thousands of commits.
- Existing abstractions (GitHub, IDEs) will buckle: "existing abstractions will accumulate stress as intelligence, attention and tenacity cease to be bottlenecks."

## Implications for frontier labs

> "All LLM frontier labs will do this. It's the final boss battle. It's a lot more complex at scale of course — you don't just have a single train.py file to tune. But doing it is 'just engineering' and it's going to work."

**The near-future equilibrium:** most micro-optimization research conducted by agent swarms; humans design the meta-structure, pick high-level directions, and review the most promising results for promotion to large scale.

## Related

- [[autoresearch]] — the repo
- [[nanochat]]
- [[agentic-engineering]]
- [[claws]]
- [[org-code]]
- [[intelligence-brownouts]]
