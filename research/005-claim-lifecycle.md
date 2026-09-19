# 005 — Claim Lifecycle and Conflict Semantics

**Status:** hypothesis / active research

## Question

How should a knowledge system represent a claim as it changes over time without rewriting history or confusing representation state with truth?

## Hypothesis

A claim lifecycle should preserve prior states and make transitions explicit. Disagreement should be represented as state, not erased by replacing one claim with another.

## Proposed model

```text
                 +--------------+
                 |    unknown   |
                 +------+-------+
                        |
                        v
                 +--------------+
                 |   asserted   |
                 +---+------+----+
                     |      |
                     v      v
                disputed  retracted
                     |
                     +------> asserted
```

The exact transition rules remain experimental.

## Design constraints

A useful lifecycle should preserve:

- claim identity;
- state transition;
- transition time;
- evidence relevant to the transition;
- actor or process responsible for the transition;
- evaluation context; and
- prior states where historical reconstruction matters.

## Important distinction

asserted, disputed, and retracted describe the state of the knowledge representation. They are not synonyms for true, false, or permanently resolved.

A claim can be asserted while still carrying material uncertainty. A disputed claim can later become supported after new evidence appears.

## Failure modes

- overwriting a previous state and losing history;
- treating retraction as proof that the proposition was always false;
- resolving conflicts by source popularity alone;
- allowing stale evidence to keep a claim permanently current;
- confusing an editorial workflow state with an epistemic evaluation.

## Next experiment

Create a synthetic timeline where the same claim receives supporting, conflicting, stale, and corrective evidence. Test whether the representation can reconstruct what was known at each evaluation time without mutating historical observations.
