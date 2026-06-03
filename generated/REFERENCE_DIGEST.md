# Reference Digest

## Purpose

This generated digest summarizes the external references that Self-Build Mode should use when constructing or refreshing this central skill.

The digest is subordinate to the three core files.

## Reference Summary

### anthropics/skills

Use as the official example repository for Agent Skills.

Extract:

- folder-based skill packaging
- `SKILL.md` as the skill entry point
- instructions/scripts/resources separation
- concrete skill examples
- marketplace-compatible skill shape

### agentskills/agentskills and agentskills.io

Use as the format reference for portable Agent Skills.

Extract:

- frontmatter conventions
- discovery/activation/execution lifecycle
- progressive disclosure
- optional resource directories
- cross-agent compatibility

### AGENTS.md and OpenAI Codex AGENTS.md Guide

Use as the project-level agent context reference.

Extract:

- `AGENTS.md` as canonical project entry
- concise setup/test/style/workflow instruction layout
- Codex-compatible instruction loading assumptions
- nested/project-specific guidance ideas

### agent-skill-bus

Use as the runtime self-improvement reference.

Extract:

- run logging
- health checks
- drift detection
- score-based skill quality monitoring
- record-run pattern
- self-improvement loop
- Knowledge Watcher idea

### alinaqi/maggy

Use as the high-complexity AI engineering harness reference.

Extract:

- skills/hooks/rules/templates/evals organization
- quality gates
- ADR workflows
- persistent memory
- validation and routing concepts

### NeoLabHQ/context-engineering-kit

Use as the context engineering and skill plugin reference.

Extract:

- token-efficient skill loading
- plugin granularity
- review/reflexion workflows
- quality-focused context design
- cross-client skill compatibility

### VoltAgent/awesome-agent-skills

Use as an ecosystem index only.

Extract:

- skill categories
- naming patterns
- candidate projects for deeper review

Do not treat it as a quality guarantee.

## Principles Extracted

1. Keep the core skill small.
2. Put detailed operational support in generated files.
3. Make project-level context independent.
4. Use `AGENTS.md` as the canonical project entry.
5. Use project-level skills for specialized agent behavior.
6. Record experience in durable project files.
7. Convert repeated failures into regression cases.
8. Separate low-risk, medium-risk, and high-risk changes.
9. Treat emotion as a signal, not as truth.
10. Use external reference structures, not wholesale copied content.
