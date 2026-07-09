# ADR-008 — Element Acceptance Criteria

**Status:** Accepted  
**Date:** 2026-07-09  
**Version:** 0.4.0 Architecture  

## Context

As UVDL evolves, there is a risk of adding new interface elements simply because they exist in other design systems.

This leads to duplicated concepts, inconsistent terminology, and an ever-growing API.

UVDL should remain a language with a compact and expressive vocabulary.

## Decision

A new Element may be introduced only if it satisfies all of the following criteria.

## Criteria

### 1. Independent Responsibility

An Element must represent a single, independent interface responsibility.

Examples:

- `Action` initiates an interaction.
- `Navigation` enables movement.
- `Field` receives information.
- `Surface` groups information.

Counterexample:

- `Button` is an HTML implementation of `Action`, not an independent responsibility.

### 2. Independent Existence

An Element must be meaningful outside any specific Pattern.

Examples:

- `Surface`
- `Field`
- `Navigation`

Counterexamples:

- `Hero Title`
- `Product Price`
- `Footer Logo`

These exist only inside larger compositions.

### 3. Rule of Three

An Element should normally appear in at least three different Patterns.

Examples:

`Media` appears in:

- Hero;
- Catalog Card;
- Article;
- Gallery.

`Brand` appears in:

- Header;
- Footer;
- Authentication;
- Splash.

Counterexample:

- `Hero Button` is used only in Hero and is therefore not an Element.

### 4. Non-Composability

A new Element must not be reproducible by combining or renaming existing Elements.

Examples:

| Candidate | Existing UVDL Element |
|---|---|
| Button | Action |
| Card | Surface |
| Badge | Status |
| Chip | Status |
| Menu | Navigation |
| Tabs | Navigation |
| Breadcrumbs | Navigation |
| Accordion | Disclosure |
| Modal | Dialog |
| Toast | Notice |
| Avatar | Media |

If an existing Element already expresses the same responsibility, no new Element should be created.

## Foundation Is Not an Element

Foundation defines the materials of the language.

Examples:

- tokens;
- typography;
- fonts;
- layout.

These are not interface Elements.

Typography defines how text is rendered.

It does not represent an object in the interface.

Therefore Typography belongs to Foundation.

## Consequences

This decision intentionally keeps the UVDL vocabulary small.

A smaller vocabulary improves:

- consistency;
- readability;
- learnability;
- long-term maintainability.

Patterns should be composed from existing Elements instead of introducing new ones whenever possible.

## Core Principle

Every new Element must prove why it cannot be expressed using the existing language.
