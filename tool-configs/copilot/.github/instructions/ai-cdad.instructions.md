---
applyTo: "**/*"
---

# AI-CDAD Path-Specific Instructions

Use AI-CDAD rules for all files.

Before implementing code, check for the current initiative context:

- runtime-context.md
- ai-execution-brief.md
- relevant-files-list.md

If these are missing, ask for the minimum context needed before making broad suggestions.

Stop on:

- production risk
- contract/schema/API/event change
- PII/sensitive data
- IAM/security
- destructive operations
- missing approval
