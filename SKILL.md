---
name: central-skill-seed
description: Generate the separate self-evolving-project-bootstrap full skill package from approved references and the local blueprint.
---

# central-skill-seed

## Purpose

`central-skill-seed` generates a separate full skill package named `self-evolving-project-bootstrap`.

It does not bootstrap projects directly and does not build a runtime layer inside itself.

## Canonical objects

| Object | Name | Responsibility |
| --- | --- | --- |
| Seed skill | `central-skill-seed` | Generate or update the full skill package. |
| Full skill | `self-evolving-project-bootstrap` | Initialize, adopt, refresh, reconstruct, and audit project-level agent context. |
| Project-level skill | `project-context-evolution` | Maintain one project's agent context after bootstrap. |

Use these names consistently.

## Seed core

The seed has exactly three operational core files:

```text
SKILL.md
ITERATION_RULES.md
PROJECT_REFERENCES.md
```

`README.md` and `full-skill/` are repository support materials.

## Primary action: generate full skill

Use this skill when the user asks to build, update, emit, or regenerate the full skill package.

Default output target:

```text
~/.codex/skills/self-evolving-project-bootstrap/
```

If the user provides another target path, use it.

When editing this repository, update `full-skill/` as the blueprint for that generated package.

## Full skill output contract

The generated `self-evolving-project-bootstrap` package must include:

```text
SKILL.md
ITERATION_RULES.md
PROJECT_REFERENCES.md
protocols/
templates/
```

It must be able to bootstrap a target project's agent context without reading `central-skill-seed`.

## Full skill responsibilities

`self-evolving-project-bootstrap` is responsible for creating or updating:

```text
AGENTS.md
.agent/project/
.agent/skills/project-context-evolution/SKILL.md
.agent/experience/
.agent/iteration/
.agent/evals/
```

These responsibilities belong to the full skill, not to the seed.

## Reference rule

Use only sources listed in `PROJECT_REFERENCES.md`, unless the user explicitly approves another source.

Extract structures, safeguards, and templates. Do not copy external repositories wholesale.

## Offline rule

If references cannot be checked online:

1. Use the seed core files.
2. Use the local `full-skill/` blueprint.
3. Mark references as not refreshed.
4. Do not claim verification.

## Prohibited behavior

Do not:

- create `generated/` as seed runtime state
- turn the seed into the full skill
- move full-skill operations into seed core
- store managed project registries in the seed
- introduce unapproved source repositories
- make the full skill depend on the seed after generation

## Success criteria

Success means a separate `self-evolving-project-bootstrap` package exists and can bootstrap project-level agent context independently.
