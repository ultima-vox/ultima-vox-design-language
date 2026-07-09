# ADR-002 — English as Canonical Language

**Status:** Accepted  
**Date:** 2026-07-09  
**Version:** 0.2.0 Ontology  

## Context

UVDL is intended to become a long-lived engineering specification.

Most major engineering specifications, RFCs, web standards, and open-source projects use English as the canonical language.

## Decision

The canonical language of UVDL is English.

Translations MAY exist, but English is the source of truth for Core specifications, RFCs, ADRs, ontology, and machine-readable models.

## Consequences

### Positive

- Easier alignment with global engineering practices.
- Better compatibility with RFC/W3C-style documentation.
- Easier future open-source usage.
- Better compatibility with AI and tooling.

### Negative

- Russian-language discussion may need summarization into English specifications.
- Additional translation work may be needed later.

## Alternatives Considered

### Russian as canonical language
Rejected because it limits future interoperability and reuse.

### Dual canonical languages
Rejected because it creates ambiguity and maintenance overhead.
