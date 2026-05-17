---
applyTo: "**/*"
---

# AI-CDAD Path-Specific Instructions

Use AI-CDAD rules for all files.

Before implementing code, check for the current initiative context:

- runtime-context.md
- ai-execution-brief.md
- relevant-files-list.md

Infer the human-facing language from the user's request, existing artifacts and repository/team conventions. If the user communicates in Portuguese, use Portuguese Brazilian (`pt-BR`) by default.

If these are missing, ask for the minimum context needed before making broad suggestions.

Stop on:

- production risk
- contract/schema/API/event change
- PII/sensitive data
- IAM/security
- destructive operations
- missing approval
