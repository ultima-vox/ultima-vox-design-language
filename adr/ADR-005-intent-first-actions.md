# ADR-005 — Intent-First Actions

**Status:** Accepted  
**Date:** 2026-07-09  
**Version:** 0.3.0 CSS MVP  

## Context

The initial component layer started with `button.css` and Bootstrap-like variants such as `btn-primary` and `btn-secondary`.

This describes visual priority, but not user intent.

UVDL is built around the chain:

```text
Human → Intent → Decision → Pattern → Component → Implementation
```

A button is only one possible implementation of an action.

An action may be a link, button, card, menu item, floating control, or another interactive element.

## Decision

UVDL will use `Action` as the component-level concept instead of `Button`.

The CSS component is `action.css`.

The base class is:

```css
.action
```

Role-oriented variants are preferred over Bootstrap-style names:

```css
.action-main
.action-support
.action-neutral
.action-danger
```

Project-specific intents such as `book-service`, `estimate-price`, or `contact` should not become Core CSS classes.

They belong to project content, markup, analytics, data attributes, or project-specific theme layers.

## Consequences

### Positive

- Better alignment with UVDL ontology.
- CSS describes component role rather than HTML element type.
- The same component can be implemented as `<a>`, `<button>`, or another interactive element.
- Keeps Core universal and project-independent.

### Negative

- Developers familiar with Bootstrap may need to adjust naming habits.
- Existing `btn-*` naming is intentionally not used.

## Example

```html
<a class="action action-main" href="/booking/">
  Book service
</a>

<button class="action action-support" type="button">
  Ask a question
</button>
```

## Rule

Core defines universal action roles.

Projects map business intents to those roles.
