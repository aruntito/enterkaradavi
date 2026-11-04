# Public Knowledge Model

KARADAVI is entity-centered and knowledge-graph-first. A reader-facing page is one representation of a deeper model whose identity, claims, evidence, provenance, relationships and revisions should remain connected.

The model is designed to be extensible. The ten knowledge trails are discovery surfaces; they are not a complete or permanent ontology.

## Core knowledge structure

Conceptually:

```text
                         CANONICAL ENTITY
                         /      |       \
                        /       |        \
                   CLAIMS   RELATIONS   REPRESENTATIONS
                     |          |             |
              ┌──────┼──────┐   |         Explanations
              |      |      |   |         Reader pages
           EVIDENCE SOURCES  CONTEXT       Structured data
              |      |      |
              └── PROVENANCE ──┘
                     |
          AUTHORITY / UNCERTAINTY
                     |
                EVALUATION
                     |
             EDITORIAL DECISION
                     |
             PUBLISHED REVISION
```

This is a conceptual model, not a claim that every component is already implemented as a separate service or database object.

## Entity and canonical identity

An **entity** is a distinct subject KARADAVI attempts to represent: a person, organization, technology, scientific subject, place, event, concept, species, institution, cultural subject or another identifiable thing.

Canonical identity is the stable reference point that allows source records, claims and relationships to converge on the same subject without erasing ambiguity.

Entity resolution is an inference, not an infallible fact. When sources are ambiguous or candidate matches remain uncertain, the model should preserve that uncertainty instead of silently merging distinct subjects.

## Claim

A **claim** is a proposition about an entity, event, state or relationship.

Claims must remain distinct from the entity they describe. A subject can persist while claims about it are added, qualified, contradicted, corrected or retracted.

## Source and observation

A **source** is an origin from which material is obtained: for example, a publication, dataset, registry, research paper, archive, API or other reference.

An **observation** records what was received, observed or extracted from a source at a particular time. Source identity and the system's observation of that source should not be conflated.

## Evidence

**Evidence** is material that supports, weakens, contradicts or contextualizes a claim. A claim may have multiple evidence items; one evidence item may be relevant to multiple claims.

Evidence should remain inspectable and connected to its source and observation context.

## Provenance

**Provenance** records where information came from and how it changed before reaching its current representation.

A provenance chain may distinguish source, retrieval, observation, extraction, normalization, entity resolution, interpretation, editorial action and publication. Transformations should not erase the origin of the material.

## Relationship

A **relationship** connects two or more entities through a meaningful, typed connection. Examples include founded-by, located-in, developed-by, part-of, influenced-by, discovered-by, preceded-by and related-to.

Relationships are not merely hyperlinks. They are graph edges with semantics, context and, where appropriate, supporting claims and evidence.

## Authority

**Authority** is contextual standing to establish or inform a particular kind of claim. A source may be authoritative for one domain, jurisdiction, period or claim type without being universally authoritative.

Authority and evidence are related but not interchangeable.

## Uncertainty and conflict

Information may be unknown, ambiguous, incomplete, stale, conflicting, unsupported or contradicted. These are meaningful knowledge states, not merely validation errors.

Conflicting claims should remain representable until evidence and context justify an editorial or evaluative decision. Uncertainty should not disappear during normalization, aggregation or drafting.

## Evaluation

An **evaluation** interprets a claim using evidence, provenance, authority, time, consistency and context. It should preserve its basis and limitations. A trust signal is an inspectable evaluation artefact, not a universal truth label.

## Revision and history

Knowledge changes. A **revision** records a change to a represented state while preserving enough history to understand what changed and why. Corrections should not silently erase prior published states or their provenance.

The public research question is how to represent revisions, claim lifecycles and editorial decisions in interoperable ways without coupling the model to one private CMS.

## Editorial state is separate

Knowledge state, editorial state and presentation state are distinct:

- a claim may be well-supported but not yet approved for publication;
- a published claim may later become disputed or stale;
- an AI-generated draft is not an editorial approval;
- a reader-facing page is a presentation of approved knowledge, not the underlying evidence itself.

> **AI never publishes.** Human editorial approval is a separate and mandatory transition.

## Why these distinctions matter

A source is not the same thing as a claim. A claim is not the same thing as truth. Evidence is not the same thing as authority. A relationship is not the same thing as a hyperlink. Publication is not the same thing as certainty.

The public KARADAVI model exists to keep these distinctions visible as knowledge is discovered, connected, reviewed, published and revised.
