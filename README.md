# AI-CDAD — AI Context-Driven Adaptive Delivery

AI-CDAD é um framework de entrega adaptativa guiada por contexto para squads que usam IA no delivery de software e dados.

## Posicionamento

> AI-CDAD governa.  
> AWS AI-DLC executa.  
> Devin orquestra guiado.  
> Humanos mantêm ownership.

## Objetivo

Apoiar entregas com IA em:

- Greenfield
- Brownfield
- Hybrid
- Bugs
- Incidentes
- Hotfixes
- Tech debt
- Refactor
- Compliance / Security remediation

## Filosofia

- Context before code
- Humans own decisions
- AI accelerates execution
- Policy-based routing
- Risk-adaptive governance
- Minimal runtime context
- Evidence-based execution

## Papéis humanos

| Papel | Responsabilidade |
|---|---|
| PM JIP - Brainstorm | Define WHAT, WHY, VALUE, PRIORITY |
| Tech Lead | Define arquitetura, risco, contratos, rollout e rollback |
| Developer | É dono da execução, testes, PR e qualidade |
| Security/Risk | Valida compliance, segurança, privacidade e evidências quando necessário |

## Estrutura

```text
architecture/     visão geral e desenho operacional
playbooks/        playbooks Tech Lead e Developer
policies/         políticas de governança, contexto, routing e validação
templates/        templates de artefatos
agent-roles/      papéis agenticos lógicos executados pelo Devin
prompts/devin/    prompts para instalação e revisão no Devin
examples/         fluxos simulados
docs/             apresentações, decisões e notas
```

## Como usar

1. Suba este conteúdo no seu GitHub pessoal.
2. Abra o repo no Devin.
3. Execute primeiro `prompts/devin/00-plan-before-files.md`.
4. Depois siga os prompts em ordem.
5. Faça tabletop tests com os exemplos.
