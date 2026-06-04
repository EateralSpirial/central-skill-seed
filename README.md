# 🌱 Central Skill Seed

`central-skill-seed` is a minimal seed skill. Its job is to generate a **separate full skill package**, not to grow a full skill inside itself.

## Architecture

```text
central-skill-seed/                  # seed skill; keep small
  README.md                          # repository documentation
  SKILL.md                           # seed entrypoint
  ITERATION_RULES.md                 # seed self-build rules
  PROJECT_REFERENCES.md              # source allowlist and registry
  full-skill/                        # blueprint of the separate full skill package the seed generates
    SKILL.md
    ITERATION_RULES.md
    PROJECT_REFERENCES.md
    protocols/
    templates/
```

## Core rule

The seed and the full skill are separate artifacts.

```text
seed skill
→ reads approved references
→ generates separate full skill package
→ full skill bootstraps project-level agent context
```

The seed must not treat `full-skill/` as its own generated runtime state. `full-skill/` is a repository blueprint and expected output shape. In actual use, the seed should generate the full skill into a distinct target directory, for example:

```text
~/.codex/skills/self-evolving-project-bootstrap/
```

or a user-specified output path.

## Seed core files

| File | Purpose |
| --- | --- |
| `SKILL.md` | Defines the seed identity and the separate full-skill generation workflow. |
| `ITERATION_RULES.md` | Defines how the seed updates itself and how it emits the full skill. |
| `PROJECT_REFERENCES.md` | Lists approved GitHub sources, generated full-skill targets, and managed project registries. |

Only these three files are operational seed core.

## Mandatory GitHub reference sources

The seed may use only approved sources listed in `PROJECT_REFERENCES.md`, including:

- `anthropics/skills` — https://github.com/anthropics/skills
- `agentskills/agentskills` — https://github.com/agentskills/agentskills
- Agent Skills specification — https://agentskills.io/specification
- `AGENTS.md` — https://agents.md
- OpenAI Codex `AGENTS.md` guide — https://developers.openai.com/codex/guides/agents-md
- `ShunsukeHayashi/agent-skill-bus` — https://github.com/ShunsukeHayashi/agent-skill-bus
- `alinaqi/maggy` — https://github.com/alinaqi/maggy
- `NeoLabHQ/context-engineering-kit` — https://github.com/NeoLabHQ/context-engineering-kit
- `VoltAgent/awesome-agent-skills` — https://github.com/VoltAgent/awesome-agent-skills

## Full skill output

The generated full skill should be an independent skill package named:

```text
self-evolving-project-bootstrap
```

It should contain its own `SKILL.md`, rules, protocols, templates, and project-bootstrap logic. It should not need the seed after generation.

## Why this split matters

The seed is stable and minimal. The full skill is operational and expandable.

This prevents the seed from becoming bloated, self-mutating, or confused with its own output.
