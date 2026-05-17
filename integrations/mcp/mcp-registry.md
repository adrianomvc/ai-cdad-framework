# MCP Registry

## Purpose

List MCPs available to AI-CDAD and define how each may be used.

## Registry

| MCP | Purpose | Access Level | Allowed Modes | Human Approval | Owner | Notes |
|---|---|---|---|---|---|---|
| GitHub MCP | repositories, PRs, issues | read/write | FAST/HYBRID/SAFE | write requires approval | Engineering | use for repo context and PRs |
| Documentation MCP | docs, knowledge base | read-only | FAST/HYBRID/SAFE | no, unless sensitive | Architecture | use for product/domain context |
| Issue Tracker MCP | issues, tasks, backlog | read/write | FAST/HYBRID/SAFE | write requires approval | Product/Engineering | use for demand traceability |
| Observability MCP | logs, metrics, traces | read-only | HYBRID/SAFE | may require approval | SRE/Tech Lead | avoid copying sensitive logs |
| Cloud MCP | cloud resources | read/write/destructive | SAFE | approval required | Platform/Tech Lead | IAM/cost/destructive changes are hard stops |
| Data Catalog MCP | schemas, datasets, lineage | read-only | HYBRID/SAFE | no, unless sensitive | Data Governance | use for data impact analysis |

## How to Add a New MCP

Create a file:

```text
integrations/mcp/<mcp-name>.md
```

Use this structure:

```markdown
# <MCP Name>

## Purpose

## Capabilities

## Access Level

read-only | write | destructive

## Allowed Risk Modes

FAST | HYBRID | SAFE

## Required Approval

## Sensitive Data Risk

## Allowed Operations

## Forbidden Operations

## Evidence Handling

## Stop Conditions

## Owner
```

Then add it to this registry.
