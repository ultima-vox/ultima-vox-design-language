# UVDL-014 — Semantic Graph Specification

**Status:** Draft  
**Version:** 0.2.0 Ontology  
**Last Updated:** 2026-07-09  
**Depends on:** UVDL-010, UVDL-011, UVDL-012, UVDL-013  
**Related:** `ontology/uvdl-ontology.yaml`  

## Purpose

Define how UVDL concepts may be represented as a semantic graph.

## Scope

This specification defines the minimum graph model needed to connect entities, relationships, rules, knowledge, and future tooling.

## Non-Goals

This specification does not define a database, graph query language, CLI implementation, or compiler.

## Definitions

A Semantic Graph is a directed graph where nodes represent UVDL concepts and edges represent meaningful relationships between them.

A Node is a graph representation of an entity, rule, pattern, token, component, implementation, or knowledge artifact.

An Edge is a directional relationship between two nodes.

## Specification

UVDL MAY represent its ontology as a semantic graph.

The graph MUST support:

- stable node identifiers;
- typed nodes;
- directional edges;
- relationship names;
- references to specifications;
- references to ADRs, RFCs, or experiments;
- validation status.

## Required Node Fields

Every graph node SHOULD include:

```yaml
id: string
name: string
type: string
status: draft | proposed | accepted | deprecated
spec: string | null
```

## Required Edge Fields

Every graph edge SHOULD include:

```yaml
id: string
source: string
relation: string
target: string
status: draft | proposed | accepted | deprecated
```

## Graph Rules

### Rule 1 — Stable IDs

Node IDs and edge IDs MUST be stable once accepted.

### Rule 2 — Directional Meaning

Edges MUST have directional meaning.

For example:

```text
Decision supported_by Pattern
```

is not equivalent to:

```text
Pattern supported_by Decision
```

### Rule 3 — Traceability

Accepted nodes and edges SHOULD reference at least one specification, ADR, RFC, or knowledge artifact.

### Rule 4 — Core Isolation

Core graph nodes MUST NOT depend on Lab-only nodes.

### Rule 5 — Minimal Model

The graph MUST remain understandable without tooling.

Tooling may improve navigation but must not be required to understand the base model.

## Example

```yaml
nodes:
  - id: primary-action
    name: Primary Action
    type: component
    status: draft
    spec: UVDL-011

edges:
  - id: primary-action-supports-decision
    source: primary-action
    relation: supports
    target: decision
    status: draft
```

## Rationale

Markdown documents are readable by humans but are not enough for tooling.

A semantic graph allows UVDL to become machine-readable while keeping human-readable specifications.

This enables future work such as:

- documentation generation;
- consistency checks;
- CLI validation;
- UX linting;
- AI-assisted design reasoning;
- dependency analysis.

## References

- `specs/UVDL-010-ontology.md`
- `specs/UVDL-011-entities.md`
- `specs/UVDL-012-relationships.md`
- `specs/UVDL-013-decision-model.md`
- `ontology/uvdl-ontology.yaml`

## Revision History

| Version | Date | Changes |
|---|---|---|
| 0.2.0 | 2026-07-09 | Initial semantic graph specification |
