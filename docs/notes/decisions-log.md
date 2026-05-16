# AI-CDAD Decisions Log

## Core decisions

- Nome oficial: **AI-CDAD — AI Context-Driven Adaptive Delivery**.
- PM Agent externo será chamado de **PM JIP - Brainstorm**.
- PM JIP - Brainstorm faz discovery, inception, histórias, aceite e priorização.
- AI-CDAD começa após a entrada da demanda no framework.
- Entry Lanes: Product, Operational, Engineering, Compliance.
- Risk Modes: FAST, HYBRID, SAFE.
- Classificação é policy-based.
- Se houver incerteza relevante: FAST → HYBRID → SAFE.
- AI-CDAD governa; AWS AI-DLC executa.
- Devin é Guided Orchestrator.
- Na v1, agentes são papéis/fases lógicas executadas pelo Devin.
- Tech Lead Playbook e Developer Playbook são separados.
- Cada playbook tem core + overlays FAST/HYBRID/SAFE.
- Developer é AI-Augmented Engineer.
- Artefatos são criados pela IA como draft.
- Humanos validam/aprovam quando há gate, risco, SAFE ou decisão crítica.
- Repo central/hub guarda artefatos globais/cross.
- Repo da aplicação guarda artefatos locais perto do código.
- runtime-context.md é o principal contexto da sessão Devin.
- Histórico arquivado é cold context e não entra por padrão.
- MCP é consultado de forma controlada pela camada Tech Lead.
- Hard stops obrigatórios: produção, contratos, PII, IAM, destrutivo, baixo contexto, SAFE sem aprovação.
- Parallel execution só quando seguro, independente e validável.
- Definition of Ready e Definition of Done são policies oficiais.
- Status UX é obrigatório.
- Context Minimization é obrigatório para evitar token bloat.
