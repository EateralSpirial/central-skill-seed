---
name: central-skill-seed
description: Use when working with a seed skill that must first self-complete into a central project-bootstrap skill before initializing, adopting, refreshing, or reconstructing project-level agent context, AGENTS.md files, or project-level skills.
---

# Central Skill Seed

## Overview

This is a seed skill, not a complete central bootstrap system.

Its first responsibility is to complete itself into a full central project-bootstrap skill. Only after completion may the full central skill initialize, adopt, refresh, or reconstruct project-level agent context environments for other software projects.

## State Detection

Treat the skill as being in seed state when the only operational core files are:

- `SKILL.md`
- `ITERATION_RULES.md`
- `PROJECT_REFERENCES.md`

An optional `agents/openai.yaml` file may exist for UI metadata. It is not part of the operational seed protocol.

Treat the skill as being in full central skill state only when it also contains generated support directories and a validation protocol:

- `templates/`
- `schemas/`
- `policies/`
- `scripts/`
- `docs/`

In seed state, do not assume the central skill is complete. Run the seed completion procedure before using it to initialize any target project.

## Target Full Structure

The seed is intended to grow into a full central skill shaped like this:

```text
central-skill/
  SKILL.md
  ITERATION_RULES.md
  PROJECT_REFERENCES.md

  templates/
    AGENTS.md.template
    project-context-evolution.SKILL.md.template
    SYSTEM_PURPOSE.md.template
    CONTEXT_MAP.md.template
    WORKFLOW.md.template
    REVIEW_POLICY.md.template
    EVAL_POLICY.md.template
    ITERATION_LOG.md.template

  schemas/
    project_registry.schema.json
    feedback_event.schema.json
    iteration_report.schema.json
    skill_update.schema.json

  policies/
    bootstrap_policy.md
    adoption_policy.md
    refresh_policy.md
    reconstruction_policy.md
    risk_policy.md
    anti_drift_policy.md
    evidence_policy.md

  scripts/
    inspect_project.py
    generate_project_context.py
    collect_project_experience.py
    summarize_managed_projects.py
    validate_central_skill.py

  docs/
    CENTRAL_SKILL_ARCHITECTURE.md
    GENERATED_FILE_MAP.md
    UPDATE_PROTOCOL.md
```

This target structure describes the completed central skill. Do not create it when the user explicitly asks for the seed only.

## Primary Operation

When invoked in seed state:

1. Inspect the current skill directory.
2. Identify missing full-skill components.
3. Read `ITERATION_RULES.md`.
4. Read `PROJECT_REFERENCES.md`.
5. Collect only referenced and trustworthy evidence.
6. Generate missing central skill files.
7. Validate the generated central skill.
8. Produce a completion report.

When invoked in full central skill state:

1. Inspect the target project.
2. Generate or update project-level agent context.
3. Generate a project-level self-iteration skill.
4. Register the project.
5. Record reusable experience for later central-skill iteration.

## Completion Boundary

Preserve the two-stage bootstrap:

```text
seed -> full central skill -> project-level agent context
```

Do not collapse it into:

```text
central skill -> project-level agent context
```

The seed's job is controlled self-completion. The completed central skill's job is project initialization and project context evolution.

## Anti-Drift Rules

- Keep the seed small and stable.
- Keep identity, goals, boundaries, completion rules, reference sources, validation standards, and anti-drift constraints in the three core files.
- Move implementation details into generated `templates/`, `schemas/`, `policies/`, `scripts/`, and `docs/` only during full completion.
- Do not treat one project's local habit as a central rule without evidence.
- Do not generate project-level context from the seed before completing the central skill.
- If the user asks for seed form only, stop after maintaining the core seed files.
