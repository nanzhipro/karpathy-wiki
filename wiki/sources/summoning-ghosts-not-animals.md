---
title: We're Summoning Ghosts, Not Building Animals (Dwarkesh Interview)
type: source-summary
created: 2026-04-17
updated: 2026-04-17
sources: [andrej-karpathy-were-summoning-ghosts-not-building-animals/transcript.md]
tags: [agi, rl, self-driving, education, cognitive-core, march-of-nines, karpathy]
---

# We're Summoning Ghosts, Not Building Animals

**Speaker:** [[andrej-karpathy|Andrej Karpathy]] (interviewed by [[dwarkesh-patel|Dwarkesh Patel]])
**Venue:** *Dwarkesh Podcast* (October 17, 2025)
**Original source:** `raw/youtube-transcript/dwarkesh-patel/andrej-karpathy-were-summoning-ghosts-not-building-animals/transcript.md`
**Format:** long-form interview, ~2h25m

## Thesis

AGI is still roughly a decade away. The headline coinage: **we are not building animals — we are summoning ghosts.** Animals are shaped by billions of years of evolution, born with enormous amounts of hardware-encoded prior ("zebra walks in minutes"). LLMs are fully digital artifacts trained by imitation of human text — a different species entirely, with a different failure profile, and a different path to generality. Treating them as near-animals (or near-humans) misreads what they are and what's needed next.

## Key Claims

1. **The [[decade-of-agents|decade of agents]], not the year of agents.** Karpathy's timeline: "roughly a decade" to AI that could plausibly be hired as an intern. Agents today are impressive demos that collapse under real work — they lack continual learning, persistent memory, robust multimodality, and computer-use reliability. The list of missing pieces is long and each is hard. *(single-source, consistent with [[software-is-changing-again]])*
2. **"Summoning ghosts, not animals."** [[animals-vs-ghosts]]. Richard Sutton's bitter-lesson / animal-intelligence framing ("learn like a baby animal") misses that LLMs start from a fully-formed distillation of human output and must be *tuned*, not *grown*. Evolution is expensive; we can't run it in our lifetime; the ghost path is the tractable one. *(coinage)*
3. **Reinforcement learning is terrible, but everything else is worse.** [[reinforcement-learning|RL]] is "sucking supervision through a straw" — a single scalar reward on a rollout broadcast back to every token, good or bad, in that rollout. The result: noisy credit assignment, catastrophic reward hacking, and "silently collapsed" model distributions where jokes converge to three jokes and ideation flattens. Process-based supervision (LLM-judge intermediate steps) is closer to how humans learn but opens new hacking surfaces. *(see [[rl-is-terrible]], [[model-collapse]])*
4. **LLMs have distinctive [[llm-cognitive-deficits|cognitive deficits]].** (a) Memorization masquerading as reasoning — LLMs over-index on training distributions; Karpathy cites the *Art of Problem Solving* as the kind of book that teaches reasoning from solutions. (b) No real ideation diversity — sampling a hundred jokes gets you three. (c) No consolidation / sleep — humans distill daily experience into weights and a clean context; LLMs don't. (d) Context is working memory, weights are long-term memory — but context drift is still an open problem. *(analytical)*
5. **The [[cognitive-core|cognitive core]] is the right target.** A much smaller model (~1B parameters feels right) that is *less knowledgeable* but *more reasoning-dense* — an "algorithm of thinking" that can learn on the fly through tool use and retrieval. Today's frontier models are overfit to memorized knowledge; the prior-free core is what agent work actually needs. *(single-source forecast)*
6. **AGI will blend into the previous ~2.5 centuries of ~2% GDP growth.** The industrial revolution metaphor: no single invention moved the dial — what moved it was broad diffusion across the economy. AGI will do the same. Don't expect a discontinuity; expect a continuation. *(macro claim)*
7. **Self-driving took long because of the [[march-of-nines]].** Each "nine" of reliability (90% → 99% → 99.9% → ...) is a separate project of equal magnitude. Karpathy traces his 2013 Waymo ride, his five years at Tesla (2017–2022), and today's Waymo commercial deployments — 12 years in, still short of full autonomy at scale. The lesson generalizes: *demos are 90% of the way; products are the remaining nines.* *(experiential)*
8. **LLMs will transform education by building "ramps to knowledge."** Karpathy's current project [[eureka]] (the "Starfleet Academy" / "gym for the mind") is about pedagogy at scale: LLMs as great 1-1 tutors personalized to the learner. He references his own teaching work — [[cs231n]], [[zero-to-hero]], [[nanogpt]], [[micrograd]], [[nanochat]] (~8k lines of code; a "strong baseline" end-to-end) — as examples of [[ramps-to-knowledge|ramps]] that take a beginner from zero to operational understanding without unnecessary cliff. *(single-source, longest segment of the interview)*

