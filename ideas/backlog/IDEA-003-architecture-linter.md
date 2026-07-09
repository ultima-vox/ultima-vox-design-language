# IDEA-003 — Architecture Linter

**Status:** Backlog  
**Priority:** Medium  
**Created:** 2026-07-09  
**Related:** ADR-006, ADR-008, packages/css/README.md  

## Problem

As UVDL grows, CSS files may accidentally violate the intended one-way dependency model.

Examples:

- Foundation importing Elements.
- Elements importing Patterns.
- Patterns importing other unrelated Patterns.
- Circular imports.
- Business-domain naming leaking into Core.

## Proposal

Create a small architecture linter that validates repository rules.

Possible checks:

- `foundation/*` must not import Elements or Patterns.
- `elements/*` may import Foundation only.
- `patterns/*` may import Foundation and Elements.
- no circular imports.
- no business-domain class names in Core.
- no Pattern introducing new Element-like concepts without ADR approval.

## Benefits

- Keeps architecture stable as the system grows.
- Prevents accidental dependency drift.
- Makes architectural rules enforceable, not just documented.
- Helps future contributors work safely.

## Risks

- Could become over-engineered too early.
- May slow down experimentation.
- Requires maintenance as architecture evolves.

## Dependencies

- Core Elements stable.
- First Patterns stable.
- Dependency rules documented.

## Notes

Do not implement during Core and initial Patterns work.

Capture only. Review after Patterns MVP and Handbook draft.
