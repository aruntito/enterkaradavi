# Research Model

KARADAVI treats machine trust as a research problem rather than a single algorithm.

## Working model

A useful trust representation should preserve at least four dimensions:

```text
Claim
 ├── Entity / subject
 ├── Evidence
 ├── Provenance
 ├── Authority context
 └── Uncertainty
```

A trust signal is therefore better understood as a structured interpretation of evidence than as an unexplained score.

## Questions under investigation

- How should entities be represented across heterogeneous sources?
- How should conflicting claims be preserved and compared?
- How can provenance survive transformations between systems?
- How should contextual authority be modeled?
- How should uncertainty propagate through derived claims?
- What minimum information does a downstream machine need to evaluate a trust signal?

## Evidence over assertion

KARADAVI should prefer a chain such as:

```text
Observation → Evidence → Claim → Evaluation → Trust Signal
```

rather than:

```text
Observation → Score
```

The first model leaves room for inspection, disagreement, and re-evaluation.

## Experimental discipline

Public research should identify assumptions, define terms, document inputs, record limitations, and make results reproducible where practical.

A failed experiment is still useful when it narrows the design space or exposes an invalid assumption.

## Non-goals

KARADAVI is not intended to:

- become a generic chatbot;
- replace source-specific expertise with one universal score;
- hide uncertainty behind confident language; or
- claim that a single trust metric can solve all information-quality problems.
