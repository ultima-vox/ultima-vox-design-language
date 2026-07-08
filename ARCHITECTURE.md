# Architecture

**Status:** Draft  
**Version:** 0.1.0 Foundation  
**Last Updated:** 2026-07-09  

## Purpose

This document defines the high-level architecture of UVDL.

## Architectural Model

```text
Human
  ↓
Intent
  ↓
Decision
  ↓
Interaction
  ↓
Pattern
  ↓
Component
  ↓
Implementation
```

## Repository Layers

### Core
Stable UVDL specification.

Contains accepted terminology, rules, tokens, component contracts, patterns, and templates.

### Lab
Research space for unvalidated concepts.

Contains ideas such as Design DNA, Design Physics, Intent Engine, and Compiler.

### Experiments
Validation layer.

Contains project-specific experiments and results.

### Knowledge
Validated design knowledge.

Contains conclusions that have evidence but may not yet be formal Core standards.

### Packages
Implementation layer.

Future packages may include tokens, CSS, CLI, HostCMS integration, and reference components.

### Examples
Reference implementations.

`mechaniki.ru` is the first planned example.

## Promotion Path

```text
Lab
  ↓
Experiment
  ↓
Knowledge
  ↓
Core
  ↓
Packages
  ↓
Examples
```

## Stability Rule

Core must remain practical and stable.

Lab may be speculative.

Knowledge must be evidence-based.

Packages must implement Core, not Lab.

## Non-Goal

UVDL does not attempt to replace designers, developers, or researchers.

It exists to improve the quality and repeatability of their decisions.
