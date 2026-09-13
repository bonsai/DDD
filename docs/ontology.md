# DDD Ontology

## 1. Core entities

| Entity | Meaning |
|---|---|
| Issue | 未確定事項、問い、作業、リスク、変更要求 |
| Document | 人間とAIが共有する固定化された知識 |
| Requirement | 満たすべき条件・振る舞い |
| Decision | 選択された判断 |
| Artifact | Code, Design, Test, Releaseなどの成果物 |
| Evidence | 判断や検証を支える観測・資料 |
| Feedback | 利用後に得られた反応・観測 |
| Change | システムまたは文書への変更 |

## 2. Core relations

```text
Issue
 ├─ raises ───────→ Issue
 ├─ refines ──────→ Requirement / Document
 ├─ resolves ─────→ Issue
 └─ depends_on ───→ Issue

Document
 ├─ derives_from ─→ Document / Evidence
 ├─ addresses ────→ Issue
 ├─ supersedes ───→ Document
 └─ constrains ───→ Change

Decision
 ├─ answers ──────→ Issue
 ├─ justifies ────→ Design / Change
 └─ supersedes ───→ Decision

Change
 ├─ implements ───→ Requirement / Decision
 ├─ verifies ─────→ Test
 └─ produces ─────→ Feedback
```

## 3. Important distinction

**Document type** and **Issue type** are different dimensions.

- `research` may be an Issue asking for investigation.
- `research-note` is the resulting Document.
- `decision` may be an Issue asking what to choose.
- `ADR` is the durable record of the chosen Decision.

Do not encode workflow state as document type.

## 4. Minimal metadata

```yaml
id: DDD-0001
type: adr
status: accepted
title: Example decision
created: 2026-09-13
updated: 2026-09-13
related_issues:
  - DDD-12
derived_from:
  - docs/research/example.md
supersedes: null
```

## 5. Graph invariant

Every significant implementation decision should be reachable from at least one Issue, Requirement, or explicit project principle. Every closed Issue should point to its resolution: Document, Change, PR, Test, or explicit rejection.
