# Traceability

**Type:** traceability
**Status:** accepted
**Source Issues:** #1 #4 #14 #21 #26

DDD is a graph, not a folder hierarchy.

## Canonical flow

`Vision → Goal → PRD → Requirement → Issue → Research/Experiment → Evidence → RFC → ADR → Design → PR → Code → Test → Release → Feedback → Issue`

## Typed relations

| Relation | Meaning |
|---|---|
| raises | creates an unresolved question |
| refines | makes a concept more precise |
| derives | produces knowledge from a source |
| proposes | suggests an answer |
| decides | adopts a decision |
| implements | realizes knowledge in change |
| verifies | supplies verification |
| supersedes | replaces an older knowledge artifact |
| depends_on | requires another artifact |
| generates | produces a downstream artifact |

The same Issue may relate to multiple Documents, and a Document may resolve multiple Issues.
