---
name: gstack
preamble-tier: 1
version: 1.2.0
description: Router for the gstack skill suite. (gstack)
allowed-tools:
  - Bash
  - Read
  - AskUserQuestion
triggers:
  - gstack
  - which gstack skill
  - route this with gstack

---
<!-- AUTO-GENERATED from SKILL.md.tmpl — do not edit directly -->
<!-- Regenerate: bun run gen:skill-docs -->


## When to invoke this skill

Sends any gstack request to the right skill
(planning, review, QA, shipping, debugging, docs, security, design). For browser/QA
and dogfooding it points you at /browse. Use when you invoke gstack without a specific
skill, or ask "which gstack skill fits this?".

## Preamble (run first)

```bash
_UPD=$(~/.claude/skills/gstack/bin/gstack-update-check 2>/dev/null || .claude/skills/gstack/bin/gstack-update-check 2>/dev/null || true)
```