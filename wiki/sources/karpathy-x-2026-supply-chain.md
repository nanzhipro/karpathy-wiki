---
title: "2026-03 — Supply Chain Attacks: litellm and npm axios"
type: source-summary
created: 2026-04-17
updated: 2026-04-17
sources: [2026/3.19.md, 2026/3.31.md]
tags: [security, supply-chain, dependencies, karpathy]
---

# 2026-03 — Supply Chain Attacks

Two posts on concrete supply-chain incidents, tied back to Karpathy's broader thesis that **dependency-heavy software is now a liability**.

## Sources

- **Mar 19** — litellm PyPI supply chain attack (credential exfiltration).
- **Mar 31** — npm axios supply chain attack (remote access trojan).

## The litellm incident (Mar 19)

A poisoned version of `litellm` was live on PyPI for less than ~1 hour. **A plain `pip install litellm` was enough to exfiltrate:**

- SSH keys
- AWS / GCP / Azure credentials
- Kubernetes configs
- Git credentials
- Env vars (all API keys)
- Shell history
- Crypto wallets
- SSL private keys
- CI/CD secrets
- Database passwords

**Blast radius:** 97M downloads/month direct, plus transitive dependents — e.g. `dspy` (which depended on `litellm>=1.64.0`).

Discovery was accidental: Callum McMahon's machine OOM-crashed because the attack had a memory bug. "**If the attacker didn't vibe code this attack it could have been undetected for many days or weeks.**"

## The axios incident (Mar 31)

`axios` — "the most popular HTTP client library with 300M weekly downloads" — also poisoned on npm. Karpathy scanned his own system and found an indirect import from `googleworkspace/cli` while experimenting with gmail/gcal CLIs. Saved by version resolution to a clean `1.13.5`, but he notes:

> "If I did this earlier today the code would have resolved to latest and I'd be pwned."

## The broader argument

Both posts feed Karpathy's [[bacterial-code]] thesis:

> "Classical software engineering would have you believe that dependencies are good (we're building pyramids from bricks), but imo this has to be re-evaluated, and it's why I've been so growingly averse to them, preferring to use LLMs to 'yoink' functionality when it's simple enough and possible."

**Proposed mitigations:**

- Personal: release-age constraints, containers, pinned dependencies.
- Systemic: **package-manager defaults must change** so that a single infection doesn't propagate via unpinned dependencies.

## The meta-shift

> "Every time you install any depedency you could be pulling in a poisoned package anywhere deep inside its entire depedency tree."

In the [[agentic-engineering]] era, agents can **rewrite or inline** what would previously have been a dependency. That makes the dependency calculus different: the *cost* of writing code you used to import just dropped.

## Related

- [[bacterial-code]]
- [[supply-chain-attacks]]
- [[build-for-agents]]
- [[llm-knowledge-bases]] — offline, file-based knowledge has a related "reduce attack surface" character
