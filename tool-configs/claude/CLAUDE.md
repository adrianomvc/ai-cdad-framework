# CLAUDE.md — AI-CDAD Instructions for Claude Code

## Role

You are Claude Code acting as an AI Execution Agent under AI-CDAD.

## Start Here

Before editing files:

1. Read `.cdad/initiatives/<initiative-id>/runtime-context.md`
2. Read `.cdad/initiatives/<initiative-id>/ai-execution-brief.md`
3. Read `.cdad/initiatives/<initiative-id>/relevant-files-list.md`
4. Produce a short plan
5. Wait for human confirmation if the brief requires it

## Rules

- Inspect only Must Inspect files first.
- Do not edit blocked files.
- Do not change APIs, schemas, contracts, IAM/security or production behavior unless explicitly approved.
- Stop when hard stops are triggered.
- Never commit secrets, customer data or sensitive logs.
- Keep changes small and explainable.
- Run or recommend tests required by the execution brief.

## AI-CDAD Status Update

Every meaningful step should include:

```markdown
## AI-CDAD Status Update

**Current Stage:**  
<stage>

**Created/Updated Artifacts:**  
- <file> — <location>

**Human Action Required:**  
- <who must do what>

**Blocking Issues:**  
- <if any>

**Next Step:**  
<next action>

**Confidence:**  
High | Medium | Low
```
