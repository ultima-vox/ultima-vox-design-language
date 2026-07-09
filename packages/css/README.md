# UVDL CSS Package

**Status:** Draft  
**Version:** 0.3.0 CSS MVP  

## Purpose

This package contains the first practical CSS implementation of UVDL.

The MVP is intentionally simple:

```text
manual foundation tokens
  ↓
base CSS
  ↓
manual component CSS
  ↓
reference project usage
```

No Builder, Compiler, Style Dictionary, schema validation, or generated CSS is used at this stage.

## Files

- `foundation.css` — readable CSS custom properties.
- `base.css` — reset and base HTML element styles.

## Usage

```html
<link rel="stylesheet" href="/path/to/uvdl/base.css">
```

`base.css` imports `foundation.css`.

## Naming Rule

UVDL CSS tokens do not use a brand prefix in the MVP.

Prefer readable names:

```css
--surface-page
--text-primary
--action-primary-bg
--space-4
--radius-md
```

## Rule

If something can be written manually in 10 minutes, do not automate it yet.

Automation appears after repeated practical pain.
