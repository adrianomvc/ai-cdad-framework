# Tool Configuration Guide

AI-CDAD can provide optional repository-level guidance for AI coding tools.

This guide explains where to place configuration files when applying AI-CDAD to an application repository.

## Recommended Configurations

### Generic / Agents.md-compatible tools

Copy:

```text
tool-configs/generic/AGENTS.md
```

to:

```text
AGENTS.md
```

Use this when a tool supports `AGENTS.md` or agent instruction files.

---

### Claude Code

Copy:

```text
tool-configs/claude/CLAUDE.md
```

to the repository root as:

```text
CLAUDE.md
```

Optional local settings template:

```text
tool-configs/claude/.claude/settings.json.template
```

Review and copy as:

```text
.claude/settings.json
```

Do not add secrets to settings files.

---

### Codex

Copy:

```text
tool-configs/codex/AGENTS.md
```

to:

```text
AGENTS.md
```

Optional configuration template:

```text
tool-configs/codex/.codex/config.toml.template
```

Review and copy as:

```text
.codex/config.toml
```

---

### Cursor

Copy:

```text
tool-configs/cursor/.cursor/rules/ai-cdad.mdc
```

to:

```text
.cursor/rules/ai-cdad.mdc
```

---

### GitHub Copilot

Copy:

```text
tool-configs/copilot/.github/copilot-instructions.md
```

to:

```text
.github/copilot-instructions.md
```

Optional path-specific instruction:

```text
tool-configs/copilot/.github/instructions/ai-cdad.instructions.md
```

to:

```text
.github/instructions/ai-cdad.instructions.md
```

---

## Safety Notes

Do not blindly copy these templates.

Before enabling in a real repository:

- remove placeholders
- adapt commands
- validate paths
- remove secrets
- confirm security policy
- ensure the AI-CDAD `.cdad/` folder is installed
