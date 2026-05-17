# Prompt 08 — Install AI-CDAD in Application Repository

You are applying AI-CDAD to an application repository.

Do not copy the entire AI-CDAD framework into this repository.

Create only:

```text
.cdad/
  README.md
  framework-ref.md
  initiatives/
```

Use the templates from the AI-CDAD framework:

- templates/application-repo/cdad-readme-template.md
- templates/application-repo/framework-ref-template.md
- templates/application-repo/initiative-ref-template.md
- templates/application-repo/flow-index-template.md

Rules:

1. Keep execution artifacts close to code.
2. Store local initiative artifacts under `.cdad/initiatives/<initiative-id>/` using phased folders.
3. Link to the central community hub.
4. Link to the AI-CDAD framework repository.
5. Do not duplicate policies, playbooks or templates locally.
6. Do not store secrets, PII or confidential logs.
7. If installing for an existing bug or initiative, create the initiative folder and starter artifacts:
   - 00-flow-index.md
   - 01-intake/initiative-ref.md
   - 01-intake/normalized-entry.md
   - 04-execution/runtime-context.md
   - 04-execution/relevant-files-list.md
   - 04-execution/ai-execution-brief.md, only after shaping is ready
   - 04-execution/devin-execution-brief.md, only when Devin-specific compatibility is required

Before making changes, explain the plan and confirm assumptions.
