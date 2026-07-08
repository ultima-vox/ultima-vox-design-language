# Governance

**Status:** Draft  
**Version:** 0.1.0 Foundation  
**Last Updated:** 2026-07-09  

## Purpose

This document defines how UVDL evolves.

## Core Rule

UVDL must make product development simpler, not more complex.

If a concept increases complexity without measurable value, it must remain in Lab or be rejected.

## Development Flow

Every significant idea follows this path:

```text
Idea
  ↓
Discussion
  ↓
RFC
  ↓
Prototype
  ↓
Experiment
  ↓
Metrics
  ↓
Review
  ↓
ADR
  ↓
Core
```

## Confidence Levels

| Level | Meaning |
|---|---|
| L0 | Idea only |
| L1 | Theoretical rationale exists |
| L2 | Prototype exists |
| L3 | Validated on one project |
| L4 | Validated on multiple projects |
| L5 | UVDL Core standard |

## Project Areas

### Core
Stable specification and reusable decisions.

### Lab
Research ideas, hypotheses, and experimental models.

### Experiments
Validation work on real projects.

### Knowledge
Validated knowledge, proofs, and reusable evidence.

## Acceptance Rule

Nothing enters Core without:

- documented problem;
- rationale;
- review;
- practical validation or clear engineering necessity;
- ADR.

## Rejection Rule

An idea may be rejected if it:

- duplicates an existing concept;
- adds terminology without clarity;
- cannot be implemented;
- cannot be validated;
- increases complexity without practical value.
