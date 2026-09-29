# Public Knowledge Model

KARADAVI separates several concepts that are often collapsed into a single article or database record.

This separation helps knowledge remain inspectable.

## Entity

An **entity** is the subject being represented.

Examples include a person, company, technology, scientific subject, place, historical event, concept, species, institution, or cultural subject.

## Claim

A **claim** is a proposition about an entity or relationship.

The entity and the claim are separate because representations change as new information appears.

## Evidence

**Evidence** is material that supports, weakens, contradicts, or contextualizes a claim.

One piece of evidence may matter to several claims. One claim may depend on several pieces of evidence.

## Provenance

**Provenance** describes where information came from and, where relevant, how it changed before reaching its current representation.

A useful provenance trail might distinguish a source, an observation, an extraction, an interpretation, an editorial action, and a published representation.

## Relationship

A **relationship** connects two entities in a meaningful way.

Relationships are not merely hyperlinks. They describe why two subjects belong on the same trail.

## Authority

**Authority** is contextual standing.

KARADAVI does not assume that one source is universally authoritative. A source may have strong standing for one kind of claim and little standing for another.

## Uncertainty

Not every knowledge state is true or false.

Information may be unknown, ambiguous, incomplete, stale, conflicting, unsupported, or contradicted.

KARADAVI treats those conditions as information rather than errors to hide.

## Evaluation

An **evaluation** interprets a claim using available evidence, provenance, authority, context, and uncertainty.

An evaluation can change when the evidence changes without rewriting the history of the underlying evidence.

## Connected state

Conceptually:

```text
                         ENTITY
                           │
              ┌────────────┼────────────┐
              │            │            │
              ▼            ▼            ▼
            CLAIM       CONTEXT      RELATION
              │                         │
              ▼                         ▼
           EVIDENCE                  ENTITY
              │
              ▼
         PROVENANCE
              │
              ▼
          AUTHORITY
              │
              ▼
        UNCERTAINTY
              │
              ▼
         EVALUATION
```

This is a research model, not a claim that all knowledge can be perfectly formalized.

## Why separate these concepts?

Because collapsing them destroys useful context.

A source is not the same thing as a claim.

A claim is not the same thing as truth.

Publication is not the same thing as certainty.

Authority is not the same thing as popularity.

Confidence is not the same thing as proof.

A relationship is not the same thing as a hyperlink.

The public KARADAVI model exists to keep those distinctions visible.
