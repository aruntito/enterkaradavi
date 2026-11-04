# KARADAVI Architecture

KARADAVI's product direction is an open, continuously evolving knowledge platform built around canonical entities and an interconnected knowledge graph. Its public architecture research describes the semantic responsibilities required to move from distributed source material to inspectable, human-approved knowledge.

This document describes conceptual boundaries, not private services or deployment topology.

## Two complementary views

KARADAVI has two connected architectural concerns:

1. **Knowledge institution:** the public-facing experience through which readers explore entities, explanations and trails.
2. **Knowledge stewardship:** the research, ingestion, identity, evidence, reconciliation and editorial processes that maintain the knowledge behind that experience.

The reader-facing page is a representation of the underlying connected state, not the source of truth for every claim.

## Knowledge lifecycle

```text
Distributed sources and research material
                 |
                 v
        Discovery / retrieval
                 |
                 v
         Observation / extraction
                 |
                 v
       Normalization / identification
                 |
                 v
     Canonical entities and relationships
                 |
                 v
       Claims + evidence + provenance
                 |
                 v
       Reconciliation / evaluation
                 |
                 v
          Editorial preparation
                 |
                 v
          HUMAN APPROVAL GATE
                 |
                 v
       Published knowledge state
                 |
                 v
       Reader experience / graph
                 |
                 v
      Monitoring and update proposals
                 └──────────────────↺
```

The lifecycle is a conceptual model. Implementations may combine, split, cache or reorder technical components while preserving the semantic distinctions and human publication gate.

## 1. Source discovery and perception

The system identifies candidate material from publications, datasets, registries, research repositories, archives, APIs and other sources.

**Question:** what material may be relevant, and where did it originate?

Discovery is not acceptance. A retrieved source is a candidate input whose identity, context, suitability and limitations must remain inspectable.

## 2. Observation and extraction

The system records what it received and extracts candidate information from it.

**Question:** what did the source actually provide?

Observation should retain source and retrieval context. Extraction is a transformation and must not be confused with the original source material.

## 3. Identification and canonical entities

Candidate records are matched to canonical entities and possible new entities.

**Question:** what subject does this material refer to?

Identity resolution should support aliases, duplicate candidates, ambiguity and unresolved matches. A system should not silently merge distinct subjects merely to produce a clean graph.

## 4. Semantics and relationships

The system represents entity types, claims, attributes, typed relationships and context.

**Question:** what does this information mean, and how is it connected?

The ten knowledge trails are discovery surfaces, not a closed ontology. The semantic model must remain extensible as new subjects and relationships are encountered.

## 5. Evidence and provenance

Claims are connected to supporting, weakening, contradicting or contextualizing evidence. Provenance records origin and transformations.

**Question:** what supports this claim, and how did it reach this representation?

A derived value without a recoverable basis is weaker than one whose evidence and transformation history can be inspected.

## 6. Reconciliation, authority and uncertainty

Information from multiple sources is compared. Conflicts, stale data, missing evidence and ambiguous identity remain explicit. Source authority is considered in relation to the claim and context.

**Question:** what agrees, what conflicts, what remains unknown, and which sources have standing for this question?

KARADAVI does not assume disagreement should be averaged away or that one source is universally authoritative.

## 7. Evaluation and editorial preparation

Evidence and context can inform an evaluation and a draft or proposed update.

**Question:** what can responsibly be presented to an editor?

Evaluation is not publication approval. A machine-readable trust signal should expose its basis and limitations rather than hide reasoning inside a universal score.

## 8. Human editorial approval and publication

A human editor reviews the prepared material and explicitly approves, rejects or requests further work.

**Question:** should this become published KARADAVI knowledge?

> **AI never publishes.**

This is a non-negotiable architectural invariant, including for autonomous discovery and update workflows.

## 9. Continuous reconciliation

Sources and the world change. The system can identify new material, possible corrections, missing relationships and stale claims, then prepare update proposals for editorial review.

**Question:** what may have changed since the last approved revision?

Continuous discovery does not authorize silent changes to published knowledge.

## Ten knowledge trails

The initial public discovery model uses People, Companies, Technology, Science, Space, Concepts, History, Places, Nature & Earth, and Society & Culture. These are navigation and discovery groupings over an extensible entity model, not ten separate knowledge silos.

## Public/private boundary

This document describes public concepts and research questions. It intentionally excludes private application code, internal services, database and deployment details, credentials, private datasets, operational tooling and unreleased implementation decisions. The public model should remain useful even when the private implementation changes.
