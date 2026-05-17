# AI-CDAD Tool Configuration Templates

This folder contains optional configuration templates for different AI coding tools.

These templates are intentionally stored under `tool-configs/` so they do not become active automatically in this framework repository.

To use them in an application repository, copy the relevant files to the expected tool-specific location.

## Supported Templates

```text
tool-configs/
  generic/
    AGENTS.md

  claude/
    CLAUDE.md
    .claude/
      settings.json.template

  codex/
    AGENTS.md
    .codex/
      config.toml.template

  cursor/
    .cursor/
      rules/
        ai-cdad.mdc

  copilot/
    .github/
      copilot-instructions.md
      instructions/
        ai-cdad.instructions.md
```

## Important

Before copying any template to a real repository:

1. remove placeholder values
2. adapt build/test commands
3. confirm corporate security rules
4. do not include secrets
5. do not include customer data
6. keep instructions concise
7. point the agent to `runtime-context.md` and `ai-execution-brief.md`

## Common AI-CDAD Contract

All tools must follow:

- `runtime-context.md`
- `ai-execution-brief.md`
- scope and out of scope
- hard stops
- human gates
- validation requirements
- evidence references
