# UVDL Manifesto

**Status:** Draft  
**Version:** 0.4.0 Architecture  
**Last Updated:** 2026-07-09  

## Manifesto

Design is not decoration.

Design is communication.

Every interface exists to help a human make a decision.

Every pixel must have a purpose.

Every interaction must have intention.

Every component must solve a problem.

Everything unnecessary should be removed.

Performance is a feature.

Accessibility is mandatory.

Consistency creates trust.

Trust creates conversion.

## Core Belief

UVDL does not start with components.

It starts with human intent, decision-making, trust, interaction, and validation.

A design language is not a component library.

It is a language for describing interfaces.

## Language Architecture

UVDL is organized as a language:

```text
Foundation
  ↓
Elements
  ↓
Patterns
  ↓
Templates
  ↓
Pages
```

### Foundation

Foundation is the alphabet of the interface.

It defines the base material:

- fonts;
- tokens;
- base HTML behavior;
- typography;
- layout.

### Elements

Elements are the words of the interface.

They are universal building blocks with one clear role:

- Action;
- Brand;
- Surface;
- Navigation;
- Field;
- Media;
- Notice;
- Status;
- Dialog;
- Disclosure.

Elements must not contain business-domain meaning.

### Patterns

Patterns are the sentences of the interface.

They combine Elements to solve repeated user problems:

- Header;
- Footer;
- Hero;
- FAQ;
- Catalog;
- Pricing;
- Contact.

Patterns may describe common product structures, but Core must still avoid project-specific business logic.

## Principles

### Intent First

Start with what the human is trying to do.

Do not start with visual decoration.

### Semantics over Appearance

Names should describe purpose before appearance.

`Action` is stronger than `Button`.

`Surface` is stronger than `Card`.

`Navigation` is stronger than `Menu`.

### Composition over Specialization

Prefer reusable Elements combined into Patterns over many narrow business components.

### Universal before Business

Core defines universal interface language.

Projects define domain-specific meaning.

### Accessibility by Default

Accessible behavior is not an enhancement.

It is part of the component contract.

### Mobile First

The smallest useful viewport must be considered first.

### Readability First

Code should be understandable before it is clever.

### Progressive Enhancement

Interfaces should remain usable when advanced behavior fails.

### The Simplest Correct Solution Wins

If something can be written manually in 10 minutes, do not automate it yet.

Automation appears after repeated practical pain.

## Engineering Principle

A design decision is not accepted because it looks good.

A design decision is accepted when it solves a problem, reduces friction, improves clarity, or has been validated in practice.

## Core Rule

If a concept cannot be explained simply, it does not belong in UVDL Core.
