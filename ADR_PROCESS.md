# ADR Process

**Status:** Draft  
**Version:** 0.1.0 Foundation  
**Last Updated:** 2026-07-09  

## Purpose

ADR means Architecture Decision Record.

An ADR documents a decision that has been accepted and explains why it was made.

## Difference Between RFC and ADR

- RFC proposes a change.
- ADR records an accepted decision.

## When to Create an ADR

Create an ADR when a decision affects:

- architecture;
- terminology;
- Core rules;
- versioning;
- repository structure;
- implementation model;
- validation model;
- tooling strategy.

## ADR Lifecycle

```text
Proposed
  ↓
Accepted
  ↓
Deprecated / Superseded
```

## ADR Template

```markdown
# ADR-000 — Title

**Status:** Proposed / Accepted / Deprecated / Superseded  
**Date:** YYYY-MM-DD  
**Related RFC:**  

## Context

## Decision

## Consequences

### Positive

### Negative

## Alternatives Considered

## References
```

## Rule

No major UVDL decision should exist only in conversation history.

If a decision matters, it must be recorded as ADR.
