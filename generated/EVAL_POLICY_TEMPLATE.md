# Eval Policy Template

## Purpose

This file defines how project-level regression cases should be created and maintained.

## Eval Philosophy

Repeated failures should become regression cases.

User corrections that reveal durable expectations should become regression cases.

Regression cases should be small, concrete, and runnable or reviewable.

## Regression Case Format

```md
## Case: <short name>

Date:

Trigger:

Related files:

Input or scenario:

Expected behavior:

Forbidden behavior:

Validation method:

Risk level:

Status:
```

## When To Add A Regression Case

Add a case when:

- an agent repeats a mistake
- a user correction reveals a hard constraint
- a command changes and future agents may use the old one
- a generated artifact violates fixed requirements
- a bug fix should not regress
- project context was ambiguous and caused failure

## When Not To Add A Regression Case

Do not add a case for:

- one-off exploratory notes
- temporary debugging observations
- subjective preferences with no durable project value
- sensitive private data
- speculative concerns with no evidence
