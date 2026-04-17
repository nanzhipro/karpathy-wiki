---
title: Intelligence Brownouts
type: concept
created: 2026-04-17
updated: 2026-04-17
sources: [2026/3.20.md]
tags: [infrastructure, llms, karpathy-coinage]
---

# Intelligence Brownouts

Karpathy's **Mar 20 2026** coinage for the agent-era equivalent of a power-grid brownout: provider capacity gets saturated and **models silently degrade** — shorter context, stricter rate limits, quality drops, or lower-capability fallbacks routed transparently to users.

## The analogy

- **Electrical brownout:** supply can't meet demand; voltage sags rather than blacking out.
- **Intelligence brownout:** inference demand exceeds provisioned capacity; providers quietly down-route queries to cheaper models, truncate context, or apply quota throttles users don't see.

## Why it matters in the agent era

[[agentic-engineering|Agents]] consume tokens ~1000× faster than humans. Multi-agent orchestration ([[claws]], [[autoresearch]] swarms) multiplies this further. Provider capacity becomes a **global shared resource** with predictable spikes and unpredictable outages.

## Karpathy's implied recommendations

- **Run local when you can.** See [[byoai]] — an open-weights model on local hardware isn't subject to someone else's capacity plan.
- **Pin model versions.** If the provider swaps in a "lighter" model silently, your reproducibility is gone.
- **Treat capacity as a first-class constraint.** Agent systems should degrade *explicitly* (refuse, wait, checkpoint) rather than silently.

## Related

- [[byoai]]
- [[claws]]
- [[agentic-engineering]]
- [[autoresearch]]
