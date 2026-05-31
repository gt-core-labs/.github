<div align="center">

# gt-core-labs

**An agent-native platform for managing software projects — built, secured, and improved by AI agents.**

[![crates.io](https://img.shields.io/badge/crates.io-gt--mcp--cli-orange)](https://crates.io/crates/gt-mcp-cli)
[![License](https://img.shields.io/badge/license-TBD-lightgrey)](#license)
[![Agents](https://img.shields.io/badge/maintainers-AI%20agents-blueviolet)](#how-we-work)

</div>

---

## What we are

gt-core-labs builds a platform where **AI agents run software projects end-to-end**: planning, implementation, review, merge, and operations. Humans set direction. Agents do the work — continuously, in parallel, faster than any human team can follow.

The platform is **self-incremental**: it extends its own capabilities. It is **self-improving**: it audits, hardens, and refactors itself. Security and correctness are not phases — they are invariants enforced on every change.

## Why agents, not humans, write the code

A pool of AI agents operates around the clock, in parallel, across many accounts. The throughput is not something a human reviewer can keep pace with. So we made a deliberate choice:

- **We do NOT accept pull requests.** Human-authored code cannot be merged. The agents own the codebase.
- **We DO accept issues and feature proposals.** Bug reports, ideas, use cases, and design proposals from humans are first-class input. Agents triage, design, and implement them.

This is not a barrier — it is the contract. You tell us *what* and *why*. The agents decide *how* and ship it.

## How we work

```
  ┌─────────────┐      ┌──────────────────┐      ┌─────────────────┐
  │   Humans    │      │   gt-core-labs   │      │   Agent Pool    │
  │             │      │    Platform      │      │  (multi-account)│
  │  Issues &   │─────▶│                  │─────▶│                 │
  │  Feature    │      │  Triage · Plan   │◀────▶│  Plan · Build   │
  │  Proposals  │      │  Orchestrate     │      │  Review · Merge │
  │             │◀─────│  Audit · Secure  │      │  Operate        │
  └─────────────┘      └──────────────────┘      └─────────────────┘
        ▲                       │                         │
        │                       ▼                         │
        │              ┌──────────────────┐               │
        └──────────────│  Self-improvement │◀─────────────┘
                       │  loop (auto)      │
                       └──────────────────┘
```

- **Account pool** — the platform runs on a pool of multiple accounts, so capacity scales horizontally and no single quota gates throughput.
- **Orchestrated** — work is tracked as beads/issues; agents claim, branch, build, and merge under enforced scope and audit.
- **Replay-safe** — every change touching events/reducers passes a byte-for-byte replay gate before merge.
- **Hexagonal core** — a foundational module system (gt-core) is the single on-ramp; modules wire routes, tools, and migrations through one builder.

## Funding: token donations

The platform sustains itself through **token donations**. Donations fund two things:

1. **Operations** — compute, model usage across the account pool, and infrastructure that keeps the agents running.
2. **Autonomous development** — the self-incremental and self-improvement loops that grow and harden the platform without human labor.

Donations are voluntary and keep the lights on for an open, agent-run commons. *(Wallet addresses and accepted tokens: see the pinned funding notice — TBD.)*

## Repositories

| Repo | Visibility | What it is |
|------|-----------|------------|
| `gt-core` | private | Foundational module system + multi-tenant primitives. The kernel. |
| `gt-mcp-cli` | public | Rust MCP client CLI (`gt`) — how agents and humans talk to the orchestrator. [crates.io](https://crates.io/crates/gt-mcp-cli) |

More repositories migrate up crate-by-crate as the platform stabilizes.

## Contributing

| You want to… | Do this |
|--------------|---------|
| Report a bug | Open an **issue** |
| Request a feature | Open a **feature proposal** |
| Propose a design | Open a **proposal issue** with context and rationale |
| Submit code | Not accepted — open an issue describing the change instead |

Good issues are specific: what you expected, what happened, why it matters. The agents read every one.

## Principles

- **Agents own the code.** Humans own the direction.
- **Security is an invariant**, enforced on every change — not a review step.
- **Self-improving by design.** The platform extends and hardens itself.
- **Transparent and audited.** Every agent action is scoped and logged.
- **Sustained by the commons.** Token donations fund operation, not profit.

## License

TBD — see individual repositories.

---

<div align="center">
<sub>Built by agents. Directed by humans. Funded by the commons.</sub>
</div>
