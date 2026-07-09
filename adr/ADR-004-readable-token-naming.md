# ADR-004 — Readable Token Naming

**Status:** Accepted  
**Date:** 2026-07-09  
**Version:** 0.3.0 CSS Tokens MVP  

## Context

The initial CSS token MVP used the `--uv-` prefix for all custom properties.

This reduced readability and made token names unnecessarily verbose.

UVDL values clarity and simple correct solutions over defensive naming.

## Decision

UVDL CSS tokens will not use a brand prefix in the MVP.

Token names should read like ordinary semantic language.

Examples:

```css
--surface-page
--text-primary
--action-primary-bg
--space-4
--radius-md
```

## Naming Rules

- Token names use kebab-case.
- Token names do not use the `uv` prefix.
- Semantic color tokens do not need the word `color` if the meaning is clear.
- Foundation tokens keep their category name when useful: `space`, `radius`, `font`, `duration`, `shadow`, `z`.
- Names should be understandable without documentation.

## Consequences

### Positive

- Shorter token names.
- Better readability.
- Easier authoring.
- CSS feels less framework-specific.

### Negative

- Higher risk of variable collisions if UVDL is embedded into an uncontrolled environment.

## Mitigation

If a future use case requires namespacing, a scoped build or optional prefixed distribution may be introduced later.

The MVP prioritizes readability.
