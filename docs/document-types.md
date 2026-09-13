# Document Types

DDD uses documents according to the question they answer.

| Type | Answers | Main output |
|---|---|---|
| Vision | Why does this exist? | Direction |
| Principles | What rules should guide us? | Constraints |
| Strategy | Where are we going and how? | Priorities |
| Glossary | What do terms mean? | Shared vocabulary |
| PRD | What product should exist and why? | Product scope |
| Requirement / Spec | What must be true or observable? | Verifiable conditions |
| Use Case | How does an actor achieve a goal? | Interaction flow |
| RFC | Which proposal should we adopt? | Candidate solutions |
| ADR | What did we decide and why? | Decision record |
| Architecture | What are the major system structures? | System design |
| Design | How will a component work? | Detailed design |
| API / Data Contract | What interface/data shape is stable? | Contract |
| Research Note | What did we learn? | Evidence and findings |
| Experiment Report | What happened when we tested an assumption? | Results |
| Test Plan | How will we verify it? | Verification strategy |
| Runbook | How is it operated? | Operational procedure |
| Security / Threat Model | What can go wrong and how do we mitigate it? | Risk controls |
| Release Notes | What changed for users/operators? | Change communication |
| Postmortem | What happened and what should change? | Corrective knowledge |
| Retrospective | What did the team learn? | Process improvement |

## Document selection rule

Use the smallest document that permanently answers the question.

- Unknown → Issue
- Investigation → Research / Experiment
- Candidate solution → RFC
- Chosen solution → ADR
- Required behavior → Requirement / Spec
- Structure → Architecture / Design
- Verification → Test Plan / Evidence
- Operation → Runbook
- Learning after an event → Postmortem / Retrospective

A document should not exist merely because the template exists. Create it when the knowledge is worth preserving or sharing.
