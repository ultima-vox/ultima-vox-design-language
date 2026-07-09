# UVDL-020 — CSS Token Model MVP

**Status:** Draft  
**Version:** 0.3.0 CSS Tokens MVP  
**Last Updated:** 2026-07-09  
**Depends on:** UVDL-010, UVDL-011, UVDL-012, ADR-003  
**Related:** `packages/css/tokens.css`  

## Purpose

Define the first practical token model for UVDL using manually maintained CSS custom properties.

## Scope

This specification covers MVP CSS tokens used by UVDL reference implementations.

## Non-Goals

This specification does not define:

- token generators;
- Style Dictionary integration;
- JSON/YAML token pipelines;
- Figma variables;
- SCSS output;
- platform-specific mobile tokens.

## Definitions

A CSS Token is a CSS custom property that represents a reusable design decision.

## Specification

UVDL CSS tokens MUST be implemented as CSS custom properties.

Tokens MUST be grouped by purpose:

- color;
- typography;
- spacing;
- radius;
- shadow;
- motion;
- layout;
- z-index.

Components SHOULD use semantic tokens where practical.

Primitive-looking values MAY exist in the MVP if they make implementation faster, but they SHOULD NOT leak into component-level CSS when a semantic token is available.

## Naming

Token names MUST use kebab-case.

Token names MUST use the `--uv-` prefix.

Examples:

```css
--uv-color-surface-page
--uv-color-text-primary
--uv-space-4
--uv-radius-md
```

## Minimal Token Layers

For the MVP, UVDL uses two practical layers:

```text
Base tokens
  ↓
Semantic tokens
```

Theoretical intent tokens are deferred until they become necessary in real project work.

## Rationale

The MVP must be useful before it is perfect.

Manual CSS tokens allow UVDL to be applied to `mechaniki.ru` immediately without premature tooling.

## Examples

```css
:root {
  --uv-color-surface-page: #ffffff;
  --uv-color-text-primary: #111827;
  --uv-color-action-primary-bg: #d71920;
  --uv-space-4: 1rem;
  --uv-radius-md: 0.75rem;
}
```

## References

- `adr/ADR-003-manual-css-before-builder.md`
- `packages/css/tokens.css`

## Revision History

| Version | Date | Changes |
|---|---|---|
| 0.3.0 | 2026-07-09 | Initial CSS token model MVP |
