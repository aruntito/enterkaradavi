# KARADAVI Architecture

KARADAVI explores a trust-oriented perception architecture for software systems that need to reason about digital entities, claims, sources, and evidence.

## System model

```text
Digital World
      │
      ▼
┌─────────────┐
│ Perception  │  observe artifacts, events, sources
└──────┬──────┘
       ▼
┌─────────────┐
│Identification│ resolve candidate entities
└──────┬──────┘
       ▼
┌─────────────┐
│  Semantics  │ interpret meaning and relationships
└──────┬──────┘
       ▼
┌─────────────┐
│   Evidence  │ connect claims to observations
└──────┬──────┘
       ▼
┌─────────────┐
│  Authority  │ evaluate contextual source standing
└──────┬──────┘
       ▼
┌─────────────┐
│    Trust    │ derive an inspectable treatment signal
└──────┬──────┘
       ▼
┌─────────────┐
│ Machine State│ expose structured downstream state
└─────────────┘
```

The layers are conceptual boundaries, not necessarily separate services. A future implementation may combine, split, cache, or reorder parts of the pipeline while preserving the semantic model.

## 1. Perception

The system observes an input: a document, page, API response, entity, statement, event, image-derived fact, or other digital artifact.

**Question:** what is present?

A perception record should retain enough source context to make later interpretation traceable.

## 2. Identification

Observed material is mapped to one or more candidate entities, concepts, sources, or event identities.

**Question:** what entity might this be?

Identity should support ambiguity. If two candidates are plausible, the system should be able to represent both rather than silently selecting one.

## 3. Semantics

The system represents attributes, relationships, types, meanings, and context in a form that downstream components can reason about.

**Question:** what does this represent here?

Semantic interpretation should distinguish the underlying observation from an interpretation derived from it.

## 4. Evidence

Claims are connected to supporting observations or sources.

**Question:** what supports this claim?

Evidence should preserve provenance. A derived value without a recoverable basis is weaker than a value whose supporting chain can be inspected.

## 5. Authority

Different sources can have different standing for different claims and contexts.

**Question:** who or what has standing to establish this fact here?

Authority is therefore modeled as contextual. A source can be authoritative for one class of claim without being universally authoritative.

## 6. Trust

Trust is a structured interpretation of available evidence, provenance, authority, consistency, uncertainty, and context.

**Question:** how should a consuming system treat this information?

KARADAVI deliberately avoids treating trust as a universal scalar. A consuming system may need to know *why* a signal exists, not merely its final value.

## 7. Machine-readable state

The output should be consumable by other software without requiring the original human interpretation to be repeated.

A useful state can expose:

- subject or entity identity;
- claim or observation;
- evidence references;
- provenance;
- authority context;
- uncertainty;
- evaluation status; and
- derived treatment signals.

## Evidence flow

The intended reasoning path is:

```text
Observation
    ↓
Evidence Record
    ↓
Claim
    ↓
Contextual Evaluation
    ↓
Trust Signal
    ↓
Machine-readable State
```

The system should be able to move backwards through the chain when investigating a result.

## Conflict handling

Conflicting information should remain representable.

```text
                 ┌─ Claim A ─ Evidence A
Subject ─────────┤
                 └─ Claim B ─ Evidence B
```

KARADAVI does not assume that disagreement should immediately be averaged away. Conflict can itself be meaningful state and may require contextual evaluation.

## Uncertainty model

Unknown, ambiguous, unsupported, conflicting, and disproven are different states.

A core rule is:

> **Do not convert missing evidence into false certainty.**

Uncertainty should travel with derived information where practical so downstream systems can distinguish a well-supported claim from an unresolved one.

## Design principles

1. **Provenance first** — preserve where information came from.
2. **Context matters** — authority and trust depend on the claim and environment.
3. **Uncertainty is data** — unknown should not silently become true or false.
4. **Evidence is inspectable** — derived signals should be traceable to inputs.
5. **Identity is explicit** — expose ambiguity when entity resolution is uncertain.
6. **Conflicts remain visible** — disagreement should not disappear behind a single value.
7. **Machine-readable by design** — outputs should be structured for downstream systems.

## Public scope

This document describes the public conceptual architecture. It intentionally excludes private deployment topology, internal infrastructure, private datasets, credentials, and unreleased implementation details.
