# Editorial Model

KARADAVI treats publication as a deliberate editorial transition rather than the automatic output of extraction or generation.

## Core rule

> **AI never publishes.**

Automation is allowed to assist the editorial process. It does not receive publication authority.

## Conceptual flow

```text
Source material
      |
      v
Observation / extraction
      |
      v
Structured draft data
      |
      v
Claims + evidence + provenance
      |
      v
AI-assisted draft
      |
      v
Human editorial review
      |
      +---- revise / reject / request more evidence
      |
      v
Editorial approval
      |
      v
Published entity state
      |
      v
Connected knowledge trails
```

This is a conceptual public model. It does not specify private services, endpoints, databases, prompts, models, or deployment topology.

## Three states that must not be confused

### 1. Knowledge state

What does the available evidence indicate?

Examples include supported, conflicting, ambiguous, unsupported, or disproven.

### 2. Editorial state

Where is the material in the publication workflow?

Examples include extracted, draft, under review, approved, rejected, or published.

### 3. Presentation state

How is approved knowledge represented to a reader or downstream system?

Examples include an entity summary, relationship, timeline item, contextual section, or machine-readable state.

These states can influence each other, but they are not equivalent.

A claim can be well-supported and still unpublished. A published claim can later become disputed. A draft can contain machine-generated prose while its underlying claims retain separately inspectable evidence.

## Human approval as provenance

Editorial approval should eventually be representable as part of a provenance chain.

```text
Source
  ↓
Extraction
  ↓
Normalization
  ↓
Draft
  ↓
Human review
  ↓
Approval
  ↓
Publication
```

The public research question is not how KARADAVI's private workflow is implemented. It is what minimum information a knowledge system should preserve so a downstream consumer can distinguish source material, machine transformation, editorial judgment, and published representation.

## AI boundary

AI assistance may be useful for:

- extracting candidate facts and relationships;
- normalizing structured fields;
- proposing summaries;
- identifying missing context;
- drafting prose from structured material;
- surfacing potential conflicts for review.

AI output should not by itself establish:

- publication approval;
- source authority;
- factual certainty;
- resolution of disputed claims;
- canonical identity when ambiguity remains.

## Relationship to the public specification

The current v0.1 schemas focus on entities, claims, evidence, provenance, authority, and trust signals. The editorial model exposes a future research requirement: provenance may need to represent transformations and approval events without coupling the public specification to KARADAVI's private CMS.

That question remains experimental.
