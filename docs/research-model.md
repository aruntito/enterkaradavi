# Research Model

KARADAVI treats machine trust as a research problem rather than a single algorithm.

## Working model

A useful trust representation preserves the structure behind a conclusion:

```text
Claim
 ├── Subject / entity
 ├── Evidence
 ├── Provenance
 ├── Authority context
 ├── Evaluation context
 └── Uncertainty
```

A trust signal is therefore a structured interpretation of evidence, not an unexplained number.

## Evidence over assertion

KARADAVI prefers:

```text
Observation → Evidence → Claim → Evaluation → Trust Signal
```

over:

```text
Observation → Score
```

The first model supports inspection, disagreement, re-evaluation, and new evidence.

## Claim vs evidence

A claim is an assertion about a subject or relationship.

Evidence is an observable or attributable basis that can support, weaken, contextualize, or contradict that claim.

They should not be collapsed into one object because:

- evidence can support multiple claims;
- one claim can have multiple evidence records;
- evidence can conflict;
- a claim can outlive a particular source snapshot; and
- evaluations may change without changing the underlying evidence.

## Provenance

Every derived signal should be traceable to its relevant inputs where practical.

A provenance chain can be represented conceptually as:

```text
Source
  ↓
Observation
  ↓
Extraction / interpretation
  ↓
Claim
  ↓
Evaluation
  ↓
Trust signal
```

The goal is not perfect historical reconstruction of every computation. The goal is enough provenance to make important decisions inspectable.

## Authority is contextual

KARADAVI does not assume a permanent global ranking of sources.

Authority may depend on:

- the type of claim;
- the relevant jurisdiction or domain;
- the time at which the claim is evaluated;
- the relationship between source and subject; and
- the declared purpose of the evaluation.

This keeps authority separate from popularity or generic reputation.

## Uncertainty propagation

A downstream result should not appear more certain than its relevant inputs justify.

Useful states include:

| State | Meaning |
| --- | --- |
| `unknown` | insufficient information |
| `ambiguous` | multiple plausible interpretations |
| `supported` | evidence supports the claim |
| `conflicting` | relevant evidence disagrees |
| `unsupported` | no adequate supporting evidence |
| `disproven` | available evidence contradicts the claim |

These labels are a starting research vocabulary, not a finalized standard.

## Questions under investigation

- How should entities be represented across heterogeneous sources?
- How should conflicting claims be preserved and compared?
- How can provenance survive transformations between systems?
- How should contextual authority be modeled?
- How should uncertainty propagate through derived claims?
- What minimum information does a downstream machine need to evaluate a trust signal?
- Which parts of the model should be normative versus implementation-specific?

## Experimental discipline

Public research should identify:

1. the problem;
2. assumptions;
3. proposed mechanism;
4. evidence or observations;
5. limitations;
6. unresolved questions; and
7. the next experiment.

A failed experiment is useful when it narrows the design space or exposes an invalid assumption.

## Non-goals

KARADAVI is not intended to:

- become a generic chatbot;
- replace source-specific expertise with one universal score;
- hide uncertainty behind confident language; or
- claim that one trust metric can solve all information-quality problems.
