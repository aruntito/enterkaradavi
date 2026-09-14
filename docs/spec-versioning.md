# Specification Versioning

KARADAVI schemas are experimental until explicitly promoted.

## Version stages

### Experimental

The schema is a research artifact. Fields and semantics may change without compatibility guarantees.

### Candidate

The model has survived documented experiments and is being evaluated for compatibility. Changes should include migration notes.

### Stable

The schema has defined semantics, compatibility expectations, examples, and documented limitations. Breaking changes require a new major version.

## Change discipline

Every meaningful schema change should answer:

1. What problem does the change solve?
2. Is the change semantic, structural, or editorial?
3. Does it invalidate existing instances?
4. Can old and new representations coexist?
5. What experiment or evidence supports the change?

Do not encode a version number merely to make an artifact look mature. Versioning exists to make change understandable.
