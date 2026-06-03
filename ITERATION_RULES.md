# Iteration Rules

## Purpose

This file defines how the central seed skill constructs, updates, and protects itself.

This skill evolves through two loops:

1. **Central Skill Self-Build Loop**
2. **Managed Project Experience Loop**

The first loop expands the three-file seed into a complete generated support layer.

The second loop extracts reusable lessons from projects initialized, adopted, refreshed, reconstructed, or audited by this skill.

## Core Invariant

This skill must remain:

```text
a central seed skill for creating independent self-evolving project-level agent context systems
```

Any change that weakens that identity is invalid.

## Three-File Core Invariant

The core seed consists of exactly three core text files:

- `SKILL.md`
- `ITERATION_RULES.md`
- `PROJECT_REFERENCES.md`

The generated support layer may contain many files, but it is subordinate and rebuildable.

Adding a fourth core file requires explicit user approval.

## Self-Build Loop

When Self-Build Mode is invoked, the agent must:

1. Read `SKILL.md`.
2. Read `ITERATION_RULES.md`.
3. Read `PROJECT_REFERENCES.md`.
4. Inspect existing `generated/` files if present.
5. Inspect mandatory external references when network access is available.
6. Read managed project entries from `PROJECT_REFERENCES.md`.
7. Inspect managed project context files where available.
8. Extract reusable structures, protocols, and failure controls.
9. Generate or update the central support layer under `generated/`.
10. Validate the generated layer against core invariants.
11. Record the run in `generated/SELF_BUILD_REPORT.md`.
12. Update `PROJECT_REFERENCES.md` only when project entries, reference statuses, reusable lessons, or self-build history need to change.

## Mandatory Reference Extraction

Self-Build Mode must inspect or refresh knowledge from these reference categories.

### Agent Skills Format

Use:

- `anthropics/skills`
- `agentskills/agentskills`
- `agentskills.io`

Extract:

- skill folder structure
- `SKILL.md` role
- metadata conventions
- progressive disclosure patterns
- bundled scripts/resources/templates
- cross-agent compatibility concerns

### Project-Level Agent Context

Use:

- `AGENTS.md`
- OpenAI Codex `AGENTS.md` guide

Extract:

- `AGENTS.md` as canonical project-level entry
- setup/test/style/workflow conventions
- instruction layering behavior
- concise project onboarding principles

### Skill Runtime And Self-Improvement

Use:

- `ShunsukeHayashi/agent-skill-bus`

Extract:

- skill execution logging
- health scoring
- drift detection
- self-improvement loop
- record-run pattern
- low-risk repair vs high-risk approval distinction
- knowledge watcher concept

### Engineering Harness

Use:

- `alinaqi/maggy`
- former reference name: Claude Bootstrap + Maggy

Extract:

- installable coding-agent configuration packs
- skills/hooks/rules/templates/evals organization
- quality gates
- ADR and review workflows
- memory organization
- dashboard and routing concepts
- test enforcement patterns

### Context Engineering

Use:

- `NeoLabHQ/context-engineering-kit`

Extract:

- token-efficient context layout
- plugin-oriented skills
- reflexion and review workflows
- granular context loading
- quality-focused context design
- cross-client compatibility

### Ecosystem Survey

Use:

- `VoltAgent/awesome-agent-skills`

Extract:

- common skill categories
- naming patterns
- ecosystem coverage
- candidate repositories for later review

Do not treat ecosystem indexes as quality guarantees.

## Source Use Rules

The agent may extract:

- directory structure ideas
- file naming conventions
- project initialization procedures
- review policies
- eval patterns
- skill health concepts
- self-improvement loop structures
- context compression patterns
- drift detection ideas
- registry patterns

The agent must not extract:

- secrets
- credentials
- copyrighted large text
- private project data
- large external systems copied wholesale
- unverified security assumptions
- patterns that make target projects permanently dependent on external tools

## Offline Self-Build Rule

If external references cannot be checked due to lack of network access, the agent must:

1. Use the local seed files.
2. Use existing `generated/REFERENCE_DIGEST.md` if available.
3. Record an offline fallback in `generated/SELF_BUILD_REPORT.md`.
4. Mark every unrefreshed reference explicitly.
5. Avoid claiming that external references were verified.

## Generated Layer Policy

The generated layer is operational support.

It may include:

- protocols
- digests
- templates
- reports
- checklists
- project bootstrap materials

It must remain subordinate to the three core files.

