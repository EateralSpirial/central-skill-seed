---
name: self-evolving-project-bootstrap
description: A seed skill that first self-builds a complete central skill support layer from reference projects, then bootstraps independent self-evolving project-level agent context environments.
---

# Self-Evolving Project Bootstrap Skill

## Core Identity

This is a central seed skill with two execution modes:

1. **Self-Build Mode**
2. **Project Context Bootstrap Mode**

The seed has exactly three authoritative core files:

- `SKILL.md`
- `ITERATION_RULES.md`
- `PROJECT_REFERENCES.md`

When executed in Self-Build Mode, the agent expands this seed into a full central skill support layer under `generated/`.

When executed in Project Context Bootstrap Mode, the agent initializes or reconstructs a target project's agent context environment so that future coding agents can keep improving that project context without depending on this central skill.

## Non-Negotiable Purpose

This skill exists to create **independent, project-level, self-evolving agent context systems**.

A project initialized by this skill must continue functioning after this central skill is removed, unavailable, or never referenced again.

The target project must receive its own:

- `AGENTS.md`
- project purpose file
- context map
- workflow rules
- iteration rules
- project-level context evolution skill
- experience logs
- failure pattern logs
- review policy
- eval policy
- regression case file
- change proposal log

## Mode A: Self-Build Mode

Use Self-Build Mode when any of these are true:

- this central skill has only its three core seed files
- `generated/` is missing
- `generated/` is incomplete
- `generated/` is stale
- the user asks to build, rebuild, refresh, improve, or complete this central skill
- the user asks to incorporate open-source reference projects into this skill
- managed project experience should be summarized back into the central skill

Self-Build Mode must:

1. Read `SKILL.md`.
2. Read `ITERATION_RULES.md`.
3. Read `PROJECT_REFERENCES.md`.
4. Inspect existing `generated/` files if present.
5. Consult the mandatory external references in `PROJECT_REFERENCES.md`.
6. Extract reusable structures, safety boundaries, templates, and iteration patterns.
7. Generate or refresh the central support layer under `generated/`.
8. Validate the generated layer against this skill's invariants.
9. Record the run in `generated/SELF_BUILD_REPORT.md`.
10. Update `PROJECT_REFERENCES.md` when reference status, managed project entries, reusable lessons, or self-build history changes.

Self-Build Mode must create or update:

- `generated/REFERENCE_DIGEST.md`
- `generated/SELF_BUILD_PROTOCOL.md`
- `generated/PROJECT_BOOTSTRAP_PROTOCOL.md`
- `generated/PROJECT_CONTEXT_TEMPLATE/`
- `generated/PROJECT_SKILL_TEMPLATE/`
- `generated/EVAL_POLICY_TEMPLATE.md`
- `generated/EXPERIENCE_CAPTURE_TEMPLATE.md`
- `generated/REVIEW_POLICY_TEMPLATE.md`
- `generated/SELF_BUILD_REPORT.md`

The generated support layer is rebuildable. The three core seed files remain authoritative.

## Mode B: Project Context Bootstrap Mode

Use Project Context Bootstrap Mode when any of these are true:

- the target project has no `AGENTS.md`
- the target project has no project-level agent context environment
- the target project has scattered or contradictory agent instructions
- the user asks this skill to initialize a project
- the user asks this skill to adopt or take over a project
- the user asks this skill to refresh, audit, or reconstruct a project-level context
- a project-level context exists but has drifted, become stale, or lost its self-iteration ability

Project Context Bootstrap Mode must:

1. Ensure the central support layer exists.
2. If the generated layer is missing or incomplete, run Self-Build Mode first.
3. Inspect the target project.
4. Infer project language, framework, package manager, commands, architecture boundaries, and risk surfaces.
5. Preserve existing valid project-specific rules.
6. Remove or quarantine contradictions.
7. Generate or update `AGENTS.md`.
8. Generate or update `.agent/`.
9. Generate the project-level `project-context-evolution` skill.
10. Create experience, iteration, review, and eval files.
11. Register the project in `PROJECT_REFERENCES.md`.
12. Produce a completion report.

## Execution Order

If `generated/` is missing, stale, or incomplete, Self-Build Mode must run before Project Context Bootstrap Mode.

Project Context Bootstrap Mode should use the generated protocols and templates when available.

## Mandatory External References

Self-Build Mode must inspect the mandatory external references listed in `PROJECT_REFERENCES.md`.

If network access is unavailable, Self-Build Mode must:

- record an offline fallback in `generated/SELF_BUILD_REPORT.md`
- clearly mark which references were not refreshed
- avoid pretending reference material was verified
- proceed only with local seed files and previously generated digests

## Target Project Outputs

When initializing or adopting a project, create or update the following where appropriate:

