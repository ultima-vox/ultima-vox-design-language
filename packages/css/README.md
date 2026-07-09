# UVDL CSS Package

**Status:** Draft  
**Version:** 0.4.0 Architecture  

## Purpose

This package contains the first practical CSS implementation of UVDL.

The MVP is intentionally simple:

```text
manual tokens
  ↓
base CSS
  ↓
elements
  ↓
patterns
  ↓
reference project usage
```

No Builder, Compiler, Style Dictionary, schema validation, or generated CSS is used at this stage.

## Structure

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

  patterns/
    coming later
```

## Foundation Files

- `foundation/fonts.css` — project font roles and presets.
- `foundation/tokens.css` — readable CSS custom properties.
- `foundation/base.css` — reset and base HTML element styles.
- `foundation/typography.css` — text scale utility classes.
- `foundation/layout.css` — container, section, stack, cluster and grid utilities.

## Element Files

- `elements/action.css` — universal action element.
- `elements/brand.css` — universal brand identity element.
- `elements/navigation.css` — universal navigation element.
- `elements/surface.css` — universal information surface element.

## Usage

```html
<link rel="stylesheet" href="/path/to/uvdl/foundation/base.css">
<link rel="stylesheet" href="/path/to/uvdl/foundation/typography.css">
<link rel="stylesheet" href="/path/to/uvdl/foundation/layout.css">
<link rel="stylesheet" href="/path/to/uvdl/elements/action.css">
<link rel="stylesheet" href="/path/to/uvdl/elements/brand.css">
<link rel="stylesheet" href="/path/to/uvdl/elements/navigation.css">
<link rel="stylesheet" href="/path/to/uvdl/elements/surface.css">
```

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

## Architecture Rule

Core CSS must avoid business-domain names.

Good:

```html
<article class="surface surface-card">
```

Project-specific:

```html
<article class="surface surface-card service-card">
```

`surface surface-card` belongs to UVDL.

`service-card` belongs to the project.

## Brand Rule

UVDL may define brand structure, but not project-specific identity assets.

Good:

```html
<a class="brand" href="/" aria-label="Homepage">
  <img class="brand-mark" src="/logo.svg" alt="">
  <span class="brand-text">
    <span class="brand-name">Project Name</span>
    <span class="brand-tagline">Project tagline</span>
  </span>
</a>
```

`brand`, `brand-mark`, `brand-name`, and `brand-tagline` belong to UVDL.

The logo file, project name, and tagline belong to the project.

## Navigation Rule

UVDL defines navigation as movement between information areas.

Header, footer, tabs, breadcrumbs, pagination and sidebars are patterns that may use `navigation`.

Good:

```html
<nav class="navigation navigation-horizontal" aria-label="Primary navigation">
  <ul class="navigation-list">
    <li class="navigation-item">
      <a class="navigation-link" href="/" aria-current="page">Home</a>
    </li>
  </ul>
</nav>
```

## Rule

If something can be written manually in 10 minutes, do not automate it yet.

Automation appears after repeated practical pain.
