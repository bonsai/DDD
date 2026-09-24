# ADR

**Architecture Decision Record** — a short record of an important technical or architectural decision and the reasons behind it.

## Purpose

ADR answers:

> Why did we choose this approach?

## Structure

```yaml
id: ADR-001
title: decision title
status: proposed | accepted | superseded | rejected | deprecated
context: context and problem
options:
  - option
decision: chosen decision
alternatives:
  - option
rationale: why the decision was chosen
consequences:
  positive:
    - consequence
  negative:
    - consequence
references:
  - related document
traceability:
  related_issues: []
  derived_from: []
  implements: []
  verified_by: []
  supersedes: null
  superseded_by: null
```

## Rules

- Record decisions that are important enough to affect future implementation or maintenance.
- Explain context and alternatives, not only the final choice.
- Keep ADR focused on WHY; detailed implementation belongs in design/spec documents.
- Do not rewrite history when a decision changes; supersede the old ADR with a new one.
- Rejected alternatives should remain visible when they explain the choice.

## Relationship

```text
POC / RESEARCH → ADR → DESIGN → BUILD
                         ↑
                    implementation
                     rationale
```
