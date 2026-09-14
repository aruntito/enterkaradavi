# 002 — Authority Is Contextual

**Status:** hypothesis

## Question

Can a machine model source authority without treating authority as a universal property of the source?

## Hypothesis

Authority should be represented as a relationship between a source, a claim domain, and a context. A source can have strong standing for one class of claims and little or no standing for another.

## Proposed model

```text
Source + Claim scope + Context + Validity window
                         ↓
                 Authority context
```

## Why this matters

A global source ranking can hide important distinctions. A source may be official for a narrow record while being irrelevant to unrelated claims. Authority can also expire, be delegated, or depend on jurisdiction and scope.

## Evaluation criteria

A useful model should make it possible to answer:

- Why does this source have standing here?
- What is the scope of that standing?
- When is it valid?
- What limitations apply?
- What happens when two sources have competing authority contexts?

## Expected failure modes

- authority generalized beyond its declared scope;
- stale authority treated as current;
- delegated authority mistaken for primary authority;
- conflicts hidden by ranking alone.

## Next experiment

Construct synthetic claims with overlapping and conflicting authority contexts and compare whether the structured representation preserves enough information for a downstream evaluator to explain its decision.
