# UVDL-012 — Relationship Specification

**Status:** Draft  
**Version:** 0.2.0 Ontology  
**Last Updated:** 2026-07-09  
**Depends on:** UVDL-010, UVDL-011  
**Related:** UVDL-013  

## Purpose

Define allowed relationships between primary UVDL entities.

## Scope

This specification covers relationships between Human, Intent, Decision, Pattern, Component, Token, and Implementation.

## Non-Goals

This specification does not define data schemas, validation tooling, or graph storage format.

## Definitions

A relationship is a directional semantic link between two entities.

## Specification

UVDL v0.2 defines the following primary relationships.

| Source | Relationship | Target | Meaning |
|---|---|---|---|
| Human | has | Intent | A human has a goal |
| Intent | leads_to | Decision | An intent creates or requires a decision |
| Decision | supported_by | Pattern | A pattern helps resolve a decision |
| Pattern | realized_by | Component | A component implements a pattern |
| Component | styled_by | Token | A component uses tokens for presentation |
| Component | implemented_as | Implementation | A component becomes platform-specific code |
| Token | expressed_in | Implementation | A token becomes CSS, JSON, Figma variable, etc. |

## Relationship Rules

### Rule 1

A Component MUST NOT exist without a Pattern or explicit implementation need.

### Rule 2

A Pattern SHOULD support at least one Intent or Decision.

### Rule 3

A Token MUST be semantic before it is visual.

### Rule 4

Implementation MUST follow Core concepts, not Lab hypotheses.

### Rule 5

Knowledge MAY attach to any entity or relationship as evidence, rationale, or validation metadata.

## Rationale

Relationships define the grammar of UVDL.

Without relationships, UVDL would be only a dictionary of terms.

## Examples

```text
Human has Intent
Intent leads_to Decision
Decision supported_by Trust Region
Trust Region realized_by Review Surface
Review Surface styled_by surface.elevated
Review Surface implemented_as HTML article
```

## References

- `specs/UVDL-010-ontology.md`
- `specs/UVDL-011-entities.md`

## Revision History

| Version | Date | Changes |
|---|---|---|
| 0.2.0 | 2026-07-09 | Initial relationship specification |
