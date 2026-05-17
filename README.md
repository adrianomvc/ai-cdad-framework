# AI-CDAD — AI Context-Driven Adaptive Delivery

> **AI-CDAD governs. AI-DLC structures the lifecycle. AI Execution Agents execute under guidance. Humans retain ownership.**

**AI-CDAD** is a tool-agnostic delivery framework for teams that want to use AI agents safely, effectively and repeatably across software, data and platform delivery.

It is designed for organizations that need speed **without losing engineering discipline, governance, traceability and human accountability**.

---

## What is AI-CDAD?

**AI-CDAD — AI Context-Driven Adaptive Delivery** is an operating model for AI-augmented delivery.

It defines how work should move from request to execution using:

- structured context
- adaptive risk classification
- human-in-the-loop gates
- role-specific playbooks
- reusable policies
- execution briefs
- validation evidence
- repository-based memory
- AI-agent adapters

AI-CDAD is not a coding agent.

AI-CDAD is not a replacement for Product, Tech Lead or Developer judgment.

It is a framework that tells AI agents **how to operate safely**.

---

## Why this framework exists

AI-assisted delivery often fails when AI starts coding without enough context.

Common problems:

- AI changes code without understanding business impact.
- Brownfield work is treated like greenfield work.
- Developers become prompt operators instead of technical owners.
- Tech Leads become bottlenecks reviewing everything.
- Context becomes too large and consumes too many tokens.
- Decisions are lost in chats, PR comments or meeting notes.
- Multiple initiatives change the same repo without coordination.
- Risks around production, contracts, PII, IAM, rollback and compliance are discovered too late.

AI-CDAD addresses these problems by introducing:

- **Entry Lanes** — where the demand comes from
- **Risk Modes** — how much governance is needed
- **Runtime Context** — the minimum safe context for execution
- **Human Gates** — when humans must validate or approve
- **Policies** — non-negotiable rules for safety and consistency
- **Playbooks** — role-specific operating guidance
- **Adapters** — tool-specific guidance for different AI agents
- **Evidence** — traceability for decisions, validation and delivery

---

## Who is this for?

AI-CDAD is useful for:

- engineering teams using AI coding agents
- data engineering teams
- platform teams
- product engineering squads
- enterprise architecture groups
- technology governance teams
- teams adopting Devin, Claude Code, Codex, Cursor, Copilot or internal agents
- organizations moving from ad hoc AI usage to governed AI-assisted delivery

---

## Core positioning

```text
AI-CDAD = governance and operating model
AI-DLC = delivery lifecycle structure
AI Execution Agent = implementation accelerator
Humans = accountability and decision owners
```

---

## Core principles

1. **Context before code**  
   AI must understand enough context before execution.

2. **AI drafts, humans own**  
   AI creates artifacts and suggestions. Humans validate critical decisions.

3. **Risk-adaptive delivery**  
   Low-risk work should move fast. Critical brownfield work should be safe.

4. **Minimal runtime context**  
   Repositories store rich memory. AI sessions load only what is needed.

5. **Evidence-based trust**  
   Runtime summaries must reference evidence, not unsupported assumptions.

6. **Safe default**  
   If relevant uncertainty exists, increase rigor: `FAST → HYBRID → SAFE`.

7. **Tool-agnostic execution**  
   AI-CDAD can work with Devin, Claude Code, Codex, Cursor, Copilot, Amazon Q, StackSpot AI, ResolveAI or internal agents.

8. **Human accountability**  
   AI does not approve risk, own delivery decisions or bypass gates.

---

## Relationship with AWS AI-DLC

AI-CDAD can be integrated with **AWS AI-DLC** as the delivery lifecycle structure.

AI-CDAD defines:

- how a demand enters the flow
- how risk is classified
- which playbooks apply
- which artifacts are required
- which humans must approve
- which context is loaded
- when an AI agent must stop

AI-DLC supports execution phases such as:

- Discover
- Design
- Build
- Test
- Deploy
- Observe

In short:

```text
AI-CDAD governs.
AI-DLC structures the lifecycle.
AI Execution Agents execute under guidance.
```

---

## AI Execution Agent model

AI-CDAD is not tied to a single AI tool.

Supported execution agents may include:

- Devin
- Claude Code
- Codex
- Cursor
- GitHub Copilot
- Amazon Q Developer
- StackSpot AI
- ResolveAI
- internal agents

The generic execution artifact is:

```text
ai-execution-brief.md
```

For Devin compatibility, the same contract may be named:

```text
devin-execution-brief.md
```

Every AI Execution Agent must:

1. read `runtime-context.md`
2. read `ai-execution-brief.md`
3. respect scope and out of scope
4. follow the applicable playbook
5. obey hard stops
6. ask for minimum missing context when blocked
7. generate validation evidence
8. produce AI-CDAD Status Updates
9. never approve its own work
10. never accept risk on behalf of humans

