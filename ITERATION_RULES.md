# Iteration Rules

## Purpose

These rules define two different lifecycles:

- Seed completion rules: how the seed grows into a full central project-bootstrap skill.
- Full skill iteration rules: how the completed central skill improves after use across projects.

In seed-only packaging, keep this file as protocol. Do not generate the full support directories unless the user explicitly asks to complete the seed.

## A. Seed Completion Rules

### Completion Target

The seed must grow into a full central skill with these generated directories:

- `templates/`
- `schemas/`
- `policies/`
- `scripts/`
- `docs/`

The generated full central skill must be able to initialize, adopt, refresh, and reconstruct project-level agent context environments.

### Completion Inputs

Use sources in this order:

1. Core seed files.
2. Current user instructions.
3. `PROJECT_REFERENCES.md`.
4. Managed project experience.
5. Trusted local projects.
6. External reference repositories.
7. Public documentation.

If a source tier is empty or unavailable, record that gap instead of inventing unsupported conventions.

### Completion Procedure

1. Inspect the current skill directory and classify it as seed state or full central skill state.
2. Read `PROJECT_REFERENCES.md` and list available evidence sources.
3. Inspect trusted local references only when they are explicitly listed or discoverable from trusted local configuration.
4. Generate the full central skill directories.
5. Generate project initialization templates.
6. Generate project adoption, refresh, and reconstruction policies.
7. Generate schemas for project registry, feedback events, iteration reports, and skill updates.
8. Generate scripts for project inspection, project context generation, experience collection, central summary, and validation.
9. Generate architecture and update protocol docs.
10. Run validation.
11. Output a completion report describing generated files, evidence used, unresolved gaps, and next safe action.

### Completion Outputs

Generate at minimum:

- `templates/AGENTS.md.template`
- `templates/project-context-evolution.SKILL.md.template`
- `templates/SYSTEM_PURPOSE.md.template`
- `templates/CONTEXT_MAP.md.template`
- `templates/WORKFLOW.md.template`
- `templates/REVIEW_POLICY.md.template`
- `templates/EVAL_POLICY.md.template`
- `templates/ITERATION_LOG.md.template`
- `schemas/project_registry.schema.json`
- `schemas/feedback_event.schema.json`
- `schemas/iteration_report.schema.json`
- `schemas/skill_update.schema.json`
- `policies/bootstrap_policy.md`
- `policies/adoption_policy.md`
- `policies/refresh_policy.md`
- `policies/reconstruction_policy.md`
- `policies/risk_policy.md`
- `policies/anti_drift_policy.md`
- `policies/evidence_policy.md`
- `scripts/inspect_project.py`
- `scripts/generate_project_context.py`
- `scripts/collect_project_experience.py`
- `scripts/summarize_managed_projects.py`
- `scripts/validate_central_skill.py`
- `docs/CENTRAL_SKILL_ARCHITECTURE.md`
- `docs/GENERATED_FILE_MAP.md`
- `docs/UPDATE_PROTOCOL.md`

### Core Retention Rules

Keep these responsibilities in the core files:

- `SKILL.md`: identity, state detection, target structure, primary operation, boundaries.
- `ITERATION_RULES.md`: seed completion protocol, full iteration protocol, validation standard.
- `PROJECT_REFERENCES.md`: evidence source index and project registry.

Put generated implementation details in support directories. Do not bury the seed identity inside generated files.

### Completion Constraints

The generated full central skill must preserve:

- Seed identity.
- Project-level independence.
- `AGENTS.md` as a canonical project entry point.
- Review boundaries.
- Rollback requirements.
- Experience harvesting.
- Anti-drift checks.
- Evidence-based updates.

### Validation Standard

The full central skill is valid only if it can:

1. Initialize a project with no existing agent context.
2. Create a project-level `AGENTS.md`.
3. Create a project-level self-iteration skill.
4. Create experience capture files.
5. Create review and eval policies.
6. Register the project.
7. Explain how future agents can continue in the project without the central skill.

### Stop Conditions

Stop before completion when:

- The user explicitly asks for seed form only.
- Required external evidence needs user approval or credentials.
- A referenced project or repository cannot be accessed.
- Validation would require modifying a target project the user has not named.

In these cases, keep the seed intact and report what remains unresolved.

## B. Full Skill Iteration Rules

Use these rules only after the central skill has completed itself.

Update the full central skill from repeated evidence gathered across managed projects. Prefer recurring patterns over one-off project quirks.

During full iteration:

1. Collect experience from initialized or adopted projects.
2. Compare project-level outcomes against current templates, policies, schemas, and scripts.
3. Identify reusable improvements.
4. Update generated support files before changing core seed files.
5. Keep project-level contexts independently usable.
6. Run central validation.
7. Record the iteration report.

Do not import project-specific preferences into central policy unless they generalize across projects or the user explicitly promotes them.

## Anti-Drift Checks

Before any seed completion or full iteration, verify:

- The two-stage bootstrap remains intact.
- The seed has not become a project initializer directly.
- The central skill does not make target projects dependent on itself after initialization.
- Generated files preserve rollback, review, evidence, and validation requirements.
- Missing evidence is marked as missing instead of silently replaced with assumptions.
