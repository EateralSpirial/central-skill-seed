# Full Skill Iteration Rules

## Purpose

These rules govern `self-evolving-project-bootstrap`.

The seed is not required after this package is generated.

## Core invariant

The full skill must remain a project-context bootstrap and context-evolution system.

It must not become a generic coding guide or a permanent runtime dependency for target projects.

## Evidence sources

Use:

- explicit user instructions
- managed project `AGENTS.md`
- managed project `.agent/project/`
- managed project `.agent/skills/project-context-evolution/SKILL.md`
- managed project `.agent/experience/`
- managed project `.agent/iteration/`
- managed project `.agent/evals/`
- approved external references in `PROJECT_REFERENCES.md`

## Promotion rule

Promote a managed-project lesson into this full skill only when it:

- appears across multiple managed projects
- fixes repeated context drift
- improves project independence
- improves review, rollback, or eval quality
- is explicitly requested by the user

## Update procedure

1. Collect managed project evidence.
2. Classify lessons as local or generalizable.
3. Update protocols or templates minimally.
4. Preserve project independence.
5. Record the update in `PROJECT_REFERENCES.md`.

## Anti-drift

Do not drift toward:

- generic software advice
- project management theory
- permanent project dependency
- uncontrolled self-modification
- user emotion optimization as the sole objective

## Scheduled update reality

This full skill is not a daemon. It updates only when invoked by a user, coding agent, scheduler, CI job, or local script.
