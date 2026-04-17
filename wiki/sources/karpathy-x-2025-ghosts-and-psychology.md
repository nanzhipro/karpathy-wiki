---
title: "2025-10 / 11 / 12 — Summoning Ghosts Origin + LLM Psychology"
type: source-summary
created: 2026-04-17
updated: 2026-04-17
sources: [2025/10.2.md, 2025/11.22.md, 2025/12.8.md]
tags: [ghosts, llm-psychology, simulator, karpathy-coinage]
---

# 2025-10 / 11 / 12 — Summoning Ghosts (Origin) & LLM Psychology

The three X posts in which Karpathy crystallized the *people-spirits / ghosts-not-animals* frame. The Oct 2 post is the direct origin of the Dwarkesh-interview title.

## Oct 2 — Sutton pod review & the Ghost coinage

Response to Richard Sutton's Dwarkesh podcast, in which Sutton argues LLMs are **not** "bitter-lesson pilled" — they're trained on finite human data.

Karpathy's framing:

- **Sutton's world:** the classical "child machine" (Turing). A single algorithm, embodied, learning purely from experience. No pretraining, no SFT. Animals as the existence proof.
- **Karpathy's counter:** animals are *not* blank-slate learners. A baby zebra runs within minutes of birth — that prior is encoded in DNA by evolution, a computation we can't rerun. "Pretraining is our crappy evolution" — our substitute cold-start, training billions of parameters via supervised imitation of internet text.

### The coinage

> "Today's frontier LLM research is not about building animals. It is about **summoning ghosts**. Ghosts are a fundamentally different kind of point in the space of possible intelligences. They are muddled by humanity. Thoroughly engineered by it. They are these imperfect replicas, a kind of statistical distillation of humanity's documents."

### Why "ghosts"

Karpathy's follow-up enumerating why the analogy is better than alternatives:
1. Digital artifacts, no embodiment (unlike animals).
2. Echo/distillation of the living.
3. Aura of mystery — we don't fully understand them.
4. Training = summoning ritual on a GPU megastructure. "Demon" was wrong — presupposes evil.
5. Nod to "ghost in the machine" (Descartes, *Ghost in the Shell*).

Weak point: ghosts are almost always *spooky* — unfair to LLMs.

> "Ghosts : animals :: planes : birds."

### Also in this post

- Appreciation for **Tinker** (Thinking Machines Lab): a post-training library that "slices complexity" — you keep 90% algorithmic control, they handle infra/forward-backward/distributed. See [[tinker]].
- Observation: **finetuning is about scope narrowing, not stylization.** Spam filters are the extreme case; DAG pipelines with mixed prompted + finetuned LLMs will be common.

## Nov 22 — Animal vs LLM optimization pressure

The quantitative restatement of the ghosts argument. The space of intelligences is vast; animals and LLMs are two points shaped by different pressures.

| Pressure axis | Animals | LLMs |
|---|---|---|
| Substrate | Brain tissue + nuclei | Transformers |
| Algorithm | SGD-free, ??? | Gradient descent |
| Operating loop | Continuous, embodied, learns at test time | Fixed weights, boot-process-die per context |
| Selection pressure | Evolution (survival of tribe in jungle) | Commercial evolution (solve-the-problem, get-the-upvote) |
| Core supervision | Self-preservation, social dynamics, exploration | Imitation of text → RL on puzzles → RLHF A/B tests |

Key insight: LLM "jaggedness" is rooted in **there is no consequence for failing a task**. Animals failing = death, so their optimization pressure is general-adversarial. LLMs fail 'r in strawberry' because it doesn't matter. Multi-task generalization is a side effect of multi-task evolution — not automatic from imitation.

> "LLMs are humanity's 'first contact' with non-animal intelligence."

People who build good models of this entity will reason about it better. People who anthropomorphize will mispredict.

## Dec 8 — LLMs as simulators, not entities

Practical consequence of the ghost frame.

> "Don't think of LLMs as entities but as simulators. When exploring a topic, don't ask 'What do you think about xyz'. There is no 'you'. Next time try: 'What would be a good group of people to explore xyz? What would they say?'"

Follow-up:
- There *is* an engineered "you" — the personality trained via SFT + RLHF. But it's **bolted on**, not emergent in the way a person's identity forms. The simulator underneath is the primitive.
- More subtle in non-verifiable domains (opinions, advice) than verifiable ones — because in those domains the "you" has no rigorous ground truth.

This frame is the practical toolkit version of [[people-spirits]].

## Synthesis

Oct 2 names it. Nov 22 explains the mechanism. Dec 8 gives users a playbook. The Dwarkesh interview a week later (Oct 2025) then consolidates it in long-form.

## Related

- [[animals-vs-ghosts]] — the concept
- [[people-spirits]] — the parallel coinage from the YC talk
- [[summoning-ghosts-not-animals]] — the Dwarkesh podcast
- [[llm-as-simulator]]
- [[intelligence-optimization-pressure]]
- [[tinker]]
- [[andrej-karpathy]]
