# UVDL-013 — Decision Model Specification

**Status:** Draft  
**Version:** 0.2.0 Ontology  
**Last Updated:** 2026-07-09  
**Depends on:** UVDL-010, UVDL-011, UVDL-012  

## Purpose

Define how UVDL models user decisions.

## Scope

This specification covers the conceptual decision model used to evaluate patterns and components.

## Non-Goals

This specification does not define behavioral analytics implementation or exact UX research methodology.

## Definitions

A Decision is a moment where a Human chooses what to do next.

Decision Cost is the perceived effort, uncertainty, or risk required to make that choice.

## Specification

A UVDL interface SHOULD reduce Decision Cost.

A Decision may be affected by:

- clarity;
- trust;
- evidence;
- cognitive load;
- interaction cost;
- perceived risk;
- time pressure;
- accessibility barriers.

## Decision Support Model

A Decision SHOULD be supported by at least one of the following:

1. Orientation — help the Human understand where they are.
2. Evidence — support claims with proof.
3. Action — provide a clear next step.
4. Feedback — show the result or state of interaction.
5. Reduction — remove unnecessary choices or friction.

## Primary Action Rule

A decision context SHOULD have one Primary Action.

Multiple competing Primary Actions increase Decision Cost and SHOULD be avoided.

## Evidence Rule

If a decision involves risk, UVDL SHOULD provide Evidence before or near the Action.

## Rationale

UVDL treats design as decision support.

A pattern is useful only if it helps a Human make a better or faster decision.

## Examples

### Service Booking

```text
Intent: book repair
Decision: contact service or leave
Decision Cost: medium/high
Support: Trust Region + Price Signal + Primary Action
```

### Service Selection

```text
Intent: choose service
Decision: select relevant repair category
Decision Cost: medium
Support: Service Selection Pattern + clear grouping + search/filter if needed
```

## References

- `TERMINOLOGY.md`
- `KNOWLEDGE_MODEL.md`

## Revision History

| Version | Date | Changes |
|---|---|---|
| 0.2.0 | 2026-07-09 | Initial decision model specification |
