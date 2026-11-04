# Public / Private Boundary

KARADAVI is an open knowledge platform with a deliberately separated public research surface and private production implementation.

The separation protects the production system without making the public knowledge mission or research direction inaccessible.

## Public knowledge platform

KARADAVI's public-facing purpose is to make structured, connected knowledge accessible to readers and useful to downstream systems. Public access to knowledge and appropriate research outputs is central to the product direction.

Open knowledge does not require every internal component used to build and maintain it to be publicly released.

## Public repository: `aruntito/enterkaradavi`

This repository contains the public research and specification layer:

- product vision and public conceptual architecture;
- research questions, methods and findings suitable for publication;
- knowledge models and terminology;
- experimental schemas and specifications;
- synthetic reference examples and reproducible experiments;
- editorial and provenance principles;
- documentation and contribution guidance.

It is MIT-licensed as a public research/software artefact repository. That licence applies to this repository's contents, subject to the licence terms; it does not grant rights to the separate private product repository or unpublished materials.

## Private repository: `aruntito/karadavi`

The canonical production application repository remains private. It contains material not intended for public release, including:

- production application source code and proprietary implementation;
- private datasets or non-public source material;
- deployment configuration and internal infrastructure details;
- credentials, secrets and security-sensitive configuration;
- unreleased product work;
- operational tooling and internal workflows.

The private repository is the source of truth for production implementation. This public repository must not pretend to be a code mirror or imply that its research schemas represent every implementation detail.

## What can move from private to public?

A product lesson may inform public research when it can be expressed without exposing proprietary code, private data, security-sensitive details or confidential operations.

Before publishing, review the material for:

- private implementation details;
- credentials, secrets and internal endpoints;
- private or licensed datasets;
- personal or confidential information;
- deployment topology and security controls;
- claims about implementation status that have not been verified.

When uncertain, keep the material private until reviewed.

## Boundary rule

> Publish reusable knowledge and research; keep private implementation and operational security private.

The public repository should stand on its own. It should explain the public concepts and invite meaningful discussion without requiring access to the private repository.
