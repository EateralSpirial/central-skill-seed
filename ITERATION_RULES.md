# Iteration Rules

## Purpose

These rules govern the seed and its generation of a separate full skill package.

The seed does not self-complete in place.

The seed emits or updates a separate full skill package.

## Core Invariant

The seed must remain a small generator.

The full skill must remain a separate operational artifact.

```text
seed != full skill
```

## Three-File Seed Core

The seed core has exactly three operational files:

- `SKILL.md`
- `ITERATION_RULES.md`
- `PROJECT_REFERENCES.md`

Do not add another operational core file without explicit user approval.

`README.md` and `full-skill/` are repository support materials, not seed core.

## Full Skill Generation Loop

When asked to generate or refresh the full skill, the agent must:

1. Read seed `SKILL.md`.
2. Read seed `ITERATION_RULES.md`.
3. Read seed `PROJECT_REFERENCES.md`.
4. Inspect the local `full-skill/` blueprint if available.
5. Inspect mandatory approved external references when network access is available.
6. Extract reusable structures and safeguards.
7. Generate or update the full skill in a separate target directory.
8. Verify that the full skill has its own `SKILL.md`, rules, protocols, templates, and project-bootstrap mechanism.
9. Verify that the full skill does not depend on this seed.
10. Record the target under `PROJECT_REFERENCES.md` if appropriate.

## Approved Reference Extraction

The seed may use only sources explicitly listed in `PROJECT_REFERENCES.md`.

### Agent Skills Format

Use:

- `anthropics/skills`
- `agentskills/agentskills`
- `agentskills.io`

Extract:

- skill package structure
- `SKILL.md` role
- frontmatter conventions
- progressive disclosure
- resource/script/template separation

### Project-Level Agent Context

Use:

- `AGENTS.md`
- OpenAI Codex `AGENTS.md` guide

Extract:

- `AGENTS.md` as project-level entry
- instruction layering assumptions
- concise setup/test/style/workflow patterns

### Runtime Self-Improvement

Use:

- `ShunsukeHayashi/agent-skill-bus`

Extract:

- run logging
- health checks
- drift detection
- self-improvement loops
- low-risk repair and high-risk approval boundaries

### Engineering Harness

Use:

- `alinaqi/maggy`

Extract:

- skills/hooks/rules/templates/evals organization
- quality gates
- ADR/review workflows
- memory and routing patterns

### Context Engineering

Use:

- `NeoLabHQ/context-engineering-kit`

Extract:

- low-token context layout
- plugin-oriented skills
- review and reflexion workflows
- granular context loading

### Ecosystem Survey

Use:

- `VoltAgent/awesome-agent-skills`

Extract:

- naming patterns
- common skill categories
- candidate repositories for later review

Do not treat ecosystem indexes as quality guarantees.

## Full Skill Output Contract

A generated full skill must include:

- its own identity
- its own iteration rules
- its own reference registry
- project bootstrap protocols
- experience harvesting protocol
- project-level context templates
- project-level skill template
- review policy template
- eval policy template
- experience capture template

The full skill must be able to initialize a target project without reading the seed.

## Seed Update Policy

Update the seed only for:

- source allowlist corrections
- generation contract corrections
- seed/full-skill boundary clarifications
- blueprint synchronization
- security or privacy boundary improvements

Do not promote ordinary full-skill operational lessons into seed core unless they affect seed generation itself.

## Full Skill Blueprint Policy

`full-skill/` is a blueprint, not seed runtime.

It may be updated to show the current expected output shape.

A generated real full skill should be written to a separate path, such as:

```text
~/.codex/skills/self-evolving-project-bootstrap/
```

or a user-specified target directory.

## Offline Rule

If network access is unavailable:

1. Use seed core files.
2. Use the local `full-skill/` blueprint.
3. Mark external references as not refreshed.
4. Avoid claiming that current external sources were verified.

## Anti-Drift Rules

The seed must not drift into:

- a generic coding guide
- a generic project-management framework
- a full project-bootstrap runtime
- a permanent managed-project registry
- an autonomous background service
- a hidden memory system

The full skill may be operational and expandable. The seed must stay minimal.

## Validation Checklist

After a seed update, verify:

- the seed still has exactly three operational core files
- the seed still generates a separate full skill
- no `generated/` runtime layer is required inside the seed
- approved sources remain explicit in `PROJECT_REFERENCES.md`
- `full-skill/` is documented as blueprint/output shape

After full-skill generation, verify:

- the full skill has its own `SKILL.md`
- the full skill can bootstrap project-level agent context
- the full skill has protocols and templates
- the full skill does not depend on seed files
- the target path is recorded if requested
