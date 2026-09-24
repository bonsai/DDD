# PRD

**Product Requirements Document** — a document that defines what product should be built and the requirements it must satisfy.

## Purpose

PRD answers:

> What are we building?

## Structure

```yaml
id: PRD-001
product: product name
problem: problem to solve
users:
  - target user
value: expected user value
requirements:
  - id: REQ-001
    statement: requirement
    priority: must
constraints:
  - product constraint
success_criteria:
  - criterion
mvp: MVP-001
kpi:
  - KPI-001
open_questions:
  - issue
traceability:
  - related issue / decision / design
```

## Rules

- Define WHAT, not implementation details.
- Describe users, problem, value, requirements, constraints, and observable acceptance criteria.
- Keep technical solution choices in design documents or ADRs.
- Define boundaries so MVP scope can be derived.
- Do not silently resolve uncertainty; unresolved questions belong in Issues.
- Material changes should create or reference an Issue and record what changed and why.

## Relationship

```text
VISION → PRD → MVP → DESIGN → BUILD
             ↓
       requirements / issues
             ↓
       research / ADR
```
