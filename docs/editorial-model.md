# Editorial Model

KARADAVI is intended to be continuously evolving, but continuous discovery must never mean automatic publication. Publication is a deliberate editorial transition with a human decision and an auditable basis.

## Core invariant

> **AI never publishes.**

AI and automation may research, discover, extract, normalize, classify, reconcile, draft and propose updates. They do not receive publication authority.

## Knowledge lifecycle

```text
Source discovery / research lead
              |
              v
     Retrieval / observation
              |
              v
      Extraction / parsing
              |
              v
    Normalization / identity resolution
              |
              v
   Claims + relations + evidence + provenance
              |
              v
       Reconciliation / evaluation
              |
              v
      Research notes / structured draft
              |
              v
        HUMAN EDITORIAL REVIEW
              |
       ┌──────┼────────┐
       v      v        v
     Revise  Reject  Request more evidence
              |
              v
       Explicit approval
              |
              v
       Published revision
              |
              v
  Monitoring / reconciliation / update proposal
              └──────────────────────────────↺
```

This is a conceptual public lifecycle. It does not specify private services, endpoints, databases, prompts, models or deployment topology.

## Three states that must not be confused

### 1. Knowledge state

What does the available evidence indicate? Examples include supported, conflicting, ambiguous, incomplete, stale, unsupported or contradicted.

### 2. Editorial state

Where is the material in the publication process? Examples include discovered, extracted, draft, under review, changes requested, approved, rejected or published.

### 3. Presentation state

How is approved knowledge represented to a reader or downstream system? Examples include an entity page, relationship view, timeline, contextual explanation or machine-readable representation.

These states can influence each other, but they are not equivalent. A supported claim can remain unpublished. A published claim can later become disputed. A generated draft is not an approved statement.

## Research and autonomous workflows

KARADAVI's intended operating model includes both deliberate research and ongoing discovery:

- **Manual research:** editors initiate focused investigations and choose the depth and scope of research.
- **Source discovery:** systems identify candidate sources, new entities and relevant material.
- **Extraction and normalization:** source material is transformed into structured candidate observations and claims.
- **Reconciliation:** candidate information is compared against existing entities, claims and sources.
- **Discover and update:** ongoing workflows identify missing context, new relationships, changed sources, conflicts and potentially stale knowledge.
- **Editorial preparation:** systems prepare evidence-backed drafts or update proposals for review.

These workflows can be increasingly autonomous in discovery and preparation. The publication gate remains human-controlled.

## Human approval as provenance

Editorial decisions should themselves be traceable. A future interoperable model may record who or what proposed a change, which evidence was considered, what transformations occurred, who reviewed it, the decision, and when the resulting revision was published.

The public research question is what minimum information a knowledge system should preserve so a consumer can distinguish source material, machine transformation, editorial judgment and published representation.

## AI boundary

AI assistance may:

- extract candidate facts and relationships;
- normalize structured fields;
- resolve or rank candidate entity matches while preserving ambiguity;
- summarize and compare sources;
- identify missing context and possible conflicts;
- draft explanations from structured material;
- propose corrections and updates when information changes.

AI output must not by itself establish:

- publication approval;
- source authority;
- factual certainty;
- resolution of disputed claims;
- canonical identity when ambiguity remains.

## Public research scope

The public specifications explore the semantics of claims, relations, evidence, provenance, authority, uncertainty, trust and editorial transitions. They do not expose or prescribe KARADAVI's private CMS, internal prompts, model configuration, operational controls or deployment implementation.
