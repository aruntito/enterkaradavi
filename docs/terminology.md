# KARADAVI Terminology

KARADAVI uses a small vocabulary so that trust discussions remain precise.

| Term | Working definition |
| --- | --- |
| **Observation** | Something a system directly receives, detects, extracts, or records. |
| **Entity** | A thing the system attempts to represent as a distinct subject. |
| **Claim** | A proposition asserted about an entity, event, relationship, or state. |
| **Evidence** | An observation or source-derived artifact that supports, weakens, or contextualizes a claim. |
| **Provenance** | Information describing where an observation, claim, or derived state came from and how it was transformed. |
| **Authority** | Context-dependent standing a source, actor, or record has for establishing or influencing a claim. |
| **Uncertainty** | Explicit representation of what is unknown, ambiguous, incomplete, stale, or disputed. |
| **Evaluation** | A structured interpretation of a claim using available evidence, provenance, authority, consistency, and context. |
| **Trust signal** | A machine-readable result of an evaluation, including the information needed to understand its basis and limitations. |
| **Machine-readable state** | Structured state intended for consumption by another software system. |

## Important distinctions

### Evidence is not authority

A source can provide evidence without having authority to establish a fact. Conversely, an authoritative source can still be incomplete, stale, or misapplied.

### Trust is not truth

A trust signal describes how a consuming system should treat available information. It does not magically establish that a claim is true.

### Confidence is not certainty

Confidence expresses an evaluation under stated assumptions. Uncertainty should remain visible rather than being converted into false precision.

### Identity is not identification

An entity may exist independently of a system's ability to identify it correctly. Identification is an inference and can remain unresolved.

## Vocabulary rule

When a design uses these terms, it should preserve their distinctions. If a new term is introduced, document why the existing vocabulary is insufficient.
