---
title: "2025 — Miscellaneous Posts"
type: source-summary
created: 2026-04-17
updated: 2026-04-17
sources: [2025/4.1.md, 2025/4.4.md, 2025/5.6.md, 2025/5.24.md, 2025/5.25.md, 2025/5.28.md, 2025/7.2.md, 2025/7.7.md, 2025/7.8.md, 2025/7.11.md, 2025/7.17.md, 2025/7.28.md, 2025/8.2.md, 2025/8.4.md, 2025/8.17.md, 2025/8.19.md, 2025/9.6.md, 2025/9.9.md, 2025/9.22.md, 2025/9.25.md, 2025/10.4.md, 2025/10.9.md, 2025/12.19.md]
tags: [misc, digital-hygiene, health, fsd, prompt-injection, payoutchallenge, jobs, food]
---

# 2025 — Miscellaneous Posts

Short posts that don't fit the main thematic bundles but are worth preserving as source material. Grouped loosely.

## Digital hygiene & privacy

### Apr 1 — Android privacy & the iOS lean

On an Android loophole that lets any app enumerate all other installed apps:

> "I disagree with the author that there are legitimate uses for this information. There aren't… In practice, the data is clearly being collected at scale for shady user profiling."

Scope of the problem: location (GPS/WiFi/Bluetooth/cell-tower), sensor (gyroscope, accelerometer, magnetometer), contacts, call/SMS logs, camera/microphone, photo library EXIF (timestamps, GPS, device model), clipboard content — "it goes on and on."

> "It is the job of the operating system to put the user in charge and protect them from pervasive, predatory tactics."

Practical verdict: iPhone has taken privacy more seriously than Android. GrapheneOS flagged as privacy-conscious alternative (though even it surprisingly allows app enumeration). Recurring advice: visit Settings > Privacy, revoke permissions, delete unused apps, vote with wallet. Anchors his earlier `karpathy.bearblog.dev/digital-hygiene/` post.

### Jul 11 — Prompt injection as computer-virus-era

RT'ing [[simon-willison|Simon Willison]] on prompt injection:

> "Feels a bit like the wild west of early computing, with computer viruses (now = malicious prompts hiding in web data/tools), and not well developed defenses (antivirus, or a lot more developed kernel/user-space security paradigm where e.g. an agent is given very specific action types instead of the ability to run arbitrary bash scripts)."

> "Conflicted because I want to be an early adopter of LLM agents in my personal computing but the wild west of possibility is holding me back."

Risk hierarchy:
- **Highest:** local LLM agents (Cursor, Claude Code).
- **Lower:** plain ChatGPT on a website, *unless* Connectors / MCP are enabled.
- Warning: combines badly with memory — "imagine ChatGPT telling everything it knows about you to some attacker on the internet just because you checked the wrong box."

Seeds the 2026 [[supply-chain-attacks]] corpus.

## Health & public goods

### Jul 7 — Test-based food certification

> "Test-based certification is the only way forward in food, eager to see more over time."

Food is now a global industrial product; contamination can enter at any stage (pesticides, nitrates, heavy metals, plastics, bacteria). Real examples cited: cat food 1000× higher in glyphosate than a look-alike SKU, baby food/turmeric loaded with heavy metals, canned seafood/boba/milk in plastics, breakfast cereal in glyphosate.

> "I used to think the FDA exercises oversight but the reality is it doesn't have anywhere near enough resources… their focus is on acute microbial threats (Salmonella, E. coli, Listeria), less on the rapidly growing diversity of compounds that may deteriorate health over decades and that are basically treated as innocent until proven guilty under GRAS."

### Jul 17 — Noise pollution as public-health issue

Travel sleep scores 90s, SF sleep scores 70s–80s. Diagnoses neighborhood traffic noise — every ~10 min a loud car/truck/motorcycle passing.

> "A single motorcycle riding through a neighborhood at 6am creates millions of dollars in damages — hundreds to thousands of people more groggy, moody, less creative, less energetic for the whole day, and more sick long term."