---

## PM Agent boundary

The Product/PM discovery layer is external to AI-CDAD.

In this framework, the PM agent is referred to as:

```text
Product Discovery Agent
```

It is responsible for:

- product discovery
- requirement elicitation
- inception
- story creation
- acceptance criteria
- prioritization

AI-CDAD starts after a demand enters the framework, either from Product Discovery Agent or from another lane such as bug, incident, tech debt or compliance.

---

## Human role boundaries

### PM / Product Discovery Agent

Owns:

- WHAT
- WHY
- VALUE
- PRIORITY
- product context
- acceptance criteria

Does not own technical implementation.

### Tech Lead

Owns:

- architecture
- technical strategy
- risk acceptance
- contract strategy
- migration strategy
- rollout strategy
- rollback strategy

Tech Lead is not expected to review every line of code.

### Developer

Owns:

- execution
- implementation feasibility
- edge cases
- tests
- PR readiness
- code quality
- AI-agent steering

The Developer is an **AI-Augmented Engineer**, not a prompt operator.

### AI / Execution Agent

Accelerates:

- context organization
- artifact drafting
- shaping
- implementation
- testing
- validation
- documentation

AI does not own risk, approvals or final accountability.

---

## Entry Lanes

AI-CDAD supports four demand entry lanes.

| Entry Lane | Used for | Typical Owner |
|---|---|---|
| Product | new features, product evolution, business enhancements | PM / Product |
| Operational | bugs, incidents, hotfixes, alerts | Developer / Tech Lead |
| Engineering | tech debt, refactor, upgrades, observability | Developer / Tech Lead |
| Compliance | security, audit, privacy, regulatory remediation | Security / Risk / Tech Lead |

---

## Risk Modes

AI-CDAD classifies each demand into one of three modes.

| Mode | When to use | Governance |
|---|---|---|
| FAST | low risk, local change, simple rollback | lightweight |
| HYBRID | new + existing systems, known dependencies | balanced |
| SAFE | brownfield critical, production, contracts, PII, compliance, low confidence | strong |

Safe default:

```text
If relevant uncertainty exists, increase rigor:
FAST → HYBRID → SAFE
```

---

## End-to-end flow

```text
Demand enters
  ↓
Entry Lane identified
  ↓
AI-CDAD Intake
  ↓
normalized-entry.md
  ↓
Triage, if needed
  ↓
delivery-assessment.md
  ↓
FAST / HYBRID / SAFE
  ↓
Technical context, if needed
  ↓
Tech Lead Design
  ↓
Solution Shaping
  ↓
Developer Feasibility Gate
  ↓
runtime-context.md
  ↓
ai-execution-brief.md
  ↓
Developer + AI Execution Agent
  ↓
Validation
  ↓
Review / Approval
  ↓
Deploy / Resolve
  ↓
Observe & Learn
  ↓
Close / Archive
```

---

## Repository model

AI-CDAD uses three repository layers.

### 1. `ai-cdad-framework`

Reusable method and operating model.

Contains:

```text
architecture/
playbooks/
policies/
templates/
agent-roles/
prompts/
adapters/
examples/
docs/
```

Purpose:

```text
How we work.
```

### 2. Central community repository / hub

Example:

```text
repo-central-ai-delivery-community
```

Contains:

```text
ai-cdad/
contexts/
initiatives/
indexes/
```

Purpose:

```text
Official memory, cross-repo governance and portfolio visibility.
```

### 3. Application repository

Where code lives.

Contains local AI-CDAD execution artifacts:

```text
.cdad/
  README.md
  framework-ref.md
  initiatives/
      <initiative-id>/
        runtime-context.md
        ai-execution-brief.md
        validation-report.md
        implementation-notes.md
        pr-summary.md
```

Purpose:

```text
Local execution close to code.
```

---

## Artifact location strategy

Do not duplicate everything everywhere.

| Artifact Type | Location |
|---|---|
| framework method | `ai-cdad-framework` |
| policies/templates/playbooks | `ai-cdad-framework` |
| global product/domain context | central community repository |
| initiative registry | central community repository |
| repo/component impact indexes | central community repository |
| runtime-context.md | application repository |
| ai-execution-brief.md | application repository |
| devin-execution-brief.md | application repository when using Devin |
| validation-report.md | application repository |
| approval-record.md | hub or local, depending on scope |
| initiative-summary.md | hub when archived |

---

## Context and token strategy

AI-CDAD is designed to avoid token bloat.

Main principle:

```text
Repositories store rich memory.
AI sessions use minimal runtime context.
```

Primary runtime artifact:

```text
runtime-context.md
```

It contains:

