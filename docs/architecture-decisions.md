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


## ADR-006 — AI assistance does not imply publication authority

**Decision:** Automated systems may extract, normalize, compare, structure, and draft knowledge, but publication requires an explicit human editorial decision.

**Reason:** Generative output and extracted data can be useful intermediate artifacts without being treated as accepted public knowledge. Keeping the boundary explicit makes provenance clearer and reduces the risk of silently promoting machine output into editorial fact.

## ADR-007 — Editorial state and epistemic state are separate

**Decision:** Whether content is draft, reviewed, approved, or published must remain conceptually separate from whether an underlying claim is supported, disputed, uncertain, or disproven.

**Reason:** Publication is a workflow decision. Evidence status is an epistemic property. Collapsing them would make a published statement appear automatically true or an unpublished statement automatically false.

## ADR-008 — Knowledge domains organize discovery, not ontology

**Decision:** The ten public knowledge domains are navigation and editorial organization surfaces, not hard ontological boundaries.

**Reason:** Real entities cross categories. A person can connect to a company, technology, place, historical event, and concept. The graph should preserve those cross-domain relationships rather than forcing knowledge into isolated silos.
