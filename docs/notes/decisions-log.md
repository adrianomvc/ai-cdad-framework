# AI-CDAD Decisions Log

This document records the key design decisions behind AI-CDAD.

---

## 1. Naming

- Official name: **AI-CDAD — AI Context-Driven Adaptive Delivery**.
- Portuguese meaning: Entrega Adaptativa Guiada por Contexto com IA.
- CDAD may still refer to the internal delivery governance flow.

---

## 2. Positioning

- AI-CDAD governs.
- AWS AI-DLC executes.
- Devin orchestrates under guidance.
- Humans retain ownership.

---

## 3. PM Boundary

- PM Agent is external.
- Its name in this framework is **Product Discovery Agent**.
- It handles discovery, inception, stories, acceptance criteria and prioritization.
- AI-CDAD does not implement Product Discovery Agent.

---

## 4. Human Roles

### PM / Product Discovery Agent

Owns WHAT, WHY, VALUE and PRIORITY.

### Tech Lead

Owns architecture, technical direction, risk, contracts, rollout and rollback.

### Developer

Owns execution, implementation feasibility, tests, PR readiness and quality.

### Devin / AI

Drafts, accelerates and supports, but does not own accountability.

---

## 5. Entry Lanes

- Product
- Operational
- Engineering
- Compliance

---

## 6. Risk Modes

- FAST
- HYBRID
- SAFE

Safe default:

```text
FAST → HYBRID → SAFE
```

---

## 7. Agent Model

- In v1, agent roles are logical phases executed by Devin.
- They are not separate autonomous systems by default.
- Devin is a guided orchestrator.

---

## 8. Playbooks

Two main playbooks:

- Tech Lead Playbook
- Developer Playbook

Each playbook has:

- core.md
- fast-overlay.md
- hybrid-overlay.md
- safe-overlay.md

---

## 9. Artifact Strategy

- AI drafts.
- Human validates/approves when required.
- Artifact becomes official after required validation.
- Human should not manually fill long documents from scratch.

---

## 10. Repository Model

Three layers:

1. `ai-cdad-framework`
2. central community repository / hub
3. application repository

---

## 11. Context Strategy

- Repositories store rich memory.
- Devin session uses minimal runtime context.
- `runtime-context.md` is the primary runtime context.
- Archived initiatives are cold context and not loaded by default.

---

## 12. MCP

- MCP is consulted by the Tech Lead Design layer.
- `mcp-query-plan.md` must exist before MCP queries.
- `technical-context-pack.md` consolidates curated results.
- Devin does not freely search everything in v1.

---

## 13. Governance

Hard stops:

- production
- contract/schema/API/event
- PII
- IAM/security
- destructive operations
- relevant cost impact
- low AI confidence
- SAFE without approval
- critical parallel initiative conflict

---

## 14. Parallel Execution

- Allowed only when safe, independent and validatable.
- Workstream Organizer creates `parallel-execution-plan.md`.
- SAFE avoids parallel critical changes.

---

## 15. Definition of Ready

Each phase must have minimum information before advancing.

If missing, Devin asks only for the minimum needed context.

---

## 16. Definition of Done

Code delivered is not enough.

Done requires validation, evidence, approvals when required, observability when applicable and learning/summary.

---

## 17. Status UX

Every Devin step that creates, updates, blocks or asks for approval must output a AI-CDAD Status Update.

---

## 18. Context Budget

Targets:

- FAST: target 20k, max 40k
- HYBRID: target 50k, max 100k
- SAFE: target 100k, max 180k

If exceeded, generate `context-reduction-plan.md`.
