# AI Agent Operating Model

**Type:** operating-model
**Status:** accepted
**Source Issues:** #5 #7 #24 #25

AI agents should operate on explicit knowledge states rather than treating the conversation as permanent memory.

## Agent loop

1. Read Issue.
2. Retrieve related Documents and Evidence.
3. Identify uncertainty and missing evidence.
4. Produce Research / RFC as appropriate.
5. Never treat a proposal as an adopted decision.
6. Use accepted ADR/Spec/Design to implement a Change.
7. Run Tests and attach Evidence.
8. Report Feedback and generate/update Issues.

## Guardrail

The agent must distinguish `proposed`, `accepted`, and `verified`. It should not invent decisions, silently resolve ambiguity, or overwrite historical knowledge.
