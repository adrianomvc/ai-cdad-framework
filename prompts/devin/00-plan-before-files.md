# Prompt 00 — Plan Before Files

You are going to help me implement an enterprise delivery framework called AI-CDAD — AI Context-Driven Adaptive Delivery.

Before changing files, read and understand this mission:

AI-CDAD must support Greenfield, Brownfield, Hybrid, Bugs, Incidents, Hotfixes, Engineering work, and Compliance / Security remediation.

AI-CDAD integrates with AWS AI-DLC workflows as the execution engine.

Important:
The PM Agent already exists outside this framework and is called Product Discovery Agent.
It runs in Microsoft Teams and is responsible for product discovery, inception, story creation, acceptance criteria and prioritization.

Do not implement the PM Agent.

Core philosophy:
- AI-CDAD governs
- AI-DLC executes
- Devin acts as a guided orchestrator
- humans retain ownership
- AI accelerates

Before creating files, produce an implementation plan with:
1. repository structure
2. files to create
3. assumptions
4. questions only if truly blocking
5. risks
6. token minimization strategy
7. brownfield safety strategy
8. how AWS AI-DLC will be integrated
9. how Devin will behave as guided orchestrator

Do not create files yet.


---

## Source of Truth Rule

README.md is the source of truth for the framework.

If any file conflicts with README.md, architecture/source-of-truth.md or docs/notes/decisions-log.md, follow this priority:

1. README.md
2. architecture/source-of-truth.md
3. docs/notes/decisions-log.md
4. policies/
5. playbooks/
6. templates/
7. examples/

Do not contradict the source of truth.
