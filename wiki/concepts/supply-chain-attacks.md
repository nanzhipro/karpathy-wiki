---
title: Supply Chain Attacks (in the Agent Era)
type: concept
created: 2026-04-17
updated: 2026-04-17
sources: [2026/3.19.md, 2026/3.31.md, 2026/2.12.md]
tags: [security, dependencies, agents]
---

# Supply Chain Attacks (in the Agent Era)

A recurring Karpathy theme in early 2026: agent-driven software has **magnified** the supply-chain risk of conventional dependency management, and agents are *also* the solution (via [[bacterial-code|bacterial code]]).

## The incidents Karpathy documents

| Date | Package | Ecosystem | Impact |
|------|---------|-----------|--------|
| Mar 19 2026 | `litellm` | PyPI | Exfiltrated all credentials, wallets, keys. 97M downloads/month + transitive (dspy). Live <1 h. |
| Mar 31 2026 | `axios` | npm | RAT payload. 300M weekly downloads. Karpathy nearly pwned via `googleworkspace/cli` transitive. |

## Why the agent era makes this worse

1. **Agents install eagerly.** An agent asked to "set up vLLM" or "install Claude's MCP plugins" will happily run `pip install X` with wide dependency resolution.
2. **Transitive surface is enormous.** Popular libraries have hundreds of descendants.
3. **Detection is often accidental.** The litellm attack was discovered because the poisoned version had a *bug* that crashed RAM.

## Karpathy's mitigation stack

**Personal hygiene:**
- Release-age constraints on installs.
- Containers / VMs for risky workloads.
- Pinned dependencies.
- Avoid latest-version resolution by default.

**Systemic:**
- Package-manager **defaults must change.** A single infection should not propagate via unpinned deps at scale.

**Cultural / architectural:**
- [[bacterial-code|Bacterial code]] — write small, self-contained, dependency-free modules.
- Use the **yoink workflow**: point an agent at the relevant library's source and have it implement the specific feature you need, inline. See the Feb 12 fp8 / torchao example.

## The meta-claim

> "Classical software engineering would have you believe that dependencies are good (we're building pyramids from bricks), but imo this has to be re-evaluated."

— Karpathy, Mar 19 2026

In the agent era, the **cost** of "just write it yourself" has collapsed (agents can port the relevant logic quickly), while the **cost** of "install and import" has risen (attack surface, maintenance burden, dependency rot). The break-even point has moved.

## Tension with Claws

[[claws|Claws]] like OpenClaw ship with plugin registries. Karpathy is skeptical:

> "Already seeing reports of exposed instances, RCE vulnerabilities, supply chain poisoning, malicious or compromised skills in the registry, it feels like a complete wild west and a security nightmare."

So Claws face the same problem at a higher abstraction: a skill is just a dependency that executes.

## Related

- [[bacterial-code]]
- [[claws]]
- [[byoai]]
- [[build-for-agents]]
- [[agentic-engineering]]
