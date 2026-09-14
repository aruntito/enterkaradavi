# Architecture Decisions

KARADAVI records important public design decisions here so that future changes have context.

## ADR-001 — Trust is structured, not a universal score

**Decision:** Trust signals should retain their relationship to claims, evidence, provenance, authority context, and uncertainty.

**Reason:** A single unexplained number hides why a system reached a conclusion and makes disagreement difficult to inspect.

## ADR-002 — Authority is contextual

**Decision:** Authority is modeled in relation to a claim and context rather than treated as a universal property of a source.

**Reason:** A source can be highly authoritative for one class of claims and irrelevant for another.

## ADR-003 — Uncertainty is first-class data

**Decision:** The public model must be able to represent unknown, ambiguous, conflicting, and unsupported states.

**Reason:** Forcing incomplete evidence into binary truth values creates false certainty.

## ADR-004 — Public research is separated from private implementation

**Decision:** `enterkaradavi` documents concepts, specifications, examples, and reproducible public research; private KARADAVI remains the implementation and operational surface.

**Reason:** The research should be understandable without exposing proprietary or operational knowledge.

## ADR-005 — Experimental status is explicit

**Decision:** Public schemas and terminology remain experimental until evidence justifies promotion.

**Reason:** Version numbers and repository activity are not substitutes for validation.
