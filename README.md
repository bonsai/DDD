# Document Driven Development (DDD)

> Issueで問いを立て、Documentで知識と判断を固定し、Codeで実行し、TestとFeedbackで次のIssueを生む。

## Definition

**Document Driven Development (DDD)** is a development method in which humans and AI discover unresolved questions through Issues, stabilize shared knowledge and decisions through Documents, execute them through Code, and generate new Issues through Tests and Feedback.

```text
Vision
  ↓
Goal
  ↓
PRD / Requirement
  ↓
Issue（問い）
  ↓
Research / Experiment
  ↓
Decision
  ↓
ADR
  ↓
Design
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

## Core principles

1. **Issue is a question.** It represents uncertainty, work, risk, or a requested change.
2. **Document is stabilized knowledge.** A document records a reusable understanding, requirement, proposal, decision, design, or evidence.
3. **ADR records decisions.** It answers what was chosen and why, not merely what was implemented.
4. **Code is executable knowledge.** Implementation should be traceable to requirements and decisions.
5. **Test is evidence.** A test verifies whether an expected behavior or property is actually satisfied.
6. **Traceability is bidirectional.** Documents create Issues; Issues update Documents.
7. **AI should navigate the graph, not invent missing history.** When evidence or a decision is absent, the agent should surface an Issue rather than silently filling the gap.

## Document families

- Vision / Principles / Strategy
- PRD / Requirements / Use Cases / User Stories
- RFC / Proposal
- ADR / Decision Record
- Architecture / Design / API / Data Model
- Research / Experiment / Evidence
- Test Plan / Verification
- Runbook / Operations / Security
- Release Notes / Postmortem / Retrospective
- Ontology / Glossary

## Issue ↔ Document

| Situation | Primary object |
|---|---|
| Something is unknown or unresolved | Issue |
| Product intent and scope | PRD |
| Observable required behavior | Requirement / Spec |
| Several solutions are being compared | RFC |
| A choice has been made | ADR |
| Implementation structure is being described | Design |
| An assumption is being investigated | Research / Experiment |
| A claim has been verified | Test / Evidence |
| A change is proposed in code | PR |
| A released change is communicated | Release Note |

See `docs/issue-document-flow.md` for the lifecycle and `docs/traceability.md` for the graph model.

## Status

This repository is the canonical specification for DDD itself. It is intentionally document-first: the method is defined before tooling is built.
