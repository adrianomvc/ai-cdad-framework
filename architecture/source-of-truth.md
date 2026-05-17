# AI-CDAD Source of Truth

This file is the operational contract for the AI-CDAD framework.

If there is any conflict between files, this priority order applies:

1. `README.md`
2. `architecture/source-of-truth.md`
3. `docs/notes/decisions-log.md`
4. `policies/*.md`
5. `playbooks/*.md`
6. `templates/*.md`
7. `examples/*`

---

## Official Name

**AI-CDAD — AI Context-Driven Adaptive Delivery**

Portuguese interpretation:

> Entrega Adaptativa Guiada por Contexto com IA

---

## Positioning

```text
AI-CDAD governs.
AI-DLC structures the lifecycle.
AI Execution Agents execute under guidance.
Humans retain ownership.
```

AI-CDAD is an operating model, not a coding bot.

---

## Non-negotiable Principles

1. Context before code.
2. AI drafts; humans own.
3. Risk-adaptive delivery.
4. Minimal runtime context.
5. Evidence-based trust.
6. Safe default: FAST → HYBRID → SAFE when uncertainty exists.
7. AI Execution Agents are guided, not free-running.
8. Developer remains an AI-Augmented Engineer, not a prompt operator.
9. Tech Lead owns architectural risk.
10. Product Discovery Agent remains external.

---

## Human Role Boundaries

### Product Discovery Agent

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
- technical direction
- risk acceptance
- contract strategy
- migration
- rollout
- rollback

### Developer

Owns:

- execution
- implementation feasibility
- edge cases
- tests
- PR readiness
- code quality
- AI-agent steering

### AI Execution Agent

Accelerates:

- artifact drafting
- context organization
- shaping
- implementation
- tests
- validation
- documentation

Does not approve risk or own final accountability.

---

## Entry Lanes

- Product
- Operational
- Engineering
- Compliance

---

## Risk Modes

### FAST

Low risk, local, isolated, simple rollback.

### HYBRID

New + existing systems, controlled integration, moderate dependency.

### SAFE

Brownfield critical, production, contracts, PII, security, compliance, migration, destructive operations or low confidence.

---

## Repository Model

### `ai-cdad-framework`

Reusable method:

- architecture
- playbooks
- policies
- templates
- agent roles
- prompts
- examples
- docs

### Central Community Repository

Official community/domain memory:

- domain context
- product context
- active initiatives
- archived initiatives
- impact indexes
- cross-repo decisions

### Application Repository

Local execution near code:

- `.cdad/initiatives/<initiative-id>/runtime-context.md`
- `.cdad/initiatives/<initiative-id>/ai-execution-brief.md`
- `.cdad/initiatives/<initiative-id>/validation-report.md`

---

## Artifact Rule

```text
AI drafts.
Human validates or approves when required.
Artifact becomes official.
```

---

## Context Rule

```text
Repos store rich memory.
AI execution sessions use minimal runtime context.
```

Primary runtime artifact:

```text
runtime-context.md
```

Never remove to save tokens:

- risk mode
- scope
- out of scope
- hard stops
- required gates
- stop conditions
- human owner
- validation requirements
- evidence references

---

## Hard Stops

AI Execution Agents must stop for:

- production change
- API/data contract/schema/event change
- PII/sensitive data
- IAM/security permissions
- destructive operation
- relevant cost impact
- low AI confidence
- SAFE mode without required approvals
- critical conflict with another active initiative

---

## Status UX

Every meaningful AI Execution Agent action must produce:

```markdown
## AI-CDAD Status Update

**Current Stage:**  
<stage>

**Created/Updated Artifacts:**  
- <file> — <location>

**Human Action Required:**  
- <who must do what>

**Blocking Issues:**  
- <if any>

**Next Step:**  
<next action>

**Confidence:**  
High | Medium | Low
```

---

## Tool-Agnostic AI Execution

AI-CDAD must be AI Execution Agent agnostic.

Devin is the first supported implementation, not the only one.

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

For Devin compatibility, this may be named:

```text
devin-execution-brief.md
```

Both names refer to the same execution contract.

Every AI Execution Agent must obey:

- runtime-context.md
- execution brief
- policies
- playbooks
- hard stops
- human gates
- validation requirements
- evidence references
