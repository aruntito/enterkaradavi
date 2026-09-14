# 001 — Trust Is Not a Score

**Status:** hypothesis / active research

## Question

Can a machine trust representation remain useful without collapsing evidence, provenance, authority, and uncertainty into one universal scalar?

## Hypothesis

For many machine-decision contexts, a structured trust state will be more useful and more inspectable than a single trust score.

## Proposed model

```text
Trust State
├── subject
├── claim
├── evidence[]
├── provenance[]
├── authority.context
├── evaluation.method
├── uncertainty
└── state
```

A consumer can then make its own decision while retaining the information needed to inspect the basis of that decision.

## Why a single score is insufficient

A score can hide important differences between two situations:

- strong evidence from an inappropriate authority;
- weak evidence from a highly relevant authority;
- conflicting sources;
- stale but previously strong evidence; or
- an unresolved identity match.

Two states could receive similar numeric scores while requiring very different downstream treatment.

## Example

Consider two sources making the same claim about an entity.

```text
Source A
  authority: high for this claim type
  evidence: direct
  freshness: current

Source B
  authority: unknown
  evidence: indirect
  freshness: current
```

A scalar model may reduce both into one number. A structured model preserves the reasons they differ.

## Evaluation criteria

A future implementation can test whether the structured model improves:

1. explainability;
2. conflict handling;
3. re-evaluation when evidence changes;
4. provenance preservation;
5. downstream decision quality; and
6. resistance to false certainty.

## Limitations

This is a conceptual hypothesis, not an empirical result. Different applications may legitimately require compact scores for ranking or thresholding. The research question is whether those scores should be derived from, rather than replace, the underlying structured state.

## Next experiment

Define a small synthetic corpus containing supported, conflicting, stale, ambiguous, and unsupported claims. Compare a scalar-only representation with the structured KARADAVI state model and evaluate how easily a consumer can explain and re-evaluate each decision.
