<div align="center">

# KARADAVI

### Machine trust · perception · semantic authority

**Infrastructure for helping machines understand what they are seeing, where it came from, and how it should be treated.**

<p>
  <a href="https://www.karadavi.com"><img src="https://img.shields.io/badge/Live%20Site-karadavi.com-111827?style=for-the-badge" alt="Live site" /></a>
  <img src="https://img.shields.io/badge/status-active%20research-111827?style=for-the-badge" alt="Active research" />
  <img src="https://img.shields.io/badge/spec-v0.1-111827?style=for-the-badge" alt="Specification v0.1" />
  <img src="https://img.shields.io/badge/license-MIT-111827?style=for-the-badge" alt="MIT License" />
</p>

<p>
  <a href="https://www.karadavi.com">Website</a> ·
  <a href="#the-idea">The idea</a> ·
  <a href="#architecture">Architecture</a> ·
  <a href="#public-model">Public model</a> ·
  <a href="#research">Research</a> ·
  <a href="#repository-map">Repository</a>
</p>

</div>

---

## The idea

Modern systems can retrieve enormous amounts of information. The harder problem is deciding **what that information means, what supports it, who has authority over it, and how uncertainty should be represented**.

KARADAVI is an experimental research platform for that layer.

It explores how software can move from raw digital observations toward structured, inspectable, machine-readable trust context.

> **Machines should not only retrieve information. They should understand what they are seeing, where it came from, and why it should be trusted.**

### The core questions

| Question | KARADAVI concern |
| --- | --- |
| **What is this?** | Perception + entity identification |
| **What does it mean?** | Semantics + context |
| **What supports it?** | Evidence + provenance |
| **Who has standing here?** | Contextual authority |
| **How certain is it?** | Uncertainty + confidence |
| **How should software consume it?** | Machine-readable state |

---

## Architecture

```text
┌──────────────────┐
│   Digital World  │
└────────┬─────────┘
         ↓
┌──────────────────┐
│    Perception    │  What is present?
└────────┬─────────┘
         ↓
┌──────────────────┐
│  Identification  │  What entity is this?
└────────┬─────────┘
         ↓
┌──────────────────┐
│     Semantics    │  What does it mean?
└────────┬─────────┘
         ↓
┌──────────────────┐
│     Evidence     │  What supports the claim?
└────────┬─────────┘
         ↓
┌──────────────────┐
│     Authority    │  Which source has standing?
└────────┬─────────┘
         ↓
┌──────────────────┐
│      Trust       │  How should it be treated?
└────────┬─────────┘
         ↓
┌──────────────────┐
│ Machine-readable │
│      State       │
└──────────────────┘
```

Trust is deliberately **not** treated as a magic number. A useful signal remains connected to the evidence, provenance, authority context, and uncertainty that produced it.

**Explore KARADAVI:** [www.karadavi.com](https://www.karadavi.com)

[Read the full architecture →](docs/architecture.md)

---

## Public model

The first public specification layer models the objects a trust-aware system needs to keep separate:

```text
ENTITY
  │
  ├── CLAIM ────────────────┐
  │      │                  │
  │      └── EVIDENCE ── PROVENANCE
  │                         │
  └── AUTHORITY CONTEXT ────┘
              │
              ↓
       TRUST SIGNAL
              │
              ↓
    MACHINE-READABLE STATE
```

### v0.1 specification surface

| Specification | Purpose |
| --- | --- |
| `entity-state.schema.json` | Top-level entity state |
| `claim.schema.json` | Atomic propositions |
| `evidence.schema.json` | Supporting or weakening artifacts |
| `provenance.schema.json` | Origin and transformation context |
| `authority.schema.json` | Contextual source standing |
| `trust-signal.schema.json` | Structured evaluation result |

[Explore the specifications →](specs/)

> **Design rule:** evidence, authority, identity, and uncertainty remain inspectable instead of being collapsed into one opaque score.

---

## Research

KARADAVI treats machine trust as a research problem rather than a single algorithm.

Current public questions include:

- Can authority be modeled as contextual standing rather than a global source ranking?
- How should uncertainty propagate through derived claims?
- How should conflicting claims remain visible to downstream systems?
- How should ambiguous entity resolution affect later evaluations?

Research notes use explicit questions, hypotheses, methods, observations, limitations, and next experiments.

[Read the research notebook →](research/)

---

## What KARADAVI is not

KARADAVI is **not** intended to be:

- another chatbot;
- a generic search engine;
- a universal truth score;
- a replacement for domain expertise; or
- a system that hides uncertainty behind confident language.

The project is interested in the **infrastructure underneath intelligent systems**.

---

## Research areas

- Entity perception and resolution
- Semantic representation
- Evidence modeling
- Provenance
- Source authority
- Contextual trust
- Confidence and uncertainty
- Machine-readable knowledge
- Claim and relationship modeling
- AI perception infrastructure

---

## Repository map

```text
enterkaradavi/
│
├── docs/
│   ├── architecture.md
│   ├── terminology.md
│   ├── design-principles.md
│   ├── research-model.md
│   ├── threat-model.md
│   └── public-private-boundary.md
│
├── specs/
│   ├── entity-state.schema.json
│   ├── claim.schema.json
│   ├── evidence.schema.json
│   ├── provenance.schema.json
│   ├── authority.schema.json
│   └── trust-signal.schema.json
│
├── research/
│   ├── 001-trust-is-not-a-score.md
│   ├── 002-contextual-authority.md
│   ├── 003-uncertainty-propagation.md
│   └── 004-entity-resolution.md
│
├── examples/
│   ├── basic-entity-state.json
│   ├── conflicting-claims.json
│   ├── provenance-chain.json
│   └── trust-evaluation.json
│
└── llms.txt
```

---

## Public / private boundary

This repository is the **public research and architecture surface** for KARADAVI.

The private `karadavi` repository remains the implementation and operational surface. Private deployment topology, private datasets, credentials, internal endpoints, unreleased product work, and proprietary implementation are intentionally excluded.

The public repository should stand on its own: someone should be able to understand the ideas without access to the private system.

[Read the boundary policy →](docs/public-private-boundary.md)

> [!IMPORTANT]
> Public documentation must never become a side channel for private implementation or operational information.

---

## Live system

The public research repository and the live KARADAVI surface have intentionally different roles:

**Research →** specifications, experiments, schemas, architecture, and reproducible thinking.

**Live →** the product-facing KARADAVI experience.

### Visit KARADAVI

**[www.karadavi.com](https://www.karadavi.com)**

The website is the front door. This repository is the public record of the ideas and technical model behind it.

---

## Status

**Active research / early specification · v0.1**

The schemas and terminology are experimental and expected to evolve. A specification is not considered stable merely because it is machine-readable.

## Contributing

KARADAVI welcomes contributions that improve the **clarity, rigor, reproducibility, or usefulness** of the public research.

See [CONTRIBUTING.md](CONTRIBUTING.md).

## Security

Do not publish credentials, private datasets, internal endpoints, private deployment configuration, or unreleased implementation details.

See [SECURITY.md](SECURITY.md).

## License

MIT — see [LICENSE](LICENSE).

<div align="center">

**KARADAVI**

_machine trust, made explicit._

[www.karadavi.com](https://www.karadavi.com)

</div>
