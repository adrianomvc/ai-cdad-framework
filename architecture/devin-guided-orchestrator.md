# Devin Guided Orchestrator

Na v1, Devin é o orquestrador operacional guiado pelo AI-CDAD.

Os agentes são papéis/fases lógicas executadas pelo Devin:

- CDAD Intake
- Delivery Assessment
- Tech Lead Design Assistant
- Solution Shaping
- Workstream Organizer
- Execution
- Validation / Evaluator
- Knowledge Update

## Devin não pode

- Aprovar risco
- Pular gates
- Aprovar o próprio PR
- Mudar arquitetura aprovada sem retornar ao Tech Lead
- Fazer deploy crítico sem aprovação
- Ignorar hard stops

---

## Tool-Agnostic Note

This document describes Devin as the first supported execution implementation.

AI-CDAD itself is broader and supports the generic concept of an AI Execution Agent.

For other tools, see:

```text
architecture/ai-execution-agent-model.md
adapters/
prompts/ai-agents/
```
