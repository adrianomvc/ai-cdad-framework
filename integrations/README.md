# Integrations

This folder defines how AI-CDAD handles external tools, sources and reusable agent capabilities.

It has two main areas:

```text
integrations/
  mcp/
  skills/
```

## MCP

MCP entries describe external tools or sources that an AI Execution Agent may query or invoke.

Examples:

- GitHub
- Jira
- Confluence
- DataDog
- AWS
- internal catalogs
- internal documentation systems

## Skills

Skills describe reusable execution capabilities that an AI Execution Agent can apply.

Examples:

- bugfix analysis
- incident triage
- brownfield impact analysis
- data quality validation
- observability review
- PR review

## Core Rule

AI-CDAD does not allow agents to use tools freely by default.

The execution brief must explicitly define:

- allowed MCPs
- forbidden MCPs
- MCP access mode
- skills to use
- stop conditions
- required approvals
