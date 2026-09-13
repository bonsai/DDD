# PRD Template

> PRD defines product intent, value, scope, and verifiable outcomes. It does not prescribe implementation details.

## 1. Problem

What problem exists? For whom? What evidence shows that it matters?

## 2. Target

Who is the primary user or actor?

## 3. Goal

What measurable or observable outcome should this product create?

## 4. Non-goals

What is explicitly outside this PRD?

## 5. User stories

```text
As a <user>,
I want <capability>,
so that <value>.
```

## 6. Requirements

Each requirement should be uniquely identifiable and testable.

```yaml
- id: REQ-001
  statement: ...
  priority: must
  related_issues: []
```

## 7. Acceptance criteria

Define observable conditions for considering the requirement satisfied.

## 8. Constraints

Business, technical, legal, budget, time, compatibility, or operational constraints.

## 9. Dependencies

External systems, decisions, documents, or teams required for delivery.

## 10. Risks

Known risks and their relationship to Issues.

## 11. Open questions

Do not silently resolve uncertainty. Link unresolved questions to Issues.

## 12. Traceability

```text
PRD → Requirement → Issue → Research/RFC → ADR → Design → Change → Test
```

## 13. Change policy

A PRD may evolve. Material changes should create or reference an Issue and record what changed and why. Implementation details belong in Design/ADR documents rather than being hidden inside the PRD.
