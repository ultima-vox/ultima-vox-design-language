# ADR-006 — CSS Layer Structure

**Status:** Accepted  
**Date:** 2026-07-09  
**Version:** 0.4.0 Architecture  

## Context

The initial CSS MVP placed all files directly in `packages/css/`.

As the system grows, this flat structure makes it harder to distinguish foundational files from universal interface elements and reusable patterns.

The term `primitives` is technically accurate, but less aligned with UVDL as a design language.

The term `elements` better matches the language metaphor and is easier for designers, developers, and product teams to understand.

## Decision

UVDL CSS will be organized by responsibility:

```text
packages/css/
  foundation/
    fonts.css
    tokens.css
    base.css
    typography.css
    layout.css

  elements/
    action.css
    brand.css
    navigation.css
    surface.css
    field.css
    media.css
    notice.css
    status.css
    dialog.css
    disclosure.css

  patterns/
    header.css
    footer.css
    hero.css
    faq.css
    catalog.css
    pricing.css
    contact.css
```

## Rules

- `foundation/` contains global foundations and utilities.
- `elements/` contains universal interface building blocks.
- `patterns/` contains reusable compositions assembled from elements.
- Business-domain CSS does not belong to UVDL Core.
- `tokens.css` is the source of CSS custom properties.

## Consequences

### Positive

- Clearer responsibility boundaries.
- Easier scaling.
- Better alignment with UVDL as a language.
- Better separation between Elements and Patterns.
- More intuitive naming for non-engineering contributors.

### Negative

- Existing imports must be updated.
- More directory depth.
- Early users must migrate from `primitives/` to `elements/`.

## Example

A service card should be assembled as:

```html
<article class="surface surface-card service-card">
  ...
</article>
```

`surface surface-card` is UVDL Core.

`service-card` is project-specific.
