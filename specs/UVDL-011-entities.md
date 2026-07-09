# UVDL-011 — Entity Specification

**Status:** Draft  
**Version:** 0.2.0 Ontology  
**Last Updated:** 2026-07-09  
**Depends on:** UVDL-010  
**Related:** UVDL-012, UVDL-013  

## Purpose

Define the seven primary entities of UVDL.

## Scope

This specification covers only primary ontology entities.

## Non-Goals

This specification does not define component implementations, token values, or visual style.

## Definitions

A primary entity is a stable concept that exists across all UVDL projects and implementations.

## Specification

UVDL MUST recognize exactly seven primary entities in v0.2 Ontology.

### 1. Human

A Human is the person using or affected by the digital product.

A Human MAY have multiple intents.

### 2. Intent

An Intent is a goal the Human wants to accomplish.

Examples:

- book service;
- find information;
- compare options;
- trust a company;
- contact support;
- complete purchase.

### 3. Decision

A Decision is a moment where the Human chooses the next action.

A Decision SHOULD be supported by clarity, evidence, and reduced friction.

### 4. Pattern

A Pattern is a repeatable solution that supports an Intent or Decision.

Examples:

- Conversion Surface;
- Trust Region;
- Progressive Disclosure;
- Service Selection;
- Data Collection Pattern.

### 5. Component

A Component is a reusable implementation unit that realizes one or more Patterns.

Examples:

- Action;
- Information Surface;
- Input;
- Navigation Item;
- Disclosure Control.

### 6. Token

A Token is a semantic value used to style or configure Components.

Examples:

- surface.primary;
- text.body;
- action.primary.background;
- radius.medium;
- spacing.region.

### 7. Implementation

An Implementation is the concrete expression of a Component, Pattern, or Template in code or platform-specific format.

Examples:

- HTML;
- CSS;
- JavaScript;
- HostCMS XSL;
- React component;
- JSON/YAML schema.

## Rationale

The entity model must remain small enough to be used in practice.

Additional concepts such as Knowledge, Evidence, Experiment, Theme, and Template are important but are not primary ontology entities in v0.2.

They may be defined as secondary entities later.

## Examples

A booking flow may be described as:

```text
Human → Intent(book repair) → Decision(contact or not) → Pattern(Conversion Surface) → Component(Primary Action) → Token(action.primary) → Implementation(button)
```

## References

- `specs/UVDL-010-ontology.md`
- `TERMINOLOGY.md`

## Revision History

| Version | Date | Changes |
|---|---|---|
| 0.2.0 | 2026-07-09 | Initial entity specification |
