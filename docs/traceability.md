# Traceability

DDD is a graph, not a pile of documents.

## Minimum graph

```text
PRD
 ↓
Requirement
 ↓
Issue
 ↓
Evidence / Research
 ↓
Decision
 ↓
ADR
 ↓
Design
 ↓
PR / Change
 ↓
Test
 ↓
Release
 ↓
Feedback
 ↺
Issue
```

## Required links

| From | To | Relation |
|---|---|---|
| Requirement | Issue | refines / raises |
| Issue | Research | investigated_by |
| Issue | ADR | resolved_by |
| ADR | Design | constrains |
| Design | PR | implemented_by |
| PR / Change | Test | verified_by |
| Test | Requirement | verifies |
| Release | Change | contains |
| Feedback | Issue | raises |

## Traceability levels

### Level 0 — local
A document is understandable by itself.

### Level 1 — issue-linked
A document points to the Issue that caused or motivated it.

### Level 2 — decision-linked
Implementation can be traced through Design/ADR to the originating requirement or Issue.

### Level 3 — evidence-linked
Claims and decisions point to research, experiments, tests, or operational evidence.

DDD aims for Level 2 by default and Level 3 for consequential decisions.

## Change impact

When changing a Requirement or ADR, inspect downstream links:

```text
changed node
 → dependent documents
 → affected issues
 → designs
 → code changes
 → tests
 → release / operations
```

The graph makes impact analysis explicit and gives AI agents a safe navigation path.

## Orphan detection

Useful automated checks include:

- closed Issue without a resolution
- ADR without an originating Issue/Requirement when one should exist
- Requirement without acceptance criteria
- PR without a related Issue for non-trivial changes
- Test without a requirement or behavior under test
- superseded Document still marked active
- document linking to a missing artifact

These are quality signals, not absolute laws. Exceptions should be explainable.
