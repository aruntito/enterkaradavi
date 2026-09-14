# 004 — Entity Resolution Should Expose Ambiguity

**Status:** hypothesis

## Question

How should KARADAVI represent an observed artifact when multiple candidate entities could match it?

## Hypothesis

Entity resolution should produce explicit candidate relationships and uncertainty rather than forcing an early binary identity decision.

## Proposed model

```text
Observation
    ↓
Candidate A  ──┐
Candidate B  ──┼── resolution state
Candidate C  ──┘
```

The resolution state should retain enough context for a later evaluator to revisit the decision when new evidence appears.

## Why this matters

Incorrect identity can contaminate every downstream layer: semantics, evidence association, authority evaluation, and trust. An early wrong match can therefore create a chain of internally consistent but externally incorrect state.

## Evaluation criteria

A useful representation should capture:

- candidate entities;
- evidence supporting each candidate;
- evidence weakening each candidate;
- resolution status;
- unresolved ambiguity; and
- the method or rule that produced the candidates.

## Next experiment

Build synthetic observations that intentionally match multiple entities and test whether downstream claims remain correctly scoped while identity remains unresolved.
