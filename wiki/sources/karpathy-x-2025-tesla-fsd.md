---
title: "2025 — Tesla FSD (HW4 Test Drive, Self-Driving Optimism)"
type: source-summary
created: 2026-04-17
updated: 2026-04-17
sources: [2025/7.24.md, 2025/11.13.md, 2025/11.14.md]
tags: [tesla-autopilot, self-driving, march-of-nines, software-2-0, fleet-learning]
---

# 2025 — Tesla FSD: HW4 Test Drive & Self-Driving Optimism

Three posts building the 2025 Tesla FSD story — the "no notes" HW4 Model X drive, the why-self-driving-matters rationale, and a Supercharger-plus-diner note.

## Jul 24 — "I am unreasonably excited about self-driving"

The macro case, in one paragraph:

> "Self-driving will be the first technology in many decades to visibly **terraform outdoor physical spaces and way of life**. Less parked cars. Less parking lots. Much greater safety for people in and out of cars. Less noise pollution. More space reclaimed for humans. Human brain cycles and attention capital freed up from 'lane following' to other pursuits. Cheaper, faster, programmable delivery of physical items and goods."

Frames self-driving as a platform shift at the scale of the automobile itself — an *era before* and *era after*.

## Nov 13 — The "no notes" HW4 Model X drive

The actual test-drive post — first time in Karpathy's 9 years at/around Tesla where a whole neighborhood drive produced **zero clips** of things to improve.

> "On the highway, I felt like a passenger in some super high tech Maglev train pod — the car is locked in the center of the lane while I'm looking out from Model X's higher vantage point through its panoramic front window, listening to the (incredible) sound system, or chatting with Grok."

City streets checklist (all handled without intervention):
- Incoming cars in tight lanes.
- Around construction and temporarily-stationary in-lane cars.
- Tricky left turns with cross-traffic from both sides.
- Out-of-order 4-way stop negotiation.
- Squeezing into bumper-to-bumper traffic to make a turn.
- Overtook a passenger-loading bus that was blocking a stop sign behind it.
- End of route: circled a parking lot, found a spot, parked.

Then the macro observation:

> "It's new for me to come back with nothing. **Perfect drive, no notes**. I expect there's still more work for the team in the long [[march-of-nines|march of 9s]], but it's just so cool to see we're beyond finding issues on any individual ~1 hour drive — you actually have to **go to the fleet and mine them**."

### The Software 2.0 victory lap

Paired with Ashok Elluswamy's ICCV25 talk, which hints at the under-the-hood stack: sensor streams (videos, maps, kinematics, audio) over **long contexts (~30 seconds)** feed into a big neural net; steering/acceleration comes out; visualization is auxiliary.

> "This is the dream of the complete **[[software-2-0]]** rewrite that scales fully with data streaming from millions of cars in the fleet and the compute capacity of your chip — not some engineer's clever new `DoubleParkedCarHandler` C++ abstraction with undefined test-time characteristics of memory and runtime."

Beyond the car: **world reconstructors, world simulators "dreaming" dynamics, RL** — "all of these components general, foundational, neural net based, how the car is really just one kind of robot… are people getting this yet?"

## Nov 14 — Supercharger + diner as "exhibit for the future"

Short note on a Supercharger-with-diner concept:

> "Love this! Supercharger, diner, … but really a kind of **exhibit for the future**. Plotting a road trip SF → LA to charge Shadowfax."

Small but thematic — infrastructure that is also a hands-on future exhibit, following the same logic as "you have to *feel* self-driving intuitively, not just think about it."

## Why this matters

- Jul 24 + Nov 13 together close the loop on [[march-of-nines]] and [[decade-of-agents]] originally framed in 2024 — self-driving is the most visible, earliest-payoff instance.
- Nov 13's "go to the fleet and mine them" is the concrete 2025 operationalization of [[march-of-nines|march-of-9s]] — each 9 gets harder because the failure signal gets sparser.
- Pair with the 2026 Jan 1 coast-to-coast (2,732 miles, zero interventions) — Nov 2025 is the neighborhood-scale milestone that foreshadows it.
- Directly seeds the 2026 "humanoid robot" generalization via the "world reconstructors + simulators dreaming dynamics" framing.

## Related

- [[tesla-autopilot]], [[tesla-fsd]]
- [[march-of-nines]]
- [[software-2-0]]
- [[decade-of-agents]]
- [[waymo]] (comparison — different stack philosophy)
- [[andrej-karpathy]]
