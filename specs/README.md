# Specifications

This directory contains public specifications and schemas for KARADAVI concepts.

## Initial specification

### `entity-state.schema.json`

The first experimental schema models a machine-readable state around an entity or digital artifact.

It provides a common envelope for:

- identity;
- claims;
- evidence references;
- provenance;
- contextual authority; and
- uncertainty / state.

The schema is intentionally small. It is a research artifact, not a finalized interoperability standard.

## Example

See [`../examples/basic-entity-state.json`](../examples/basic-entity-state.json) for a minimal instance.

## Specification principles

1. **Separate observation from interpretation.**
2. **Keep provenance attached to derived information.**
3. **Allow uncertainty and conflict to be represented explicitly.**
4. **Do not require a universal trust score.**
5. **Version normative changes deliberately.**
6. **Keep experimental proposals clearly labeled.**

## Future direction

Potential future specifications include:

- claim and evidence records;
- source and authority context;
- provenance chains;
- identity resolution records;
- uncertainty propagation;
- trust evaluations; and
- machine-to-machine state exchange.

No specification in this directory should expose private deployment details or depend on unpublished internal implementation.
