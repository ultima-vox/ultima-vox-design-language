# Versioning

**Status:** Draft  
**Version:** 0.1.0 Foundation  
**Last Updated:** 2026-07-09  

## Purpose

This document defines how UVDL releases are versioned.

## Versioning Model

UVDL uses semantic versioning principles:

```text
MAJOR.MINOR.PATCH
```

## Release Stages

### v0.1 — Foundation
Project purpose, governance, knowledge model, terminology, and architecture.

### v0.2 — Tokens
Semantic design tokens: color, typography, spacing, radius, elevation, motion.

### v0.3 — Components
Reference component model and first implementation primitives.

### v0.4 — Patterns
Reusable design and UX patterns.

### v0.5 — Templates
Page-level and experience-level templates.

### v0.6 — HostCMS
HostCMS integration guidelines and reference implementation.

### v0.7 — CLI
Initial validation tooling.

### v0.8 — Knowledge
Structured knowledge base and validation records.

### v0.9 — Beta
Stabilization before production release.

### v1.0 — Production
Stable UVDL release suitable for production projects.

## Change Types

### Major
Breaking changes to terminology, architecture, token model, or component contracts.

### Minor
New stable features, tokens, patterns, templates, or validated knowledge.

### Patch
Clarifications, typo fixes, documentation improvements, non-breaking corrections.

## Stability Rule

Before v1.0, Core may change, but every significant change must be documented.

After v1.0, breaking changes require a migration note.
