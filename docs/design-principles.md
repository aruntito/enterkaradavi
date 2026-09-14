# Design Principles

These principles guide the public KARADAVI model.

1. **Provenance first** — preserve origin and transformation history.
2. **Context matters** — authority and trust are evaluated in context.
3. **Uncertainty is data** — ambiguity, absence, conflict, and staleness must remain representable.
4. **Evidence is inspectable** — derived signals should be traceable to their inputs.
5. **Claims are first-class objects** — do not bury assertions inside opaque records.
6. **Identity is explicit** — unresolved or competing entity matches remain visible.
7. **Trust is contextual** — avoid pretending one universal score works for every domain.
8. **Machine-readable by design** — public concepts should have structured representations where practical.
9. **Experimental claims stay labeled** — hypotheses and proposals are not presented as standards.
10. **Public surface stays independent** — the research repository must remain understandable without private implementation access.

## A practical test

For any proposed trust mechanism, ask:

> Can another system inspect what was observed, what was claimed, what evidence supports it, what authority context applies, and what remains uncertain?

If not, the mechanism is probably hiding too much reasoning inside a single output.
