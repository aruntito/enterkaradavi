# 003 — Uncertainty Should Propagate

**Status:** hypothesis

## Question

What should happen when uncertain inputs are used to derive a new claim or trust signal?

## Hypothesis

Derived state should preserve material uncertainty from its inputs instead of silently converting ambiguous inputs into precise outputs.

## Proposed model

```text
Uncertain observation
        ↓
Uncertain evidence
        ↓
Claim with known limitations
        ↓
Evaluation with explicit uncertainty
        ↓
Trust signal with visible uncertainty
```

## Research constraints

A useful representation should distinguish at least:

- missing information;
- conflicting information;
- ambiguous identity;
- stale information; and
- uncertainty introduced by the evaluation method.

## Failure mode

A system that produces a single precise number from uncertain or conflicting inputs can create false confidence downstream even when every individual component behaved as designed.

## Next experiment

Create synthetic evidence graphs with one uncertain input at a time and test whether the resulting state can identify which uncertainty entered the evaluation and whether it materially affected the disposition.
