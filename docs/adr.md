# ADR Template

> ADR (Architecture Decision Record) records a durable decision and its rationale.

## Status

`proposed` / `accepted` / `rejected` / `deprecated` / `superseded`

## Context

What situation, constraint, problem, or Issue required a decision?

## Decision

State the chosen option clearly and unambiguously.

## Alternatives

List the meaningful alternatives considered.

| Option | Advantages | Disadvantages | Reason |
|---|---|---|---|
| A | ... | ... | ... |
| B | ... | ... | ... |

## Rationale

Why was this decision selected? Reference evidence, requirements, experiments, or principles.

## Consequences

### Positive

- ...

### Negative / Trade-offs

- ...

### Follow-up

- ...

## Traceability

```yaml
related_issues: []
derived_from: []
implements: []
verified_by: []
supersedes: null
superseded_by: null
```

## Rules

1. ADR records a **decision**, not a task list.
2. The decision must be understandable without reading the implementation.
3. Reversibility should be stated when relevant.
4. Rejected alternatives should remain visible when they explain the choice.
5. A changed decision should create a new ADR that supersedes the old one; do not rewrite history to erase the old rationale.
