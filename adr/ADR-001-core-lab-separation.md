# ADR-001 — Separate Core and Lab

**Status:** Accepted  
**Date:** 2026-07-09  
**Version:** 0.1.0 Foundation  

## Context

UVDL contains both practical production concepts and speculative research ideas.

Mixing these in one layer would make the system unstable and difficult to use in real projects.

## Decision

UVDL separates stable and experimental work:

- `core/` contains stable specification.
- `lab/` contains research concepts and hypotheses.
- `experiments/` contains validation attempts.
- `knowledge/` contains validated conclusions.

Ideas must follow this path:

```text
Lab → Experiment → Knowledge → Core
```

## Consequences

### Positive

- Core remains practical.
- Research can continue without blocking production work.
- Experimental ideas do not become standards too early.
- Real projects can safely consume Core.

### Negative

- More documentation discipline is required.
- Some ideas will take longer to become official.

## Alternatives Considered

### Single documentation layer
Rejected because it would mix hypotheses and standards.

### Core-only system
Rejected because UVDL needs space for research and long-term innovation.
