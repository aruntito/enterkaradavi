# Specifications

Public machine-readable specifications for KARADAVI.

## v0.1 surface

| Schema | Represents |
| --- | --- |
| [`entity-state.schema.json`](entity-state.schema.json) | Top-level machine-readable state |
| [`claim.schema.json`](claim.schema.json) | A proposition about a subject |
| [`evidence.schema.json`](evidence.schema.json) | Supporting, weakening, or contextual evidence |
| [`provenance.schema.json`](provenance.schema.json) | Origin and transformation history |
| [`authority.schema.json`](authority.schema.json) | Contextual standing of a source or actor |
| [`trust-signal.schema.json`](trust-signal.schema.json) | Structured evaluation of a claim |

## Model

```text
Entity
  └── Claim
       ├── Evidence
       │    └── Provenance
       ├── Authority context
       └── Uncertainty
              ↓
        Trust signal
              ↓
     Machine-readable state
```

The schemas deliberately keep these concepts separate. A consuming system can therefore inspect the basis of an evaluation instead of receiving only an opaque score.

## Status

These schemas are **experimental v0.1**. They are research artifacts, not finalized interoperability standards.

Changes that alter field meaning, required fields, or interpretation should be treated as specification changes and documented deliberately.

## Principles

1. Separate observation from interpretation.
2. Keep provenance attached to derived information.
3. Preserve conflict and uncertainty explicitly.
4. Do not require a universal trust score.
5. Prefer composable records over opaque envelopes.
6. Keep experimental proposals clearly labeled.

## Examples

See [`../examples/`](../examples/) for small synthetic instances.

No specification in this directory should expose private deployment details or depend on unpublished internal implementation.
