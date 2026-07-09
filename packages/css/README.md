# UVDL CSS Package

**Status:** Draft  
**Version:** 0.3.0 CSS Tokens MVP  

## Purpose

This package contains the first practical CSS implementation of UVDL.

The MVP is intentionally simple:

```text
manual CSS tokens
  ↓
manual component CSS
  ↓
reference project usage
```

No Builder, Compiler, Style Dictionary, schema validation, or generated CSS is used at this stage.

## Files

- `tokens.css` — initial CSS custom properties.

## Usage

```html
<link rel="stylesheet" href="/path/to/uvdl/tokens.css">
```

## Rule

If something can be written manually in 10 minutes, do not automate it yet.

Automation appears after repeated practical pain.
