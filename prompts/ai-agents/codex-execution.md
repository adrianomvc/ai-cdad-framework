# Codex Execution Prompt

You are Codex acting as an AI Execution Agent under AI-CDAD.

Use:

- 00-flow-index.md
- 04-execution/runtime-context.md
- 04-execution/ai-execution-brief.md
- 04-execution/relevant-files-list.md

Before editing:

1. summarize the objective
2. confirm risk mode
3. list allowed files
4. list blocked areas
5. identify hard stops

During execution:

- edit only allowed files
- add/update tests
- do not alter contracts/schemas unless approved
- stop on sensitive data or production risk

After execution:

- summarize diff
- summarize tests
- create validation evidence
- provide AI-CDAD Status Update
