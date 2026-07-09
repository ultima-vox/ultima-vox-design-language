# ADR-007 — Brand as Secondary Entity

**Status:** Accepted  
**Date:** 2026-07-09  
**Version:** 0.3.0 CSS MVP  

## Context

The UVDL ontology intentionally keeps seven primary entities:

```text
Human → Intent → Decision → Pattern → Component → Token → Implementation
```

A Brand element is needed in almost every digital product:

- header;
- footer;
- hero;
- login page;
- splash screen;
- document templates;
- email templates.

However, making Brand an eighth primary entity would weaken the small ontology model.

## Decision

Brand is a secondary entity in UVDL.

Brand represents the identity expression of a project or organization inside an interface.

Brand is implemented as a Component and expressed through Implementation.

## Rules

- Brand is not a primary ontology entity.
- Brand belongs to the interface language because it appears across many patterns.
- Brand must not contain project-specific assets in UVDL Core.
- UVDL Core may define Brand structure and behavior.
- Specific logos, names, slogans, icons, and legal text belong to projects.

## CSS Layer

UVDL provides a primitive CSS file:

```text
packages/css/primitives/brand.css
```

It defines universal brand presentation classes such as:

```css
.brand
.brand-mark
.brand-name
.brand-tagline
```

## Consequences

### Positive

- Keeps the primary ontology small.
- Gives brand identity a reusable interface role.
- Avoids mixing project-specific assets into Core.
- Supports header, footer, hero, and document patterns.

### Negative

- Brand is not part of the primary chain.
- Some documentation must distinguish primary and secondary entities clearly.

## Example

```html
<a class="brand" href="/" aria-label="Homepage">
  <img class="brand-mark" src="/logo.svg" alt="">
  <span class="brand-name">Project Name</span>
</a>
```
