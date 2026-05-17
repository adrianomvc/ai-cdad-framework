# Operating Model

## Product Discovery Agent

Responsável por discovery, inception, histórias, critérios de aceite, valor, prioridade e escopo de negócio.

É externo ao AI-CDAD.

## Tech Lead

Responsável por direção arquitetural, risco, contratos, migração, rollout, rollback e decisões técnicas.

## Developer

Responsável por execução técnica, testes, edge cases, PR readiness, qualidade e condução do Devin.

## Devin / IA

Responsável por drafts de artefatos, organização de contexto, shaping, implementação assistida, testes, validação e documentação.

A IA não aprova risco e não substitui ownership humano.

## HITL

Human-in-the-loop acontece em:

- PM validation
- Tech Lead design approval
- Developer feasibility gate
- Review / approval
- Hard stops
- SAFE mode
- Compliance/security

---

## AI Execution Agent

AI-CDAD can be executed by multiple AI tools.

Examples:

- Devin
- Claude Code
- Codex
- Cursor
- GitHub Copilot
- Amazon Q Developer
- internal agents

The execution agent must follow:

- runtime-context.md
- ai-execution-brief.md
- policies
- playbooks
- human approval gates
- stop conditions

Devin remains the first supported implementation.
