# MCP Consumption Policy

## Purpose

Define safe and controlled use of MCP sources.

---

## Principle

MCP is not free-form internal internet.

It must be used to create curated technical context.

---

## Flow

```text
normalized-entry.md
↓
delivery-assessment.md
↓
mcp-query-plan.md
↓
controlled MCP queries
↓
technical-context-pack.md
↓
Tech Lead validation when needed
↓
Shaping / Devin execution
```

---

## MCP Query Plan

Before querying MCP, create:

```text
mcp-query-plan.md
```

It must include:

- objective
- questions to answer
- sources to query
- search terms
- expected outputs
- do-not-load list

---

## Technical Context Pack

After querying MCP, create:

```text
technical-context-pack.md
```

It must include:

- must-know context
- relevant repos
- relevant components
- known dependencies
- contracts/schemas
- evidence references
- unknowns
- optional details

---

## v1 Sources

- GitHub
- Docs / Confluence
- Jira
- architecture docs
- API/data contracts

## Phase 2 Sources

- AWS
- DataDog
- CloudWatch
- Glue / Athena / Data Catalog

---

## Rule for Devin

In v1, Devin should consume curated context.

Devin should not freely query all MCP sources unless explicitly allowed by a Tech Lead or policy update.
