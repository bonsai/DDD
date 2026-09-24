# POC

**Proof of Concept** — a small experiment used to validate whether a technical or methodological approach works under defined conditions.

## Purpose

POC answers:

> Can this approach work?

## Structure

```yaml
id: POC-001
question: hypothesis to validate
approach: approach under test
constraints:
  - constraint
experiment: experiment description
result: observed result
conclusion: validated | rejected | inconclusive
next_action: next step
```

## Rules

- Start from a concrete uncertainty or hypothesis.
- Keep the experiment smaller than the final implementation.
- Record observed evidence, not only expectations.
- Separate technical feasibility from product desirability.

## Relationship

```text
PRD → uncertainty → POC → evidence → DESIGN / ADR → BUILD
```
