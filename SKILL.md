---
name: central-skill-seed
description: A minimal seed skill that generates a separate full self-evolving project bootstrap skill package, rather than building the full skill inside itself.
---

# Central Skill Seed

## Core Identity

This is a **seed skill**.

Its job is to generate a separate, complete skill package.

It must not turn itself into the full skill.

The full skill it generates is expected to be named:

```text
self-evolving-project-bootstrap
```

## Core Separation Rule

The seed and the full skill are separate artifacts.

```text
central-skill-seed
→ generates self-evolving-project-bootstrap
→ self-evolving-project-bootstrap initializes project-level agent context
```

The seed remains small. The full skill becomes operational.

The seed must not store its full runtime under `generated/` inside itself.

## Seed Core Files

The seed has exactly three operational core files:

- `SKILL.md`
- `ITERATION_RULES.md`
- `PROJECT_REFERENCES.md`

Repository documentation and `full-skill/` blueprints are not seed core.

## Execution Mode A: Generate Full Skill

Use this mode when:

- the user asks to build, complete, emit, or regenerate the full skill
- the full skill does not exist yet
- the full skill exists but is stale
- approved external references changed
- managed full-skill or project experience should be incorporated into a new full-skill version

### Output Target

The full skill must be generated into a separate target directory.

Preferred default target:

```text
~/.codex/skills/self-evolving-project-bootstrap/
```

If the user specifies another path, use that path.

If working only inside this repository, update the blueprint under:

```text
full-skill/
```

but do not treat that blueprint as seed runtime state.

### Required Full Skill Contents

The generated full skill must contain at least:

```text
self-evolving-project-bootstrap/
  SKILL.md
  ITERATION_RULES.md
  PROJECT_REFERENCES.md
  protocols/
    SELF_UPDATE_PROTOCOL.md
    PROJECT_BOOTSTRAP_PROTOCOL.md
    EXPERIENCE_HARVEST_PROTOCOL.md
  templates/
    project-context/
      AGENTS.md.template
      SYSTEM_PURPOSE.md.template
      CONTEXT_MAP.md.template
      WORKFLOW.md.template
      ITERATION_RULES.md.template
    project-skill/
      SKILL.md.template
    EVAL_POLICY_TEMPLATE.md
    EXPERIENCE_CAPTURE_TEMPLATE.md
    REVIEW_POLICY_TEMPLATE.md
```

### Generation Procedure

1. Read the seed core files.
2. Read `PROJECT_REFERENCES.md` and extract the approved source allowlist.
3. Inspect mandatory GitHub references when network access is available.
4. Extract reusable structures, safeguards, and protocols.
5. Generate the separate full skill package.
6. Validate that the full skill does not depend on this seed.
7. Record the generated target path in `PROJECT_REFERENCES.md`.
8. Report created or updated files.

## Execution Mode B: Update Seed

Use this mode only when:

- the user explicitly asks to update the seed
- the seed's approved sources need correction
- the seed/full-skill separation rule needs clarification
- the full-skill blueprint must be updated to match the generation contract

Seed updates must stay minimal.

Do not move full-skill operational content back into seed core.

## What The Full Skill Does

The full skill, once generated, is responsible for:

- initializing project-level `AGENTS.md`
- creating `.agent/project/`
- creating a project-level context-evolution skill
- creating experience capture files
- creating review and eval policies
- registering managed projects
- harvesting reusable experience from managed projects
- updating itself from evidence

Those responsibilities belong to the generated full skill, not to the seed.

## Mandatory External References

When generating the full skill, use only references listed in `PROJECT_REFERENCES.md`.

If network access is unavailable:

- use local seed files
- use the local `full-skill/` blueprint if present
- record the offline fallback
- do not claim unverified references were refreshed

## Prohibited Behavior

The seed must not:

- build a `generated/` runtime layer inside itself
- become the full project-bootstrap skill
- permanently store managed project experience inside seed core
- copy external repositories wholesale
- invent reference sources that are not in `PROJECT_REFERENCES.md`
- make generated full skills depend on the seed after creation
- expand beyond the three operational core files without explicit user approval

## Success Criteria

The seed succeeds when it can emit a separate, self-contained full skill package that can initialize and maintain project-level agent context without referencing this seed.
