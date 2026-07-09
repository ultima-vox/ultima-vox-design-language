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
    dialog.css
    disclosure.css
    field.css
    icon.css
    media.css
    navigation.css
    notice.css
    status.css
    surface.css

  patterns/
    catalog.css
    contact.css
    faq.css
    footer.css
    form.css
    header.css
    hero.css
    pricing.css
```

## Dependency Graph

Dependencies are one-way.

```text
Foundation
  ↓
Elements
  ↓
Patterns
  ↓
Templates
  ↓
Applications
```

Rules:

- Foundation imports nothing from Elements or Patterns.
- Elements may import Foundation.
- Patterns may import Foundation and use Elements in markup.
- Patterns must not depend on project business classes.
- Projects may import everything they need.

## Foundation Files

- `foundation/fonts.css` — project font roles and presets.
- `foundation/tokens.css` — readable CSS custom properties.
- `foundation/base.css` — reset and base HTML element styles.
- `foundation/typography.css` — text scale utility classes.
- `foundation/layout.css` — container, section, stack, cluster and grid utilities.

## Element Files

- `elements/action.css` — universal action element.
- `elements/brand.css` — universal brand identity element.
- `elements/dialog.css` — universal focused interaction element.
- `elements/disclosure.css` — universal show/hide information element.
- `elements/field.css` — universal input and form field element.
- `elements/icon.css` — universal icon element.
- `elements/media.css` — universal visual media element.
- `elements/navigation.css` — universal navigation element.
- `elements/notice.css` — user-facing notice element.
- `elements/status.css` — object state element.
- `elements/surface.css` — universal information surface element.

## Pattern Files

- `patterns/catalog.css` — scan, compare and choose from a collection.
- `patterns/contact.css` — choose a communication path or submit a request.
- `patterns/faq.css` — resolve doubts and reduce decision friction.
- `patterns/footer.css` — closing navigation, brand and meta information.
- `patterns/form.css` — provide structured information and complete a request.
- `patterns/header.css` — persistent orientation and primary navigation.
- `patterns/hero.css` — main intent and first decision.
- `patterns/pricing.css` — compare offers and choose a commitment level.

## Composition Matrix

| Pattern | Main Elements |
|---|---|
| Header | Brand · Navigation · Action · Surface |
| Hero | Surface · Media · Action · Status · Typography |
| Footer | Brand · Navigation · Surface · Typography |
| FAQ | Disclosure · Surface · Typography |
| Contact | Field · Action · Notice · Surface · Icon · Typography |
| Pricing | Surface · Status · Action · Icon · Typography |
| Catalog | Surface · Media · Status · Action · Icon · Typography |
| Form | Field · Action · Notice · Surface · Typography |

## Usage

```html
<link rel="stylesheet" href="/path/to/uvdl/foundation/base.css">
<link rel="stylesheet" href="/path/to/uvdl/foundation/typography.css">
<link rel="stylesheet" href="/path/to/uvdl/foundation/layout.css">
<link rel="stylesheet" href="/path/to/uvdl/elements/action.css">
<link rel="stylesheet" href="/path/to/uvdl/elements/brand.css">
<link rel="stylesheet" href="/path/to/uvdl/elements/dialog.css">
<link rel="stylesheet" href="/path/to/uvdl/elements/disclosure.css">
<link rel="stylesheet" href="/path/to/uvdl/elements/field.css">
<link rel="stylesheet" href="/path/to/uvdl/elements/icon.css">
<link rel="stylesheet" href="/path/to/uvdl/elements/media.css">
<link rel="stylesheet" href="/path/to/uvdl/elements/navigation.css">
<link rel="stylesheet" href="/path/to/uvdl/elements/notice.css">
<link rel="stylesheet" href="/path/to/uvdl/elements/status.css">
<link rel="stylesheet" href="/path/to/uvdl/elements/surface.css">
<link rel="stylesheet" href="/path/to/uvdl/patterns/catalog.css">
<link rel="stylesheet" href="/path/to/uvdl/patterns/contact.css">
<link rel="stylesheet" href="/path/to/uvdl/patterns/faq.css">
<link rel="stylesheet" href="/path/to/uvdl/patterns/footer.css">
<link rel="stylesheet" href="/path/to/uvdl/patterns/form.css">
<link rel="stylesheet" href="/path/to/uvdl/patterns/header.css">
<link rel="stylesheet" href="/path/to/uvdl/patterns/hero.css">
<link rel="stylesheet" href="/path/to/uvdl/patterns/pricing.css">
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

## Pattern Rule

A Pattern is a composition of Elements.

A Pattern should mostly define layout, spacing, alignment and responsive behavior.

A Pattern should not duplicate Element responsibility.

Good:

```html
<section class="hero">
  <div class="container hero-inner">
    <div class="hero-content">
      <h1 class="text-display">Main intent</h1>
      <p class="text-subtitle">Supporting explanation.</p>
      <div class="hero-actions">
        <a class="action action-main" href="#">Primary action</a>
      </div>
    </div>
    <div class="hero-media">
      <div class="media media-wide"></div>
    </div>
  </div>
</section>
```

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

## Notice and Status Rule

Notice and Status are not the same concept.

`notice` communicates something the human should know now.

```html
<div class="notice notice-warning">
  <div class="notice-content">
    <strong class="notice-title">Limited time</strong>
    <p class="notice-text">The offer ends soon.</p>
  </div>
</div>
```

`status` describes the state of an object.

```html
<span class="status status-success">
  <span class="status-dot" aria-hidden="true"></span>
  Available
</span>
```

## Icon Rule

Icons support recognition, orientation, or state.

Icons should not replace text by default.

```html
<span class="icon icon-sm" aria-hidden="true">
  <svg viewBox="0 0 24 24"></svg>
</span>
```

## Media Rule

Media displays visual content such as images, video, illustrations, maps, or embeds.

```html
<figure>
  <div class="media media-wide">
    <img src="/image.jpg" alt="Description">
  </div>
  <figcaption class="media-caption">Image caption</figcaption>
</figure>
```

## Disclosure Rule

Disclosure shows or hides related information on demand.

FAQ and accordion patterns may use `disclosure`.

```html
<details class="disclosure">
  <summary class="disclosure-summary">
    Question
    <span class="disclosure-indicator" aria-hidden="true">⌄</span>
  </summary>
  <div class="disclosure-content">
    Answer text.
  </div>
</details>
```

## Dialog Rule

Dialog temporarily moves the human into a focused interaction context.

Use it only when interruption is justified.

```html
<dialog class="dialog" aria-labelledby="dialog-title">
  <div class="dialog-panel">
    <header class="dialog-header">
      <div>
        <h2 class="dialog-title" id="dialog-title">Dialog title</h2>
        <p class="dialog-description">Short explanation.</p>
      </div>
      <button class="dialog-close" type="button" aria-label="Close">×</button>
    </header>
    <div class="dialog-body">
      Dialog content.
    </div>
    <footer class="dialog-footer">
      <button class="action action-neutral" type="button">Cancel</button>
      <button class="action action-main" type="button">Confirm</button>
    </footer>
  </div>
</dialog>
```

## Core Elements Status

The CSS Elements MVP is complete when the following files exist:

```text
action.css
brand.css
dialog.css
disclosure.css
field.css
icon.css
media.css
navigation.css
notice.css
status.css
surface.css
```

## Current Patterns Status

The initial commercial-site Patterns MVP currently includes:

```text
catalog.css
contact.css
faq.css
footer.css
form.css
header.css
hero.css
pricing.css
```

## Rule

If something can be written manually in 10 minutes, do not automate it yet.

Automation appears after repeated practical pain.
