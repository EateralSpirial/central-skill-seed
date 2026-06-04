# Iteration Rules

## Purpose

These rules keep `central-skill-seed` small and make its output contract precise.

## Invariant

```text
central-skill-seed != self-evolving-project-bootstrap
```

The seed generates the full skill. The full skill performs project bootstrap.

## Allowed seed changes

Update the seed only for:

- reference allowlist changes
- generation contract changes
- seed/full-skill boundary clarification
- `full-skill/` blueprint synchronization
- security or privacy boundary fixes

Do not promote ordinary full-skill operating lessons into the seed unless they affect generation.

## Generation procedure

When generating or refreshing `self-evolving-project-bootstrap`:

1. Read seed `SKILL.md`.
2. Read seed `ITERATION_RULES.md`.
3. Read seed `PROJECT_REFERENCES.md`.
4. Inspect `full-skill/` as the local blueprint.
5. Inspect approved references when available.
6. Generate or update the full skill in a separate target path.
7. Verify the full skill has its own core files, protocols, and templates.
8. Verify the full skill does not depend on seed files.
9. Record the generated target in `PROJECT_REFERENCES.md` when useful.

## Approved reference extraction

Use only approved sources in `PROJECT_REFERENCES.md`.

Extract:

- skill package structure
- `SKILL.md` conventions
- `AGENTS.md` project-context conventions
- self-improvement loop patterns
- review and eval policy patterns
- context-engineering patterns

Do not extract:

- secrets
- credentials
- private project data
- large external files wholesale
- unverified security assumptions

## Blueprint policy

`full-skill/` is a blueprint for the generated package.

It may be updated when the desired full skill changes. It is not seed runtime state and must not contain managed project history.

## Offline rule

When network access is unavailable:

1. Use seed core files.
2. Use `full-skill/`.
3. Mark external references as not refreshed.
4. Avoid claiming source freshness.

## Validation checklist

Before finishing a seed update, verify:

- the seed still has exactly three operational core files
- object names are consistent
- there is no `generated/` seed runtime layer
- `full-skill/` remains a blueprint
- the full skill can exist independently
- approved sources remain explicit

Before finishing full-skill generation, verify:

- the package name is `self-evolving-project-bootstrap`
- it has `SKILL.md`, `ITERATION_RULES.md`, and `PROJECT_REFERENCES.md`
- it has project-bootstrap protocols and templates
- it can create `project-context-evolution` inside target projects
- it does not require `central-skill-seed`