If a generated file conflicts with a core file, the core file wins.

## Managed Project Experience Loop

When managed project experience exists, the agent may update the generated central support layer by inspecting:

- target project `AGENTS.md`
- `.agent/project/`
- `.agent/skills/project-context-evolution/SKILL.md`
- `.agent/experience/LESSONS.md`
- `.agent/experience/FAILURE_PATTERNS.md`
- `.agent/experience/USER_CORRECTIONS.md`
- `.agent/iteration/ITERATION_LOG.md`
- `.agent/iteration/CHANGE_PROPOSALS.md`
- `.agent/evals/REGRESSION_CASES.md`
- `.agent/evals/EVAL_POLICY.md`

Extract only generalizable lessons.

Project-specific facts must remain in the project.

## Lesson Promotion Rule

A project lesson may be promoted into this central skill only if at least one condition is true:

- it appears in multiple managed projects
- it fixes repeated context drift
- it improves project-level independence
- it clarifies risk boundaries
- it improves eval or regression policy
- it improves rollback quality
- it improves initialization accuracy
- the user explicitly asks to promote it

## Emotional Feedback Rule

User emotion may be used as a signal for:

- friction
- violated expectation
- repeated agent failure
- project context ambiguity
- workflow mismatch
- missing regression coverage
- missing review boundary

Emotion must not be treated as objective truth.

Emotion must not be used to manipulate users.

Strong negative emotion should trigger:

- failure classification
- context review
- regression case creation
- rule clarification
- possible project-level skill update

Strong positive emotion should trigger:

- lesson preservation
- pattern extraction
- template improvement if generalizable

## Self-Modification Risk Policy

### Low Risk

May be applied directly:

- wording clarification
- typo fix
- formatting cleanup
- missing checklist item
- improved file path description
- reference digest refresh
- generated template clarification

### Medium Risk

Requires a written update proposal:

- new generated file type
- new bootstrap protocol
- changed project initialization procedure
- changed reference extraction method
- changed project-level context component
- changed review policy

### High Risk

Requires explicit user approval:

- changing the core purpose
- increasing the core file count
- removing project independence requirement
- removing `AGENTS.md` as canonical project entry
- allowing automatic high-risk project rewrites
- storing sensitive project data
- making target projects depend permanently on this central skill
- replacing the two-mode execution model

## Anti-Drift Rules

This skill must not drift toward:

- generic software engineering advice
- generic project management theory
- generic prompt engineering advice
- autonomous self-modifying agent ideology
- uncontrolled self-modification
- user emotion optimization as the sole objective
- hidden memory accumulation
- permanent project dependency
- blind copying of open-source skill packs

## Validation Checklist For Self-Build

After each Self-Build run, verify:

- the two execution modes are preserved
- the three-file core invariant is preserved
- the generated layer exists
- the generated layer is rebuildable
- mandatory references were considered or offline fallback was recorded
- project templates create independent project-level contexts
- managed project registry remains intact
- risk boundaries remain explicit
- no sensitive data was imported
- no external project was copied wholesale
- `SELF_BUILD_REPORT.md` was updated

## Validation Checklist For Project Bootstrap

After each Project Context Bootstrap run, verify the target project has:

- `AGENTS.md`
- `.agent/project/SYSTEM_PURPOSE.md`
- `.agent/project/CONTEXT_MAP.md`
- `.agent/project/WORKFLOW.md`
- `.agent/project/ITERATION_RULES.md`
- `.agent/skills/project-context-evolution/SKILL.md`
- `.agent/experience/LESSONS.md`
- `.agent/experience/FAILURE_PATTERNS.md`
- `.agent/experience/USER_CORRECTIONS.md`
- `.agent/iteration/ITERATION_LOG.md`
- `.agent/iteration/CHANGE_PROPOSALS.md`
- `.agent/iteration/REVIEW_POLICY.md`
- `.agent/evals/REGRESSION_CASES.md`
- `.agent/evals/EVAL_POLICY.md`

Also verify:

- the target project can operate without this central skill
- the target project has explicit risk boundaries
- the target project records agent experience
- repeated failures can become regression cases
- future agents know how to update project context

## Scheduled Update Reality Check

This skill is not a daemon.

Periodic self-update works only when one of the following invokes it:

- user request
- coding-agent run
- external scheduler
- CI job
- local script
- project-level workflow trigger

The skill must not claim it can update itself in the background without invocation.
