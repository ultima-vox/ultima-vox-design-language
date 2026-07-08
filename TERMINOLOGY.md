# Terminology

**Status:** Draft  
**Version:** 0.1.0 Foundation  
**Last Updated:** 2026-07-09  

## Purpose

This document defines the first shared vocabulary of UVDL.

## Terminology Rule

A new term is allowed only if it is:

- more precise;
- more reusable;
- easier to reason about;
- not just a decorative replacement for a common word.

## Foundational Terms

### Intent
What the user is trying to accomplish.

Examples:

- find a service;
- compare options;
- trust a company;
- book a visit;
- contact support.

### Decision
A moment where the user chooses what to do next.

### Action
An interface element or pattern that allows the user to do something.

Common implementation: button, link, submit control.

### Primary Action
The most important next step in the current context.

### Secondary Action
A useful but less important next step.

### Content Region
A meaningful area of an interface that answers one user question or supports one intent.

Common implementation: section.

### Conversion Surface
A high-priority content region designed to orient the user and move them toward a decision.

Common implementation: hero, promo block, landing header.

### Information Surface
A bounded surface that groups related information.

Common implementation: card, tile, panel.

### Trust Region
A content region that reduces perceived risk and increases confidence.

Examples: reviews, guarantees, real photos, certificates, ratings.

### Evidence
Information that supports a claim.

Examples: reviews, cases, metrics, photos, guarantees.

### Progressive Disclosure
A pattern that reveals information gradually to reduce cognitive load.

Common implementation: accordion, tabs, expandable content.

### Data Collection Pattern
A pattern used to collect information from the user.

Common implementation: form.

## Deprecated as Primary Terms

The following terms may still be used in implementation, but they are not preferred as language-level concepts:

| Common Term | UVDL Term |
|---|---|
| Hero | Conversion Surface |
| Button | Action |
| Card | Information Surface |
| Section | Content Region |
| Form | Data Collection Pattern |
| Accordion | Progressive Disclosure |