```text
AGENTS.md
.agent/
  project/
    SYSTEM_PURPOSE.md
    CONTEXT_MAP.md
    WORKFLOW.md
    ITERATION_RULES.md
  skills/
    project-context-evolution/
      SKILL.md
  experience/
    LESSONS.md
    FAILURE_PATTERNS.md
    USER_CORRECTIONS.md
  iteration/
    ITERATION_LOG.md
    CHANGE_PROPOSALS.md
    REVIEW_POLICY.md
  evals/
    REGRESSION_CASES.md
    EVAL_POLICY.md
```

`AGENTS.md` is the canonical project-level entry point for coding agents.

Detailed rules should live under `.agent/`, not inside a bloated `AGENTS.md`.

## Project-Level Independence Requirement

A target project initialized by this skill must be self-contained.

Future coding agents working in the project must be able to answer:

- what the project is for
- how to set it up
- how to test it
- how to modify it safely
- what not to modify
- where to record lessons
- how to update project rules
- how to add regression cases
- how to propose high-risk changes
- how to preserve the project's self-iteration ability

without reading this central skill.

## Operation Modes For Target Projects

### Initialize

Use when the target project has no agent context.

Create the full project-level context environment from scratch.

### Adopt

Use when the user asks this skill to take over an existing project.

Inspect existing docs, scripts, conventions, tests, agent files, and workflows. Preserve valid local rules. Consolidate them into a coherent project-level context.

### Refresh

Use when the target project already has a context system but needs updates.

Read existing `AGENTS.md`, `.agent/`, project-level skills, lessons, failure patterns, iteration logs, and eval files. Update minimally.

### Reconstruct

Use when project context is noisy, contradictory, stale, or structurally weak.

Extract durable principles, archive obsolete rules, rebuild context files, and create a migration note.

### Audit

Use when the user asks whether the project has a usable self-evolving agent context.

Inspect and report missing components, drift risks, stale commands, weak review rules, and missing eval coverage.

## Target Project AGENTS.md Principles

Generated `AGENTS.md` should be concise and operational.

It should include:

- project purpose
- setup commands
- test commands
- build commands
- lint/typecheck commands if available
- coding rules
- architecture boundaries
- agent workflow
- self-iteration requirement
- experience recording rule
- risk policy
- pointers to `.agent/`

It should not become a full handbook.

## Project-Level Skill Requirement

Every initialized or adopted project must receive:

```text
.agent/skills/project-context-evolution/SKILL.md
```

That skill must teach future coding agents how to:

- update project context
- update `AGENTS.md`
- record project lessons
- record repeated failure patterns
- add regression cases
- classify risky changes
- propose context updates
- preserve project self-iteration ability
- avoid depending on this central skill

## Experience Capture Requirement

Every initialized or adopted project must contain:

```text
.agent/experience/LESSONS.md
.agent/experience/FAILURE_PATTERNS.md
.agent/experience/USER_CORRECTIONS.md
```

Future agents must record durable, reusable project experience there.

Do not store secrets, credentials, sensitive user data, or private business details unless the user explicitly requests it.

## Eval Requirement

Every initialized or adopted project must contain:

```text
.agent/evals/REGRESSION_CASES.md
.agent/evals/EVAL_POLICY.md
```

Repeated agent failures should become regression cases.

User corrections that reveal systematic misunderstanding should become regression cases.

## Review And Risk Requirement

Every initialized or adopted project must contain:

```text
.agent/iteration/REVIEW_POLICY.md
.agent/iteration/CHANGE_PROPOSALS.md
.agent/iteration/ITERATION_LOG.md
```

At minimum, project changes must be classified as:

- low risk
- medium risk
- high risk

Low-risk changes may be applied directly.

Medium-risk changes require a written proposal.

High-risk changes require explicit user approval.

## Project Registration Requirement

Every project initialized, adopted, refreshed, reconstructed, or audited by this skill must be recorded in `PROJECT_REFERENCES.md` unless the user explicitly asks not to record it.

## Prohibited Behavior

This skill must not:

- create projects that permanently depend on this central skill
- hide project-specific rules only inside this central skill
- overwrite useful existing project rules without preserving them
- blindly copy external repositories
- create vague agent instructions
- create self-iteration rules with no review boundary
- allow autonomous high-risk project rewrites
- treat all user feedback as correct
- treat emotion classification as objective fact
- optimize only for short-term user appeasement
- collect secrets, credentials, or private data
- expand the core seed beyond the three core files without explicit user approval

## Success Standard

The minimum success standard is:

A project with no prior agent context can be initialized by this skill. After initialization, future coding agents can work in that project, update its agent context, record lessons, add regression cases, and preserve self-iteration ability without referencing this central skill.
