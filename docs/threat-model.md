# Threat Model

KARADAVI is concerned with systems making decisions from digital information. The public model therefore treats manipulation of evidence and context as first-class risks.

## Threats under consideration

- **Source spoofing** — information appears to originate from a more authoritative source than it actually does.
- **Evidence tampering** — supporting material is modified, truncated, or selectively presented.
- **Provenance loss** — transformations remove the information needed to understand origin.
- **Entity confusion** — two distinct entities are incorrectly resolved as one, or one entity is split into multiple identities.
- **Context collapse** — a source that is authoritative in one context is incorrectly treated as authoritative everywhere.
- **Stale state** — previously valid information remains trusted after the underlying state changes.
- **Conflict suppression** — competing claims disappear instead of remaining visible to evaluation.
- **False precision** — uncertain inputs produce an apparently exact trust score.
- **Model capture** — an evaluation mechanism systematically favors a source or class of evidence for reasons unrelated to the claim.

## Security posture

The public repository describes concepts and schemas. It is not a security guarantee for any particular deployment. Implementations must establish their own controls for authenticity, integrity, access, storage, and operational security.

## Research questions

1. Which provenance fields are minimally necessary to detect meaningful tampering?
2. How should stale evidence affect a trust evaluation?
3. How can conflicting authoritative sources be represented without silently selecting one?
4. Which attacks become possible when downstream systems consume trust signals without their evidence context?
5. How should an implementation communicate that an evaluation is incomplete?

## Boundary

This document intentionally avoids private deployment topology, credentials, internal endpoints, or unreleased implementation details.
