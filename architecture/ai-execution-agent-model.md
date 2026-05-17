# AI Execution Agent Model

## Purpose

AI-CDAD must be independent of a single AI tool.

The framework can be used with any AI execution tool that is able to follow:

- `runtime-context.md`
- `ai-execution-brief.md`
- policies
- playbooks
- hard stops
- human approval gates
- validation requirements
- evidence requirements

## Definition

An **AI Execution Agent** is any AI tool or agent used to execute delivery work under AI-CDAD constraints.

Examples:

- Devin
- Claude Code
- Codex
- Cursor
- GitHub Copilot
- Amazon Q Developer
- StackSpot AI
- ResolveAI
- internal agents

## Positioning

```text
AI-CDAD governs.
AWS AI-DLC structures the delivery lifecycle.
AI Execution Agent executes under guidance.
Humans retain ownership.
```

## Tool-Agnostic Contract

Every AI Execution Agent must:

1. read `runtime-context.md`
2. read `ai-execution-brief.md`
3. respect scope and out of scope
4. use the appropriate playbook and overlay
5. respect hard stops
6. stop if required context is missing
7. ask humans only for the minimum missing context
8. generate validation evidence
9. produce AI-CDAD Status Updates
10. never approve its own work
11. never accept risk on behalf of humans

## Devin Compatibility

Devin is the first supported implementation.

For compatibility, the artifact:

```text
devin-execution-brief.md
```

is treated as a Devin-specific alias for:

```text
ai-execution-brief.md
```

Both must follow the same execution contract.

## Required Adapter

Each supported tool should have an adapter document under:

```text
adapters/
```

The adapter must define:

- how to pass context
- how to constrain scope
- how to request diffs/changes
- how to request tests
- how to enforce stop conditions
- how to capture evidence
- how to produce AI-CDAD Status Updates

---

## MCP and Skill Resolution

AI Execution Agents must resolve MCPs and Skills from the framework structure.

Default locations:

```text
integrations/mcp/mcp-registry.md
integrations/skills/skill-registry.md
```

For each execution, the agent must read:

```text
runtime-context.md
ai-execution-brief.md
```

The execution brief tells the agent which MCPs and Skills are allowed.

If MCPs or Skills are not listed in the execution brief, the agent must not assume access.

If a needed MCP or Skill is missing, the agent must stop and ask for the minimum required context or create a proposal under `integrations/`.
