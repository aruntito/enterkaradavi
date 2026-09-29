# Changelog

All notable public changes to KARADAVI are recorded here.

## [Unreleased]

### Product progress sync — 2026-09-29
- Documented the current 10-domain knowledge taxonomy.
- Documented the canonical entity engine and entity-type normalization work.
- Added the current assisted editorial pipeline: extraction → structured draft data → AI-assisted drafting → human review → publication.
- Made the editorial invariant explicit: **AI never publishes.**
- Documented admin/public surface separation, PWA foundations, origin-story experience, and knowledge-graph direction.
- Updated the roadmap to distinguish private product progress from public specification maturity.

### Added
- Public v0.1 conceptual architecture and research model.
- Public specification document describing resource, reference, temporal, conflict, and evaluation semantics.
- Experimental schemas for entity state, claims, relations, evidence, provenance, authority, and trust signals.
- Reference examples for basic entity state and explicit relations.
- Research notes covering trust representation, contextual authority, uncertainty propagation, entity resolution, and claim lifecycle.
- Automated JSON/schema validation through GitHub Actions.

### Corrected
- Aligned the basic entity-state example with the published claim and evidence schemas.
- Extended validation to cover the relation schema and relation reference example.

### Direction
- Tighten terminology and normative schema requirements.
- Add reproducible experiments around conflicting evidence, uncertainty, entity resolution, and claim history.
- Establish compatibility and versioning rules before calling any schema stable.
