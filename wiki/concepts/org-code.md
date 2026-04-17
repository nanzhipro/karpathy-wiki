---
title: Org Code
type: concept
created: 2026-04-17
updated: 2026-04-17
sources: [2026/2.4.md, 2026/3.6.md]
tags: [organizations, agents, karpathy]
---

# Org Code

Karpathy's informal term for the **programming-of-organizations** that becomes natural once LLM agents are cheap: defining roles, protocols, review steps, and escalation paths as code that orchestrates populations of agents. Sibling to [[claws]] but framed around imitating an *organization*, not composing a *tool chain*.

## The shape

1. **Roles.** Explicit agent personae — reviewer, planner, implementer, critic.
2. **Protocols.** Message formats, handoff rules, escalation triggers.
3. **Supervision.** An overseer agent (or [[claws|claw]]) that approves, merges, retries.
4. **Artifacts.** Every action logged as inspectable text.

## Karpathy's pointers

- The **Feb 4 "moltbook" 150K-agent** thought experiment implicitly sketches org-code: such a population only behaves usefully if *org-coded*.
- The **Mar 6 claws** framing is adjacent: claws are the programming model *for* org-code.

## Why it matters

> "The future of agent systems is less 'one AGI' and more 'many specialized agents wired together by code.'"

Org-code is how a normal engineer wires that. It makes **who decides what, and who checks whom** explicit, inspectable, version-controllable — a prerequisite for trusting agent populations with anything serious.

## Related

- [[claws]]
- [[agentic-engineering]]
- [[people-spirits]]
- [[autoresearch]]
