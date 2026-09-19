# KARADAVI Public Specification

**Current surface:** v0.1 experimental

This document explains how the public schemas fit together. It describes meaning and interchange, not storage, deployment, or private services.

## Resource model

```text
Entity / Source / Event / Artifact
            |
            +-- Claims
            +-- Relations
            +-- Evidence
            +-- Provenance
                     |
                     v
              Evaluation context
                     |
                     v
                Trust signal
```

The important rule is that these are separate concerns.

- Claim says what is being asserted.
- Relation says how two referenced resources are connected.
- Evidence records what supports, weakens, or contextualizes a claim.
- Provenance records origin and transformations.
- Authority describes contextual standing.
- Trust signal records an evaluation and its uncertainty.
- Entity state provides a machine-readable envelope for a subject and its associated state.

## Reference rules

References use stable string identifiers such as:

- entity:example-acme
- claim:example-acme:name
- evidence:example-registry-001
- relation:acme-founded-by-tito

The identifier namespace is experimental. A future stable version must define collision, normalization, ownership, and versioning rules.

## Claim lifecycle

A claim may move through states such as:

```text
unknown -> asserted -> disputed -> retracted
                    \-> asserted
```

These labels describe the state of the representation, not an assertion that the underlying proposition is true or false.

## Conflict semantics

Conflicting claims should coexist when they describe the same subject and predicate but disagree about the object or interpretation.

The public model does not silently resolve the conflict. An evaluator may consider evidence, provenance, authority, time, identity, and context before producing a trust signal.

## Temporal semantics

Timestamps should be interpreted according to their field names.

- observed_at describes when an observation was made.
- published_at describes when a source says material was published.
- retrieved_at describes when the system obtained the material.
- evaluated_at describes when an evaluation was produced.
- valid_from / valid_until describe an authority validity window.

These times are not interchangeable.

## Evaluation rule

A trust signal is an evaluation artifact, not a universal truth label.

A consumer should be able to inspect its claim reference, disposition, basis, evidence references, authority references, uncertainty, evaluation time, and method.

A consumer may derive a compact score for its own application, but that score is downstream of the structured state.

## Versioning

The v0.1 schemas are experimental and changes may be breaking.

Until a stable versioning policy exists:

1. treat schema changes as potentially breaking;
2. update affected examples in the same change;
3. update documentation when semantics change;
4. record material changes in CHANGELOG.md;
5. keep experimental additions clearly labeled.

## Non-goals

The public specification does not define:

- a universal trust score;
- a mandatory database model;
- a deployment architecture;
- a private editorial workflow;
- a universal source ranking;
- an implementation language or framework.

The public contract should remain useful even when the private implementation changes.
