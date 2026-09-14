# Maintainer Checklist

Use this checklist before merging substantial public changes.

## Research

- [ ] The question is explicit.
- [ ] Claims are separated from observations.
- [ ] Limitations are documented.
- [ ] Negative or conflicting evidence is preserved.

## Specifications

- [ ] Schema changes are intentional.
- [ ] Existing examples were checked.
- [ ] Compatibility impact is documented.
- [ ] Experimental vs candidate status is clear.

## Security and boundary

- [ ] No credentials or secrets.
- [ ] No private datasets or personal data.
- [ ] No internal endpoints or deployment topology.
- [ ] No unreleased private implementation details.

## Validation

- [ ] GitHub Actions passes.
- [ ] Documentation links are sensible.
- [ ] Changelog is updated when appropriate.
- [ ] Roadmap reflects the resulting state.
