# Public / Private Boundary

KARADAVI is intentionally split between a public research surface and a private implementation surface.

## Public: `enterkaradavi`

The public repository is for material that helps other engineers and researchers understand and evaluate the ideas:

- architecture
- research models
- specifications
- schemas intended for public use
- reference examples
- reproducible experiments
- documentation

## Private: `karadavi`

The private repository remains the home for material that should not be publicly released, including:

- proprietary implementation
- private datasets
- deployment configuration
- internal infrastructure details
- credentials and secrets
- unreleased product work
- operational tooling that is not intended for publication

## Boundary rule

A useful test before publishing is:

> Does this artifact explain or demonstrate the public research without exposing private implementation or operational knowledge?

If the answer is unclear, keep the artifact private until it has been reviewed.

The public repository should stand on its own. It should not require access to the private repository to understand the public concepts.
