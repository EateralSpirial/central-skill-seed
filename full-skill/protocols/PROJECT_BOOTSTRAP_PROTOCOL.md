# Project Bootstrap Protocol

## Procedure

### Step 1. Inspect Project Shape

Identify:

- project name
- language
- framework
- package manager
- build command
- test command
- lint command
- typecheck command
- deployment surface
- existing docs
- existing agent instructions

### Step 2. Infer Agent Needs

Determine what future agents need to know:

- setup
- tests
- safe edit boundaries
- architecture map
- generated files
- secrets policy
- review policy
- eval policy

### Step 3. Generate Project Context

Create:

- `AGENTS.md`
- `.agent/project/`
- `.agent/skills/project-context-evolution/SKILL.md`
- `.agent/experience/`
- `.agent/iteration/`
- `.agent/evals/`

### Step 4. Validate Independence

Confirm future agents can maintain project context without reading this full skill.
