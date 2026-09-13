# GitHub Semantics

**Type:** integration
**Status:** accepted
**Source Issues:** #11 #24 #25

GitHub objects can be interpreted as knowledge transformations.

| GitHub object | DDD role |
|---|---|
| Issue | unresolved question / uncertainty |
| PR | proposed implementation answer |
| Review | verification of the answer |
| Merge | adoption of the change |
| Commit | historical change record |
| Release | delivered change |

Chat is a workspace/input, not the canonical source of truth. Important knowledge must be promoted into Issues, Documents, ADRs, Code, or Evidence.
