# Founding Decisions

**Status:** Draft  
**Version:** 0.1.0 Foundation  
**Last Updated:** 2026-07-09  

## FD-001 — UVDL is a Design Language, not only a Design System

UVDL is created as a language of decisions, not as a list of UI components.

Components are implementation details. The language starts with intent, meaning, decision, interaction, and validation.

## FD-002 — Decisions before Components

The project motto is:

> Decisions before Components.

A component must not exist only because it is common in other systems. It must exist because it supports a user intent or solves a repeatable design problem.

## FD-003 — Core and Lab are separate

UVDL separates stable and experimental work.

- `core/` contains stable specifications.
- `lab/` contains research concepts and hypotheses.
- `experiments/` contains validation attempts.
- `knowledge/` contains validated knowledge.

Ideas move through:

`Lab → Experiment → Knowledge → Core`

## FD-004 — Everything starts as Draft

Every idea, term, pattern, rule, token, component, or implementation starts as Draft.

Nothing becomes accepted without review.

## FD-005 — Foundation before Tokens

No production tokens, components, or CSS are introduced before Foundation is defined.

The system must first answer:

- why it exists;
- how it evolves;
- how decisions are made;
- how knowledge is validated;
- what terminology it uses.

## FD-006 — mechaniki.ru is the first reference project

The first practical validation target is `mechaniki.ru`.

Solutions proven there may later move from project-specific implementation into UVDL Knowledge or Core.