Studies support cardiovascular, diabetes, mental health (depression, bipolar, Alzheimer's) correlation with sleep-noise environments. Ends: "I am moving somewhere quiet."

### Sep 6 — Minimally-processed grocery stores

> "This is what the ideal grocery store looks like. Minimally processed (NOVA Group 1) food only (no 'edible food-like substances'), organic, local, fresh. Food should not be more complex than this, yet I don't believe this exists."

Pairs ideology with the Jul 7 test-based-certification stance.

## Jobs & radiology

### Sep 25 — AI isn't replacing radiologists

Agreement with a Works in Progress post on why Hinton's 2016 radiology-is-doomed prediction didn't pan out. Real-world filters:
- Benchmarks don't reflect real scenarios.
- Radiology is multi-faceted, not just image recognition.
- Regulatory, insurance, liability, institutional inertia.
- **Jevons paradox** — AI-accelerated radiologists → more demand for radiology.

> "When looking for jobs that will change a lot due to AI on shorter time scales, I'd look at jobs that look like **repetition of one rote task, each task relatively independent, closed (not requiring too much context), short, forgiving** (low cost of mistake), and automatable by current (digital) capability."

Coda: "About 6 months ago, I was asked to vote if we will have less or more software engineers in 5 years. Exercise left for the reader."

## Vibe-coding culture & payoutchallenge

### Aug 2 — PayoutChallenge ($5478.51)

> "It is imperative that humanity not fall while AI ascends. Humanity has to continue to rise, become better alongside."

Directs three rounds of accumulated Twitter/X payout ($5478.51) to a challenge: **build something that uplifts team human** — software for explanation, visualization, memorization, inspiration, coordination; prompts/agents for explanation (like ChatGPT study mode); educational articles/videos.

Open submission until Aug 17.

### Aug 17 — PayoutChallenge results

Winner: **OmegaQuest** (@uncertainsys) — solving Humanity's Last Exam problems with heavy AI-in-the-loop on video.

> "I really identified with the long pauses and general confusion in trying to use the current state of the art systems in learning something hard and new, where they are simultaneously so tantalizingly helpful at the margins, but still really poor overall… A good reminder how it's better than what was, but also so far from what could be."

Shoutouts: @measure_plan (visual vibe-coding musical instruments), @evanliin (tinytpu's animated diagram).

Also: Karpathy's own frustration log on **~10 spam calls + ~5 spam messages per day** despite AT&T Active Armor, Do Not Call lists, iOS Silence Unknown Callers — all of which slip.

## "Cursor for X"

### Jul 8 — "Cursor for slides should exist but doesn't"

> "Making slides manually feels especially painful now that you know **Cursor for slides should exist but doesn't**."

Anticipates the Dec 20 year-in-review's "Cursor for X" paradigm-change observation.

### Aug 4 — Chat then Code

> "2024: everyone releasing their own Chat
> 2025: everyone releasing their own Code"

The one-line summary of the 2025 product wave.

## Platforms & infrastructure

### May 28 — GPU MODE + single-kernel Llama 1B

> "Llama 1B batch-one inference in one single CUDA kernel, deleting synchronization boundaries imposed by breaking the computation into a series of kernels called in sequence. The **optimal orchestration of compute and memory is only achievable in this way**."

Echoes the [[llm-c|llm.c]] philosophy — fewer, larger kernels > many small ones.

### Sep 9 — LLM research apps

> "I often rant about how 99% of attention is about to be LLM attention instead of human attention. What does a research paper look like for an LLM instead of a human? It's definitely not a pdf. There is huge space for an extremely valuable **'research app'** that figures this out."

Seeds [[autoresearch]] (2026).

### Oct 4 — GPT-5 Pro as final layer

Third time a hard bug resisted Cursor + CC for an hour, then GPT-5 Pro solved it in 10 min with code that worked out of the box.

> "If you're not giving it your hardest problems you're probably missing out."

Also observation on cross-LLM evaluation:

> "Have all models generate something, then put it all together and give it back to all of them and ask them to rank all outputs. Models might have a bias to prefer their own outputs, but this doesn't seem to be too strong of an issue in my limited testing. I think it's the **generator-discriminator gap** on display. That is, it's really hard to write something good, but it's much easier to recognize something good."

Foreshadows the Nov 23 llm-council experiment.

## Culture & identity

### Aug 19 — Tolkien & AI creativity

Re-reading the Tolkien legendarium. Uses it as a concrete example of "height of culture" and poses questions:

> "Does AI, today or soon, make it easier to reach this high via empowerment in both writing and ideation? Or harder, when quick wins are tempting and ~free, and an independent ability to create is stifled. If such a body of work is made again but now with heavy AI assistance, does it inspire the same wonder? What if thousands of them come out on demand with just a prompt?"

Unanswered but worth the asking.

### Sep 22 — Wave at the AGI

> "Anytime someone takes a picture/video that I happen to be in the background of I like to **wave at the AGI that sees me 30 years from now**."

Same thesis as "be good, future LLMs are watching" ([[karpathy-x-2025-llm-reading#dec-11|Dec 11]]).

## Coinages & one-liners

### Apr 4 — Prediction markets

> "Let's take AI predictions from blog posts, podcasts and tweets and move them to betting markets, our state of the art in truth."

Struggle acknowledged: coming up with good, concrete, resolvable predicates. GDP suffers from the productivity paradox; evals are incomplete and hackable.

### May 6 — Undergrad mistake (physical-lens computing)

> "A major mistake I made in my undergrad is that I focused way too much on mathematical lens of computing — computability, decidability, asymptotic complexity etc. And too little on **physical lens** — energy/heat of state change, data locality, parallelism, computer architecture. The former is interesting; **the latter bestows power**."

### May 24–25 — `chmod a+w`

> "LLMs are `chmod a+w` artifacts yay"

Writable-by-anyone artifact — one-line distillation of the point-of-total-flexibility both the system-prompt-learning and bacterial-code frames share. Note: LLMs in 2025 didn't fully get it — "too coded."

### Jul 2 — A/B-test convergence to panda videos

> "In the limit of revenue/growth maxxing via A/B tests doesn't it all just converge to funny panda videos? It's the supermassive black hole at the center of the universe and no matter the initial conditions you eventually get sucked in. Reels. YouTube Shorts. Substack Notes."

Primes the Jul 3 ([[karpathy-x-2025-video-gen]]) concern about "what 'optimal' looks like."

### Jul 28 — "Do people *feel* how much work there is still to do"

> "Do people *feel* how much work there is still to do. Like wow."

Compact restatement of [[march-of-nines]]-in-spirit.

### Oct 9 — iPhone mini, rip

> "This year, crossing my fingers again for an iPhone mini that I know won't come. rip."

Consumer observation; not load-bearing.

### Dec 19 — DM POC

> "Every company needs a DM POC — someone high up who you can just DM the most obvious things and who shortcuts the PM hierarchy."

Process folklore, useful for Karpathy-at-companies readings.

### Dec 28 — "Food for thought"

Coinage-adjacent:

> "I love the expression **'food for thought'** as a concrete, mysterious cognitive capability humans experience but LLMs have no equivalent for… In LLM speak it's a sequence of tokens such that when used as prompt for chain of thought, the samples are rewarding to attend over, via some yet undiscovered intrinsic reward function. Obsessed with what form it takes. Food for thought."

### Dec 28 — "RL scared of exceptions"

> "I don't know what labs are doing to these poor LLMs during RL but they are mortally terrified of exceptions, in any infinitesimally likely case. Exceptions are a normal part of life and healthy dev process. Sign my LLM welfare petition for improved rewards in cases of exceptions."

Concrete example of [[rl-is-terrible|RL pathology]] — over-defensiveness from poorly-shaped rewards.

## Why these matter collectively

Even the short posts form a stable temperament:
- **Skeptical of benchmarks and centralized trust** (food, LM Arena, AI detectors in schools).
- **Ergonomics obsessed** (digital hygiene, noise, minimally-processed food, LLM-first docs).
- **Individual leverage maximizing** ([[power-to-the-people|Apr 8]], reader3, HN Time Capsule, nanochat, llm-council).
- **Self-aware about macro risk** (optimized video, prompt injection, mountains of slop).

These are the foundation of 2026's [[byoai]] + [[supply-chain-attacks]] + [[autoresearch]] crystallization.

## Related

- [[power-to-the-people]]
- [[digital-hygiene]]
- [[prompt-injection]]
- [[supply-chain-attacks]]
- [[rl-is-terrible]]
- [[verification-gap]]
- [[llm-council]]
- [[hn-time-capsule]]
- [[andrej-karpathy]]