## Structure of the Interview (Dwarkesh's Chapters)

1. AGI is still a decade away (0:00–30:33)
2. LLM cognitive deficits (30:33–40:53)
3. RL is terrible (40:53–50:26)
4. How do humans learn? (50:26–1:07:13)
5. AGI will blend into 2% GDP growth (1:07:13–1:18:24)
6. ASI (1:18:24–1:33:38)
7. Evolution of intelligence & culture (1:33:38–1:43:43)
8. Why self-driving took so long (1:43:43–1:57:08)
9. Future of education (1:57:08–2:26:08)

## Notable Quotes

> "We're not building animals, we're summoning ghosts."

> "Reinforcement learning is sucking supervision through a straw."

> "It's a noisy supervision signal. You do a rollout, you get one scalar at the end — pass or fail — and you broadcast that scalar to every token along the way. The ones that were good get reinforced; the ones that were bad get reinforced too, if the rollout happened to succeed."

> "Every nine is a constant amount of work."

> "I think AGI is about a decade away. Not a year away. A decade."

> "Models today are kind of silently collapsed... you ask for a joke and you get one of three jokes."

> "What I actually want is a cognitive core. Stripped of world knowledge, but with the algorithm of thinking — so it can pick up the knowledge via tool use when it needs to."

> "I think pedagogy at scale is the thing. The great tutor is the thing Bloom's two-sigma paper is about. We can now build that for real."

## Named Entities & References

- [[dwarkesh-patel|Dwarkesh Patel]] — interviewer
- [[waymo]] — cited as deep self-driving benchmark
- [[tesla]] — Karpathy's 2017–2022 employer, Autopilot reference for [[march-of-nines]]
- [[openai]] — founding team member
- Richard Sutton — foil: "build animals" / bitter-lesson
- Carl Shulman — prior interview guest Karpathy references on AGI timelines
- Quintin Pope — referenced on shard theory / biological intelligence
- Nick Lane — referenced on evolution of cells (the "origin of life" is the hard step)
- Andy Matuschak — referenced on spaced repetition / education
- Gwern — referenced on model psychology
- [[claude-code]], GPT-5 Pro, [[deepseek-v3-2]] — frontier tools Karpathy personally uses
- [[nanochat]], [[micrograd]], [[nanogpt]], [[cs231n]], [[zero-to-hero]] — Karpathy's own teaching ramps
- Bloom's two-sigma paper — cited as the aspiration for 1-1 AI tutoring
- [[eureka]] — Karpathy's current AI-education venture ("Starfleet Academy")

## Concepts Introduced / Reinforced

- [[animals-vs-ghosts]] — the interview's headline framing
- [[rl-is-terrible]] — RL as "sucking supervision through a straw"
- [[model-collapse]] — silent distributional narrowing from RLHF/RL
- [[cognitive-core]] — stripped-down reasoning-dense model
- [[llm-cognitive-deficits]] — memorization, no ideation, no consolidation
- [[decade-of-agents]] — timeline claim, consistent with [[software-is-changing-again]]
- [[march-of-nines]] — why self-driving (and agents) take a decade
- [[ramps-to-knowledge]] — Karpathy's pedagogical philosophy
- [[in-context-learning]] as working memory vs. weights as long-term memory
- [[agi-blends-into-2-percent-growth]] — macro-economic framing

## Open Questions

- Is "silently collapsed" empirically measurable, or a vibe? Karpathy asserts distributional narrowing but offers no metric.
- If the [[cognitive-core]] is the target, does current RL pointed at verifiable rewards actively *harm* that goal (by overfitting reasoning to narrow evals)?
- Does Karpathy's 1B-parameter cognitive-core estimate match any published frontier result, or is it gut-feel?
- How does the "decade of agents" square with the pace of progress 2023–2026? Does Karpathy explicitly commit to specific benchmarks?

## My Reading (commentary)

The most important move in this interview is decoupling *LLM psychology* from *human* or *animal* psychology. Once you accept "ghost," the list of needed pieces (continual learning, consolidation, persistent memory, prior-free reasoning core) reads less like deficits and more like *missing subsystems*. The [[march-of-nines]] argument is also the most underappreciated claim in AI discourse — it applies directly to coding agents, not just self-driving, and it predicts the timeline Karpathy keeps citing. Taken together with [[software-is-changing-again]], Karpathy's public position is remarkably consistent: useful products now, full autonomy in ~10 years.
