# DDD Lifecycle

## 0. Frame

Define Vision, Principles, and PRD. Identify goals, scope, and constraints.

## 1. Discover

Create Issues for uncertainty, missing requirements, risks, bugs, or requested changes.

## 2. Investigate

Use Research Notes, Experiments, prototypes, benchmarks, and Evidence to reduce uncertainty.

## 3. Propose

Use an RFC when multiple meaningful solutions need comparison or review.

## 4. Decide

Record durable choices in an ADR. Rejected alternatives and rationale remain visible.

## 5. Design

Translate requirements and decisions into Architecture, Design, API, Data, UX, Security, or other implementation specifications as needed.

## 6. Implement

Create Tasks and PRs. Code should reference the Issue and applicable Requirement/ADR.

## 7. Verify

Use automated/manual Tests and Evidence to verify acceptance criteria and important invariants.

## 8. Release

Ship the change and record user/operator-facing effects.

## 9. Learn

Capture Feedback, incidents, Postmortems, and Retrospectives. Turn meaningful discoveries into new Issues or updated Documents.

## State transition principle

```text
uncertainty → investigation → decision → implementation → evidence → learning
```

The lifecycle is cyclic. A release does not end knowledge work; it creates new evidence.

## AI operating rule

At each stage, the agent should prefer:

1. existing authoritative Documents;
2. linked Issues and evidence;
3. explicit new Issues for missing information;
4. a new Document only when the result is durable knowledge;
5. implementation after the necessary decisions are explicit.

This prevents an agent from filling gaps with plausible but unrecorded assumptions.
