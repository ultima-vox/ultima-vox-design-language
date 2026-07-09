# ADR-003 — Manual CSS Before Builder

**Status:** Accepted  
**Date:** 2026-07-09  
**Version:** 0.3.0 CSS Tokens MVP  

## Context

UVDL previously considered a future Builder, schemas, YAML graph, and generated CSS artifacts.

That direction is valid long-term, but it increases complexity before the system has enough real-world usage.

The first practical goal is to build `mechaniki.ru` using UVDL principles.

## Decision

UVDL will start with manually maintained CSS token files.

No Builder, Compiler, Style Dictionary pipeline, schema validation, or token generation is required for the MVP.

The initial implementation path is:

```text
Markdown specification
  ↓
Manual CSS tokens
  ↓
Manual components
  ↓
Patterns
  ↓
mechaniki.ru reference implementation
```

## Consequences

### Positive

- Lower complexity.
- Faster path to real project usage.
- Easier iteration while token architecture is still forming.
- No premature tooling lock-in.

### Negative

- Manual token maintenance may become repetitive later.
- Platform-specific outputs are not automatic.
- Future migration to generated tokens may require refactoring.

## Rule

If something can be written manually in 10 minutes, UVDL should not automate it yet.

Automation appears after repeated pain, not before it.

## Future Option

A Builder or Style Dictionary pipeline may be reconsidered after UVDL has been used across several real projects and token repetition becomes a measurable maintenance problem.
