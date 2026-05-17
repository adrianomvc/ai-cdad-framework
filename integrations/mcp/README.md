# MCP Integration

## Purpose

This folder defines the Model Context Protocol sources/tools available to AI-CDAD.

MCP is treated as a controlled capability.

AI agents must not query or invoke MCPs freely without an execution context.

## Files

```text
integrations/mcp/
  README.md
  mcp-registry.md
  mcp-access-levels.md
  mcp-query-plan-template.md
  technical-context-pack-template.md
  examples/
```

## Flow

```text
Delivery Assessment
↓
Risk Mode
↓
MCP Query Plan
↓
Controlled MCP access
↓
Technical Context Pack
↓
Tech Lead / Developer review, if required
↓
AI Execution Brief
↓
Execution
```

## Rule

Read-only MCP access may be allowed by policy.

Write/action/destructive MCP access requires explicit human approval.
