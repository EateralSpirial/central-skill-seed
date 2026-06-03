# Project Context Bootstrap Protocol

## Purpose

This protocol defines how to initialize, adopt, refresh, reconstruct, or audit a target project's agent context environment.

## Precondition

If the central generated layer is missing or incomplete, run Self-Build Mode first.

## Operation Modes

### Initialize

Use when the project has no agent context.

### Adopt

Use when the user asks this central skill to take over an existing project.

### Refresh

Use when project context exists but needs updates.

### Reconstruct

Use when project context is noisy, contradictory, stale, or structurally weak.

### Audit

Use when the user asks whether the project context is usable.

## Procedure

### Step 1. Inspect Project Shape

Identify:

- project name
- local path
- primary language
- framework
- package manager
- build system
- test runner
- lint command
- typecheck command
- app entry points
- deployment surface
- docs
- scripts
- configuration files
- existing agent instructions
- existing `.agent/` or `.codex/` directories

### Step 2. Infer Project Agent Needs

Determine what future coding agents need:

- setup commands
- test commands
- build commands
- safe-edit rules
- architecture boundaries
- file ownership boundaries
- generated-file rules
- secret-handling rules
- eval rules
- review rules
- project context update rules

### Step 3. Preserve Existing Valid Context

If existing rules exist:

- preserve useful local knowledge
- remove duplication
- resolve contradictions
- archive obsolete instructions where appropriate
- avoid destroying project-specific conventions

### Step 4. Generate AGENTS.md

Create or update `AGENTS.md`.

Keep it concise.

Include pointers to `.agent/` for detailed rules.

### Step 5. Generate .agent/project

Create:

- `.agent/project/SYSTEM_PURPOSE.md`
- `.agent/project/CONTEXT_MAP.md`
- `.agent/project/WORKFLOW.md`
- `.agent/project/ITERATION_RULES.md`

### Step 6. Generate Project-Level Skill

Create:

- `.agent/skills/project-context-evolution/SKILL.md`

This skill must preserve future self-iteration ability without depending on the central skill.

### Step 7. Generate Experience Files

Create:

- `.agent/experience/LESSONS.md`
- `.agent/experience/FAILURE_PATTERNS.md`
- `.agent/experience/USER_CORRECTIONS.md`

### Step 8. Generate Iteration Files

Create:

- `.agent/iteration/ITERATION_LOG.md`
- `.agent/iteration/CHANGE_PROPOSALS.md`
- `.agent/iteration/REVIEW_POLICY.md`

### Step 9. Generate Eval Files

Create:

- `.agent/evals/REGRESSION_CASES.md`
- `.agent/evals/EVAL_POLICY.md`

### Step 10. Register Project

Update central `PROJECT_REFERENCES.md` unless the user asks not to.

### Step 11. Completion Report

Report:

- files created
- files updated
- rules installed
- missing information
- unresolved risks
- suggested next action

## Safety Rules

Do not:

- delete existing files without explicit approval
- overwrite useful project-specific context
- store secrets
- create permanent dependency on the central skill
- enable autonomous high-risk rewrites
- hide detailed rules outside the project

## Success Criteria

The project can now guide future coding agents using its own files.
