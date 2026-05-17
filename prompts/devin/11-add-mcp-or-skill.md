# Prompt 11 — Add MCP or Skill

You are helping evolve AI-CDAD by adding a new MCP or Skill.

Before changing files, identify whether the request is:

1. New MCP
2. New Skill
3. Update to existing MCP
4. Update to existing Skill

Rules:

- MCPs go under `integrations/mcp/`.
- Skills go under `integrations/skills/`.
- Every MCP must be registered in `integrations/mcp/mcp-registry.md`.
- Every Skill must be registered in `integrations/skills/skill-registry.md`.
- Do not add secrets or real credentials.
- Do not enable write/destructive access by default.
- Read-only is the default MCP access level.
- Write access requires approval.
- Destructive access is a hard stop.
- Update `templates/execution/ai-execution-brief-template.md` only if the contract needs to change.
- Update docs if usage changes.

Output:

1. proposed files to create/update
2. risk assessment
3. access level
4. approval required
5. final diff summary
