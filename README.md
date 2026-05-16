# AI-CDAD — AI Context-Driven Adaptive Delivery

AI-CDAD is an enterprise delivery framework for AI-augmented software and data delivery.

It is designed to help teams use AI tools such as Devin safely and effectively across:

- greenfield initiatives
- brownfield evolution
- hybrid delivery
- bugs
- incidents
- hotfixes
- technical debt
- refactoring
- compliance and security remediation

## Positioning

> AI-CDAD governs.  
> AWS AI-DLC executes.  
> Devin orchestrates under guidance.  
> Humans retain ownership.

AI-CDAD is not a coding agent.  
AI-CDAD is not a replacement for Product, Tech Lead or Developer judgment.

It is an operating model that defines how context, risk, human decisions, artifacts, playbooks and AI-assisted execution work together.

---

## Why this framework exists

AI delivery fails when the model starts coding without enough context.

Common problems:

- AI changes code without understanding business impact.
- Brownfield changes are treated like greenfield work.
- Developers become prompt operators instead of technical owners.
- Tech Leads become bottlenecks reviewing everything.
- Context grows too large and consumes too many tokens.
- Decisions are lost in chat, Teams or PR comments.
- Multiple initiatives modify the same repository without coordination.
- Risks around production, contracts, PII, IAM and rollback are discovered too late.

AI-CDAD solves this by introducing:

- entry lanes
- risk modes
- context lifecycle
- runtime context
- human-in-the-loop gates
- playbooks by role
- policies
- artifact ownership
- minimal runtime context
- evidence-based execution

---

## Core principles

1. **Context before code**  
   AI must understand enough context before execution.

2. **AI drafts, humans own**  
   AI creates artifacts and suggestions. Humans validate critical decisions.

3. **Risk-adaptive delivery**  
   Low-risk work should be fast. Brownfield critical work should be safe.

4. **Minimal runtime context**  
   Repositories store rich memory. Devin sessions load only what is needed.

5. **Evidence-based trust**  
   Runtime summaries must reference evidence, not rely on unsupported assumptions.

6. **Safe default**  
   If relevant uncertainty exists, increase rigor: FAST → HYBRID → SAFE.

7. **Devin is guided, not free-running**  
   Devin executes within AI-CDAD policies, playbooks, gates and stop conditions.

---

## Relationship with AWS AI-DLC

AI-CDAD integrates with AWS AI-DLC as the execution engine.

AI-CDAD defines:

- how a demand enters the flow
- how risk is classified
- which playbooks apply
- which artifacts are required
- which humans must approve
- which context is loaded
- when Devin must stop

AWS AI-DLC supports execution phases such as:

- Discover
- Design
- Build
- Test
- Deploy
- Observe

In short:

```text
AI-CDAD = governance and operating model
AI-DLC = execution lifecycle
Devin = guided orchestrator
