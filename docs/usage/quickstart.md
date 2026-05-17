# AI-CDAD Quickstart

## 1. Choose how you want to use AI-CDAD

There are three common scenarios:

| Scenario | What to use |
|---|---|
| You want to evolve the framework | Use this repository directly |
| You want to create a central community hub | Use `prompts/devin/07-setup-central-community-hub.md` |
| You want to apply AI-CDAD to an application repo | Use `prompts/devin/08-install-ai-cdad-in-application-repo.md` or copy `.cdad/` templates manually |

---

## 2. First command with Devin

Open this repository in Devin and run only:

```text
prompts/devin/00-plan-before-files.md
```

Do not allow Devin to create or change files before it returns a plan.

Review the plan first.

Then run, in order:

```text
prompts/devin/01-create-scaffold.md
prompts/devin/02-strengthen-rules.md
prompts/devin/03-architecture-review.md
prompts/devin/04-apply-corrections.md
prompts/devin/05-create-examples.md
prompts/devin/06-final-audit.md
```

---

## 3. Install AI-CDAD in an application repository

In the application repository, create:

```text
.cdad/
  README.md
  framework-ref.md
  initiatives/
```

Use these templates:

```text
templates/application-repo/cdad-readme-template.md
templates/application-repo/framework-ref-template.md
templates/application-repo/initiative-ref-template.md
```

For a new initiative, create:

```text
.cdad/initiatives/<initiative-id>/
  initiative-ref.md
  normalized-entry.md
  runtime-context.md
  relevant-files-list.md
  ai-execution-brief.md
```

If using Devin specifically, you may also use:

```text
devin-execution-brief.md
```

as a Devin-compatible alias for:

```text
ai-execution-brief.md
```

---

## 4. Install optional AI tool configuration

Copy the relevant template from `tool-configs/` to the expected tool location.

Examples:

```text
tool-configs/generic/AGENTS.md
→ AGENTS.md

tool-configs/claude/CLAUDE.md
→ CLAUDE.md

tool-configs/codex/AGENTS.md
→ AGENTS.md

tool-configs/cursor/.cursor/rules/ai-cdad.mdc
→ .cursor/rules/ai-cdad.mdc

tool-configs/copilot/.github/copilot-instructions.md
→ .github/copilot-instructions.md
```

Only copy what you need.

Do not activate all configurations blindly.

---

## 5. Minimum execution loop

For any AI Execution Agent:

```text
runtime-context.md
↓
ai-execution-brief.md
↓
relevant-files-list.md
↓
AI agent execution
↓
validation-report.md
↓
pr-summary.md
↓
initiative-summary.md
```

---

## 6. Safety rule

Before corporate use:

- remove sensitive data
- do not commit secrets
- do not include customer data
- do not paste production logs with PII
- run security review
- adapt policies to your organization

See:

```text
policies/information-security-policy.md
```
