# ADR-006 — CSS Layer Structure

**Status:** Accepted  
**Date:** 2026-07-09  
**Version:** 0.3.0 CSS MVP  

## Context

The initial CSS MVP placed all files directly in `packages/css/`.

As the system grows, this flat structure makes it harder to distinguish foundational files from primitive components and future composite patterns.

## Decision

UVDL CSS will be organized by responsibility:

```text
packages/css/
  foundation/
    fonts.css
    foundation.css
    base.css
    typography.css
    layout.css

  primitives/
    action.css
    surface.css
    field.css
    media.css
    status.css
    notice.css

  composites/
    hero.css
    faq.css
    catalog.css
    contact.css
```

## Rules

- `foundation/` contains global foundations and utilities.
- `primitives/` contains universal interface building blocks.
- `composites/` contains reusable patterns assembled from primitives.
- Business-domain CSS does not belong to UVDL Core.

## Consequences

### Positive

- Clearer responsibility boundaries.
- Easier scaling.
- Better alignment with UVDL ontology.
- Better separation between primitive components and composite patterns.

### Negative

- Existing imports must be updated.
- More directory depth.

## Example

A service card should be assembled as:

```html
<article class="surface surface-card service-card">
  ...
</article>
```

`surface surface-card` is UVDL Core.

`service-card` is project-specific.
