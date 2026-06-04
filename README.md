# central-skill-seed

A minimal seed skill that generates a separate full skill package.

## Objects

| Object | Canonical name | Role |
| --- | --- | --- |
| Seed skill | `central-skill-seed` | Generates the full skill package. |
| Full skill | `self-evolving-project-bootstrap` | Bootstraps and maintains project-level agent context. |
| Project-level skill | `project-context-evolution` | Lets an initialized project maintain its own agent context. |

Do not use other names for these objects.

## Flow

```text
central-skill-seed
  -> generates self-evolving-project-bootstrap
    -> initializes project AGENTS.md and .agent/
      -> installs project-context-evolution
```

## Repository layout

```text
central-skill-seed/
  README.md
  SKILL.md
  ITERATION_RULES.md
  PROJECT_REFERENCES.md
  full-skill/                  # blueprint for the generated full skill
```

The seed has only three operational core files:

```text
SKILL.md
ITERATION_RULES.md
PROJECT_REFERENCES.md
```

`README.md` is documentation. `full-skill/` is the blueprint of the package the seed generates. It is not seed runtime state.

## Install target for the generated full skill

Default target:

```text
~/.codex/skills/self-evolving-project-bootstrap/
```

A user-specified path may override this default.

## Approved reference sources

The seed may use only sources listed in `PROJECT_REFERENCES.md`. Current approved sources include:

- https://github.com/anthropics/skills
- https://github.com/agentskills/agentskills
- https://agentskills.io/specification
- https://agents.md
- https://developers.openai.com/codex/guides/agents-md
- https://github.com/ShunsukeHayashi/agent-skill-bus
- https://github.com/alinaqi/maggy
- https://github.com/NeoLabHQ/context-engineering-kit
- https://github.com/VoltAgent/awesome-agent-skills

## Boundary rule

The seed stays small. The full skill is operational. Initialized projects must not depend on either one after their own `project-context-evolution` skill is installed.
