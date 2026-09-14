# Examples

This directory contains small, self-contained examples showing how KARADAVI concepts can be represented or consumed.

## Current example

### `basic-entity-state.json`

A minimal machine-readable entity state containing:

- an entity identity;
- a supported claim;
- an evidence reference;
- provenance timestamps; and
- contextual authority.

Validate the structure against [`../specs/entity-state.schema.json`](../specs/entity-state.schema.json).

## What examples should demonstrate

Examples should favor clarity over framework complexity. Useful future examples include:

- competing claims from different sources;
- provenance chains;
- contextual authority evaluation;
- explicit ambiguity and uncertainty;
- conflicting evidence; and
- a trust state derived from multiple evidence records.

Examples should remain synthetic or use appropriately public material. Do not place private datasets, credentials, internal service information, or unreleased implementation here.
