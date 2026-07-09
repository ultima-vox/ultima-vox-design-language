# RFC-001 — Future UVDL Site Builder

**Status:** Draft  
**Created:** 2026-07-09  
**Related:** ADR-003, UVDL-010, UVDL-014  

## Problem

If UVDL becomes a reusable design language, the same patterns, components, and templates will likely repeat across multiple projects.

Manually assembling every site from scratch may become inefficient after several reference implementations.

## Hypothesis

In the future, UVDL can become the foundation for a site builder that assembles websites from validated patterns, components, templates, and project-specific content.

The builder should not be part of the MVP.

## Proposal

Treat a future site builder as a long-term Lab direction.

The possible future flow:

```text
Project brief
  ↓
Business type
  ↓
User intents
  ↓
UVDL patterns
  ↓
Page templates
  ↓
Components
  ↓
HTML/CSS/HostCMS output
```

## MVP Boundary

The current MVP remains simple:

```text
Manual CSS tokens
  ↓
Manual components
  ↓
Manual patterns
  ↓
mechaniki.ru reference implementation
```

No builder, compiler, schema generator, or visual editor is added before repeated practical need is proven.

## Possible Future Capabilities

- Generate page structure from business type and intents.
- Select patterns based on conversion goals.
- Assemble static HTML/CSS.
- Export HostCMS-compatible templates.
- Validate pages against UVDL rules.
- Suggest missing trust, CTA, FAQ, or contact regions.
- Produce project-specific theme files.

## Risks

- Premature complexity.
- Lock-in to an immature model.
- Poor generated output if patterns are not validated.
- Distraction from practical reference implementations.

## Validation Plan

Before building a site builder, UVDL must be used in at least several real projects.

Initial validation candidates:

1. mechaniki.ru
2. Zelseptik
3. Auto Prestige

## Success Metrics

The builder idea may move forward only if it can show:

- faster site assembly;
- fewer repeated layout decisions;
- lower rework;
- consistent UX quality;
- maintainable generated code;
- compatibility with HostCMS workflows.

## Decision

Draft only.

This RFC captures the future direction but does not change the current MVP roadmap.
