# Issue ↔ Document Flow

DDD treats development as a knowledge lifecycle.

## Canonical flow

```text
Vision
  ↓
PRD
  ↓
Requirement
  ↓
Issue
  ↓
Research / Experiment
  ↓
RFC
  ↓
Decision
  ↓
ADR
  ↓
Architecture / Design
  ↓
Task / PR
  ↓
Code
  ↓
Test
  ↓
Release
  ↓
Feedback
  ↓
Issue
```

Not every change needs every stage. The flow is a vocabulary, not bureaucracy.

## Issue states

An Issue can represent:

- question / uncertainty
- bug
- requirement gap
- change request
- task
- risk
- research request
- decision request
- documentation gap
- improvement

## Resolution patterns

### Question
`Issue → Research → Decision → ADR → Close`

### Implementation
`Issue → Requirement → Design → PR → Test → Close`

### Bug
`Issue → Evidence → Root cause → Fix → Test → Close`

### Product change
`Feedback → Issue → PRD/Requirement update → Design → PR → Release`

## Closing rule

An Issue is not closed because someone stopped working on it. It is closed when its question, change, or obligation has an explicit resolution or an explicit decision not to act.

## Document generation rule

Create a durable Document when an Issue produces knowledge that is likely to be reused, reviewed, or needed to understand a future change.

Examples:

- one-off task → Issue may be enough
- reusable product definition → PRD
- repeated architectural question → ADR
- investigation with reusable findings → Research Note
- proposal requiring review → RFC

## AI-agent rule

An AI agent should:

1. read the relevant Issue and linked Documents;
2. identify missing context;
3. create or request an Issue when uncertainty is material;
4. update the appropriate Document when a durable conclusion is reached;
5. implement only after the applicable requirements and decisions are sufficiently clear;
6. leave traceability from implementation back to the originating question.
