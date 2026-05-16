# CDAD v1 - Devin Implementation Prompt

(Arquivo gerado a partir da definição do framework CDAD)

Cole TODO o conteúdo abaixo no Devin.

====================================================================

# Mission

You are helping implement an enterprise delivery framework called:

# CDAD — Context-Driven Adaptive Delivery

This framework is designed to support:

- Greenfield delivery
- Brownfield evolution
- Hybrid delivery
- Bugs
- Incidents
- Hotfixes
- Engineering work
- Compliance / security remediation

The framework must integrate with AWS AI-DLC workflows as the execution engine:

https://github.com/awslabs/aidlc-workflows

Important:

The PM Agent already exists outside this framework.

The PM Agent is external, runs in Microsoft Teams, and is responsible for:

- Product discovery
- Requirement elicitation
- Inception
- Story creation
- Acceptance criteria
- Prioritization

Do not implement the PM Agent.

CDAD starts after a demand enters the framework, whether it came from the PM Agent or from another entry lane such as bug, incident, tech debt, or compliance.

# Core Philosophy

CDAD governs.
AI-DLC executes.
Devin acts as a guided orchestrator.
Humans retain ownership.
AI accelerates.

# Human Role Boundaries

## PM
Defines:
- WHAT
- WHY
- VALUE
- PRIORITY

## Tech Lead
Owns:
- architectural direction
- technical strategy
- risk acceptance
- contract strategy
- migration strategy
- rollout strategy

## Developer
Owns:
- technical execution
- implementation refinement
- edge cases
- test refinement
- PR readiness
- execution feasibility
- code quality

Developer is an AI-Augmented Engineer, not a prompt operator.

## AI / Devin
Accelerates:
- context organization
- artifact drafting
- shaping
- implementation
- testing
- validation
- documentation

AI does not own decisions.

# Required repository structure

cdad-framework/
repo-central-da-sigla/
repo-da-aplicacao/

# Required framework folders

architecture/
playbooks/
policies/
templates/
agent-roles/
prompts/
examples/

# Entry Lanes
- Product
- Operational
- Engineering
- Compliance

# Risk Modes
- FAST
- HYBRID
- SAFE

Rules:
FAST -> low risk
HYBRID -> controlled integration
SAFE -> brownfield critical / contract / production / PII / uncertainty

If uncertainty exists:
FAST → HYBRID → SAFE

# Required policies
Create:
- delivery-routing-policy.md
- governance-policy.md
- failure-handling-policy.md
- context-lifecycle-policy.md
- context-budget-policy.md
- context-minimization-policy.md
- mcp-consumption-policy.md
- human-approval-policy.md
- artifact-ownership-policy.md
- parallel-initiatives-policy.md
- parallel-execution-policy.md
- validation-policy.md
- deployment-policy.md
- definition-of-ready-policy.md
- definition-of-done-policy.md

# Required templates
Create all templates for:
intake
design
execution
governance
indexes

Including:
- runtime-context-template.md
- relevant-files-list-template.md
- context-reduction-plan-template.md
- parallel-execution-plan-template.md

# Core runtime principles
Repositories store rich memory.
Devin session uses minimal runtime context.

Never remove:
- risk mode
- scope
- out of scope
- hard stops
- required gates
- stop conditions
- human owner
- validation requirements
- evidence references

# Token budgets
FAST:
Target 20k
Max 40k

HYBRID:
Target 50k
Max 100k

SAFE:
Target 100k
Max 180k

# Parallel execution
Implement governed parallel execution with:
- workstream-organizer
- parallel-execution-plan.md

# Hard stops
Must stop for:
- production
- contract/schema changes
- PII
- IAM/security
- destructive operations
- low confidence
- SAFE without approvals

# Status format
Always output:

## CDAD Status Update
Current Stage
Created/Updated Artifacts
Human Action Required
Blocking Issues
Next Step
Confidence

# Output expectation
Populate files with useful content.
No empty placeholders.
Enterprise-ready.
Lightweight enough for adoption.
Ready for tabletop testing.

====================================================================

SECOND REVIEW PROMPT

Review the generated CDAD framework and check for:

1. Missing policies
2. Duplicated concepts
3. Overly heavy process
4. Token bloat risks
5. Ambiguous human ownership
6. Unsafe brownfield assumptions
7. Missing references to AWS AI-DLC
8. Missing distinction between central hub and application repository
9. Missing FAST/HYBRID/SAFE differences
10. Missing Devin stop conditions

Return a prioritized list of corrections before changing files.
