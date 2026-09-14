<div align="center">

# KARADAVI

### Machine trust · perception · semantic authority

**Infrastructure for helping machines understand what they are seeing, where it came from, and how it should be treated.**

<p>
  <img src="https://img.shields.io/badge/status-active%20research-111827?style=flat-square" alt="Active research" />
  <img src="https://img.shields.io/badge/license-MIT-111827?style=flat-square" alt="MIT License" />
  <img src="https://img.shields.io/badge/surface-public%20research-111827?style=flat-square" alt="Public research" />
</p>

<p>
  <a href="#the-idea">The idea</a> ·
  <a href="#architecture">Architecture</a> ·
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

KARADAVI's public conceptual pipeline is:

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

The important distinction is that **trust is not treated as a magic number**. A useful trust signal should remain connected to the evidence, provenance, authority context, and uncertainty that produced it.

[Read the full architecture →](docs/architecture.md)

---

## Research model

KARADAVI currently investigates a structured chain:

```text
Observation
    ↓
Evidence
    ↓
Claim
    ↓
Evaluation
    ↓
Trust Signal
```

Rather than collapsing everything into:

```text
Observation → Score
```

This keeps the reasoning inspectable and leaves room for disagreement, re-evaluation, and new evidence.

### Design principles

- **Provenance first** — preserve where information came from.
- **Context matters** — authority is contextual, not automatically universal.
- **Uncertainty is data** — unknown should not silently become true or false.
- **Evidence is inspectable** — derived signals should be traceable to inputs.
- **Identity is explicit** — ambiguous entity resolution should stay ambiguous.
- **Machine-readable by design** — outputs should be usable by downstream systems.

[Read the research model →](docs/research-model.md)

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
│   ├── research-model.md
│   └── public-private-boundary.md
│
├── specs/
│   ├── README.md
│   └── entity-state.schema.json
│
├── research/
│   ├── README.md
│   └── 001-trust-is-not-a-score.md
│
├── examples/
│   ├── README.md
│   └── basic-entity-state.json
│
└── llms.txt
```

The repository is intentionally documentation- and specification-first. Implementation can evolve independently while the public model remains understandable and reviewable.

---

## Public / private boundary

This repository is the **public research and architecture surface** for KARADAVI.

The private `karadavi` repository remains the implementation and operational surface. Private deployment topology, private datasets, credentials, internal endpoints, unreleased product work, and proprietary implementation are intentionally excluded.

The public repository should stand on its own: someone should be able to understand the ideas without access to the private system.

[Read the boundary policy →](docs/public-private-boundary.md)

> [!IMPORTANT]
> Public documentation must never become a side channel for private implementation or operational information.

---

## Status

**Active research / early specification.**

The concepts, schemas, terminology, and architecture are expected to evolve as experiments are conducted. Experimental material is labeled as such rather than presented as settled standards.

---

## Contributing

KARADAVI welcomes contributions that improve the **clarity, rigor, reproducibility, or usefulness** of the public research.

Good contributions include architecture proposals, specification improvements, research notes, schema design, reference examples, and documentation corrections.

See [CONTRIBUTING.md](CONTRIBUTING.md).

## Security

Do not publish credentials, private datasets, internal endpoints, private deployment configuration, or unreleased implementation details.

See [SECURITY.md](SECURITY.md).

## License

MIT — see [LICENSE](LICENSE).

<div align="center">

**KARADAVI**

_machine trust, made explicit._

</div>
