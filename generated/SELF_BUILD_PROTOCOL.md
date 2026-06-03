# Self-Build Protocol

## Purpose

This protocol defines how the central seed skill expands or refreshes itself.

## Inputs

Required:

- `SKILL.md`
- `ITERATION_RULES.md`
- `PROJECT_REFERENCES.md`

Optional:

- existing `generated/`
- managed project entries
- managed project `.agent/` directories
- external references
- trusted local projects from `.codex/config.toml`

## Procedure

### Step 1. Load Core Seed

Read:

- `SKILL.md`
- `ITERATION_RULES.md`
- `PROJECT_REFERENCES.md`

Identify:

- core invariants
- current execution modes
- required generated files
- mandatory external references
- managed project registry

### Step 2. Check Generated Layer

Inspect whether these exist:

- `generated/REFERENCE_DIGEST.md`
- `generated/SELF_BUILD_PROTOCOL.md`
- `generated/PROJECT_BOOTSTRAP_PROTOCOL.md`
- `generated/PROJECT_CONTEXT_TEMPLATE/`
- `generated/PROJECT_SKILL_TEMPLATE/`
- `generated/EVAL_POLICY_TEMPLATE.md`
- `generated/EXPERIENCE_CAPTURE_TEMPLATE.md`
- `generated/REVIEW_POLICY_TEMPLATE.md`
- `generated/SELF_BUILD_REPORT.md`

Classify state:

- missing
- incomplete
- stale
- coherent

### Step 3. Refresh External References

When network access is available, inspect mandatory external references listed in `PROJECT_REFERENCES.md`.

For each reference, extract:

- relevant structures
- relevant safeguards
- relevant iteration patterns
- relevant anti-drift rules
- relevant template ideas

Do not copy large text.

If network access is unavailable, record offline fallback.

### Step 4. Inspect Managed Projects

Read managed project entries from `PROJECT_REFERENCES.md`.

For each available managed project, inspect:

- `AGENTS.md`
- `.agent/project/`
- `.agent/skills/project-context-evolution/SKILL.md`
- `.agent/experience/`
- `.agent/iteration/`
- `.agent/evals/`

Extract only generalizable lessons.

### Step 5. Generate Or Refresh Support Layer

Create or update:

- reference digest
- self-build protocol
- project bootstrap protocol
- project context templates
- project-level skill template
- eval policy template
- experience capture template
- review policy template
- self-build report

### Step 6. Validate

Verify:

- generated layer preserves the two execution modes
- generated layer preserves project independence
- generated layer is subordinate to core files
- generated project templates produce a self-evolving project context
- no sensitive data was imported
- no external project content was copied wholesale
- review and risk boundaries remain explicit

### Step 7. Record Self-Build Run

Update `generated/SELF_BUILD_REPORT.md`.

If needed, update `PROJECT_REFERENCES.md` under Self-Build History.

## Failure Handling

If self-build fails:

- preserve partial output
- record what succeeded
- record missing references or inaccessible files
- do not claim completion
