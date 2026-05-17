# AI-CDAD Configuration Guide

## Repository-level configuration

AI-CDAD can be configured at three levels:

```text
1. Framework repository
2. Central community hub
3. Application repository
```

---

## 1. Framework repository

This repository stores the reusable method:

```text
architecture/
policies/
playbooks/
templates/
prompts/
adapters/
tool-configs/
docs/
```

Do not store company secrets, customer data, production logs or proprietary implementation details here if the repository is public.

---

## 2. Central community hub

Create a central hub for domain/product memory and cross-repo governance:

```text
ai-cdad/
contexts/
initiatives/
indexes/
```

Use:

```text
prompts/devin/07-setup-central-community-hub.md
```

The hub should contain:

- product/domain context
- active initiatives
- archived initiatives
- repo impact index
- component impact index
- approval records for cross-repo decisions

---

## 3. Application repository

Install only the local `.cdad/` folder:

```text
.cdad/
  README.md
  framework-ref.md
  initiatives/
```

Use:

```text
prompts/devin/08-install-ai-cdad-in-application-repo.md
```

Do not copy the entire framework into the application repository.

---

## 4. AI tool configuration

Optional tool configurations live in:

```text
tool-configs/
```

They are inactive until copied to the expected tool location.

### Generic

```text
tool-configs/generic/AGENTS.md
→ AGENTS.md
```

### Claude Code

```text
tool-configs/claude/CLAUDE.md
→ CLAUDE.md
```

Optional settings:

```text
tool-configs/claude/.claude/settings.json.template
→ .claude/settings.json
```

### Codex

```text
tool-configs/codex/AGENTS.md
→ AGENTS.md
```

Optional config:

```text
tool-configs/codex/.codex/config.toml.template
→ .codex/config.toml
```

### Cursor

```text
tool-configs/cursor/.cursor/rules/ai-cdad.mdc
→ .cursor/rules/ai-cdad.mdc
```

### GitHub Copilot

```text
tool-configs/copilot/.github/copilot-instructions.md
→ .github/copilot-instructions.md
```

Optional path-specific instruction:

```text
tool-configs/copilot/.github/instructions/ai-cdad.instructions.md
→ .github/instructions/ai-cdad.instructions.md
```

---

## 5. What every tool config must enforce

Every tool configuration must point the AI agent to:

- `00-flow-index.md`
- `04-execution/runtime-context.md`
- `04-execution/ai-execution-brief.md`
- `04-execution/relevant-files-list.md`
- hard stops
- scope/out of scope
- human gates
- validation requirements

---

## 6. Do not configure unsafe automation by default

Avoid automatic permissions for:

- production deploy
- destructive operations
- IAM/security changes
- secret access
- database destructive commands
- forced pushes
- cloud infrastructure changes

These must remain human-approved.

---

### Devin

Devin does not need to copy a tool configuration file into the repository root.

Instead, use the Devin setup flow and session instructions.

Reference:

```text
docs/usage/devin-setup-guide.md
tool-configs/devin/devin-session-instructions.md
```

Recommended first prompt in Devin:

```text
prompts/devin/00-plan-before-files.md
```

For application repositories, use:

```text
prompts/devin/08-install-ai-cdad-in-application-repo.md
```

---

## MCP and Skills Configuration

Use:

```text
integrations/mcp/
integrations/skills/
```

to define available MCPs and reusable Skills.

### Add a new MCP

1. Create `integrations/mcp/<mcp-name>.md`.
2. Register it in `integrations/mcp/mcp-registry.md`.
3. Define access level: read-only, write or destructive.
4. Define allowed risk modes.
5. Define required approvals.
6. Reference it in `04-execution/ai-execution-brief.md`.

### Add a new Skill

1. Create `integrations/skills/<skill-name>.md`.
2. Use `integrations/skills/skill-template.md`.
3. Register it in `integrations/skills/skill-registry.md`.
4. Reference it in `04-execution/ai-execution-brief.md`.

### Agent rule

If a Skill or MCP is needed but missing from the registry, the agent must not improvise.

It must propose the new entry and ask for human approval when required.
