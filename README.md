# 🌱 Self-Evolving Project Bootstrap Skill

A three-file central seed skill that can first complete itself into a full central skill support layer, then initialize independent self-evolving agent context environments for software projects.

## Core idea

```text
three-file seed
-> generated central support layer
-> project-level AGENTS.md + .agent/
-> future coding agents keep the project context evolving without depending on this central skill
```

## Two execution modes

### 1. Self-Build Mode

Use this when the central skill is incomplete, stale, or still only a seed. The agent reads the three core files and the mandatory GitHub reference projects, then generates or refreshes `generated/`.

### 2. Project Context Bootstrap Mode

Use this when a target project has no `AGENTS.md`, no `.agent/` context, or a stale/contradictory agent context. The skill creates a project-level context environment that remains independent after this central skill is removed.

## Core seed files

| File | Purpose |
| --- | --- |
| `SKILL.md` | Defines identity, execution modes, target outputs, and invariants. |
| `ITERATION_RULES.md` | Defines how the central skill self-builds and evolves from managed project experience. |
| `PROJECT_REFERENCES.md` | Lists mandatory GitHub references, managed projects, reusable lessons, and self-build history. |

## Mandatory GitHub reference projects

The current source allowlist is explicit and repository-level:

- `anthropics/skills` — https://github.com/anthropics/skills
- `agentskills/agentskills` — https://github.com/agentskills/agentskills
- Agent Skills specification — https://agentskills.io/specification
- `AGENTS.md` — https://agents.md
- OpenAI Codex `AGENTS.md` guide — https://developers.openai.com/codex/guides/agents-md
- `ShunsukeHayashi/agent-skill-bus` — https://github.com/ShunsukeHayashi/agent-skill-bus
- `alinaqi/maggy` — https://github.com/alinaqi/maggy
- `NeoLabHQ/context-engineering-kit` — https://github.com/NeoLabHQ/context-engineering-kit
- `VoltAgent/awesome-agent-skills` — https://github.com/VoltAgent/awesome-agent-skills

The skill may extract structures, protocols, safeguards, and templates from these sources. It must not copy external repositories wholesale.

## Generated layer

`generated/` is rebuildable operational support. It contains protocols and templates used by the central skill after Self-Build Mode:

```text
generated/
  REFERENCE_DIGEST.md
  SELF_BUILD_PROTOCOL.md
  PROJECT_BOOTSTRAP_PROTOCOL.md
  PROJECT_CONTEXT_TEMPLATE/
  PROJECT_SKILL_TEMPLATE/
  EVAL_POLICY_TEMPLATE.md
  EXPERIENCE_CAPTURE_TEMPLATE.md
  REVIEW_POLICY_TEMPLATE.md
  SELF_BUILD_REPORT.md
```

## Project bootstrap output

A target project initialized by this skill should receive:

```text
AGENTS.md
.agent/project/SYSTEM_PURPOSE.md
.agent/project/CONTEXT_MAP.md
.agent/project/WORKFLOW.md
.agent/project/ITERATION_RULES.md
.agent/skills/project-context-evolution/SKILL.md
.agent/experience/LESSONS.md
.agent/experience/FAILURE_PATTERNS.md
.agent/experience/USER_CORRECTIONS.md
.agent/iteration/ITERATION_LOG.md
.agent/iteration/CHANGE_PROPOSALS.md
.agent/iteration/REVIEW_POLICY.md
.agent/evals/REGRESSION_CASES.md
.agent/evals/EVAL_POLICY.md
```

## Core invariant

A target project must be able to continue agent-context iteration without this central skill.

## License

No license has been selected yet.
