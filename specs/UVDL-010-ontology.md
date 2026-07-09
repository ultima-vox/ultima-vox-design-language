# UVDL-010 — Ontology Specification

**Status:** Draft  
**Version:** 0.2.0 Ontology  
**Last Updated:** 2026-07-09  
**Depends on:** UVDL Foundation  
**Related:** UVDL-011, UVDL-012, UVDL-013  

## Purpose

Define the minimum ontology of Ultima Vox Design Language.

## Scope

This specification defines the top-level entities and conceptual layers used by UVDL.

## Non-Goals

This specification does not define visual tokens, component APIs, CSS, HTML, or implementation details.

## Definitions

Ontology is the shared model of what exists in UVDL and how those things relate.

## Specification

UVDL MUST use the following seven top-level entities:

1. Human
2. Intent
3. Decision
4. Pattern
5. Component
6. Token
7. Implementation

The canonical conceptual chain is:

```text
Human → Intent → Decision → Pattern → Component → Token → Implementation
```

Knowledge, Experiment, and Evidence are not primary design entities.

They are metadata layers that explain why a design entity exists, how it was validated, and how confident UVDL is in it.

## Entity Roles

### Human
The person using or affected by the product.

### Intent
What the human wants to accomplish.

### Decision
A point where the human chooses what to do next.

### Pattern
A repeatable solution that supports a decision or intent.

### Component
A reusable implementation unit that realizes a pattern.

### Token
A semantic value used to style or configure components.

### Implementation
The concrete code, markup, CMS template, or runtime expression.

## Rationale

The ontology intentionally remains small.

If the model cannot be explained on one page, it is too complex for UVDL v0.2.

## Examples

```text
Human: car owner
Intent: book repair
Decision: choose whether to contact the service
Pattern: Conversion Surface
Component: Primary Action
Token: action.primary.background
Implementation: HTML button + CSS custom properties
```

## References

- `ARCHITECTURE.md`
- `TERMINOLOGY.md`
- `KNOWLEDGE_MODEL.md`

## Revision History

| Version | Date | Changes |
|---|---|---|
| 0.2.0 | 2026-07-09 | Initial ontology draft |
