# Review Policy Template

## Purpose

This file defines project-level risk categories and review requirements for agent changes.

## Risk Levels

### Low Risk

May be applied directly.

Examples:

- typo fixes
- comments
- documentation clarifications
- small tests
- adding regression cases
- updating stale file paths
- adding non-invasive logging

### Medium Risk

Requires a written change proposal before or alongside implementation.

Examples:

- changing workflow rules
- changing module boundaries
- adding dependencies
- modifying shared utilities
- changing data schemas
- changing default behavior
- updating eval policy

Requirements:

- write proposal in `.agent/iteration/CHANGE_PROPOSALS.md`
- explain problem, evidence, files affected, test plan, rollback plan
- run relevant tests

### High Risk

Requires explicit user approval.

Examples:

- changing project purpose
- major architecture rewrite
- deleting significant files or history
- modifying security or auth behavior
- changing deployment behavior
- changing privacy/data collection behavior
- enabling autonomous high-risk rewrites
- removing review gates

Requirements:

- do not implement without approval
- provide architecture note
- provide rollback plan
- identify alternatives

## Change Proposal Format

```md
## Proposal: <short title>

Date:

Problem:

Evidence:

Risk level:

Proposed change:

Files affected:

Alternatives:

Test plan:

Rollback plan:

Decision:
```