- goal
- scope
- out of scope
- risk mode
- required gates
- critical constraints
- evidence references
- stop conditions
- human owners
- validation requirements
- relevant files

Recommended token budgets:

| Mode | Target | Maximum |
|---|---:|---:|
| FAST | 20k | 40k |
| HYBRID | 50k | 100k |
| SAFE | 100k | 180k |

If context exceeds budget, generate:

```text
context-reduction-plan.md
```

---

## Governance hard stops

An AI Execution Agent must stop when detecting:

- production change
- API/data contract/schema/event change
- sensitive data / PII
- IAM/security permission change
- destructive operation
- relevant cost impact
- low AI confidence
- SAFE mode without required approvals
- conflict with another active initiative on a critical component/contract

Hard stop means:

```text
stop
explain risk
request approval
record decision
continue only if approved or plan adjusted
```

---

## Project documentation

For a professional overview of the project, see:

- [`docs/project/project-charter.md`](docs/project/project-charter.md)
- [`docs/project/market-positioning.md`](docs/project/market-positioning.md)
- [`docs/project/use-cases.md`](docs/project/use-cases.md)
- [`docs/project/adoption-model.md`](docs/project/adoption-model.md)
- [`docs/project/roadmap.md`](docs/project/roadmap.md)
- [`docs/project/faq.md`](docs/project/faq.md)

---

## How to use with Devin

Run prompts in this order:

```text
prompts/devin/00-plan-before-files.md
prompts/devin/01-create-scaffold.md
prompts/devin/02-strengthen-rules.md
prompts/devin/03-architecture-review.md
prompts/devin/04-apply-corrections.md
prompts/devin/05-create-examples.md
prompts/devin/06-final-audit.md
prompts/devin/07-setup-central-community-hub.md
prompts/devin/08-install-ai-cdad-in-application-repo.md
prompts/devin/09-tabletop-local-bugfix.md
prompts/devin/10-validate-framework-coverage.md
```

Start with:

```text
prompts/devin/00-plan-before-files.md
```

Important:

```text
Do not let Devin create or change files before it explains the plan.
```

---

## How to use with other AI tools

Use:

```text
prompts/ai-agents/generic-ai-execution-agent.md
```

or the tool-specific prompt:

```text
prompts/ai-agents/claude-code-execution.md
prompts/ai-agents/codex-execution.md
prompts/ai-agents/cursor-copilot-execution.md
```

Also review the relevant adapter:

```text
adapters/
```

---

## Information security

When using a personal repository, do not commit:

- customer data
- PII
- production logs with sensitive data
- secrets
- tokens
- passwords
- private keys
- proprietary internal code
- confidential architecture details
- non-public contracts or schemas

For corporate adoption, use an internal repository and follow:

```text
policies/information-security-policy.md
```

---

## Adoption path

Recommended adoption:

```text
1. Personal GitHub repo
2. AI-CDAD framework review
3. Devin or AI-agent planning
4. Tabletop tests
5. Central community repo pilot
6. One application repo pilot
7. Local bugfix test
8. HYBRID scenario test
9. SAFE brownfield scenario test
10. Internal security review
11. Squad/community rollout
```

---

## Validation status

This package includes validation reports:

```text
docs/notes/contract-validation-report.md
docs/notes/v7-48-checks-revalidation-report.md
docs/notes/tool-agnostic-contract-validation-report.md
```

The v7 package was validated against:

- original 48 contract checks
- tool-agnostic AI Execution Agent checks

---

## Final rule

> PM defines the what.  
> Tech Lead defines safe technical direction.  
> Developer owns execution.  
> AI accelerates.  
> AI-CDAD governs.

---

## Tool configuration templates

This package includes optional tool configuration templates under:

```text
tool-configs/
```

These templates help apply AI-CDAD instructions to tools such as Claude Code, Codex, Cursor and GitHub Copilot.

They are stored under `tool-configs/` so they do not become active automatically.

See:

```text
docs/notes/tool-configuration-guide.md
```

---

## Configuration and usage guides

For setup and operation, see:

```text
docs/usage/quickstart.md
docs/usage/configuration-guide.md
docs/usage/operating-manual.md
docs/notes/tool-configuration-guide.md
```

```text
docs/usage/devin-setup-guide.md
```

---

## MCP and Skills

AI-CDAD supports controlled MCP usage and reusable skills.

MCP configuration lives in:

```text
integrations/mcp/
```

Skill definitions live in:

```text
integrations/skills/
```

The execution brief must explicitly define:

- allowed MCPs
- forbidden MCPs
- MCP access level
- required skills
- optional skills
- stop conditions
- required approvals

Core rule:

```text
MCP access is read-only by default.
Write/action access requires approval.
Destructive access is a hard stop.
```
