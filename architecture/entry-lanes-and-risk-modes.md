# Entry Lanes and Risk Modes

## Entry Lanes

- Product: PM JIP - Brainstorm, negócio, feature, evolução.
- Operational: bug, incidente, hotfix, alerta.
- Engineering: tech debt, refactor, upgrade, observability.
- Compliance: security, audit, LGPD, CVE.

## Risk Modes

- FAST: baixo risco, local, rollback simples.
- HYBRID: novo + legado, dependências conhecidas.
- SAFE: brownfield crítico, produção, contrato, PII, compliance ou incerteza.

## Safe Default

Se houver incerteza relevante:

```text
FAST → HYBRID → SAFE
```
