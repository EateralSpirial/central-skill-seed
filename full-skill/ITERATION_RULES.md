# Full Skill Iteration Rules

## Purpose

These rules govern the generated full skill, not the seed.

The full skill may update its own protocols and templates based on managed project experience.

## Core Invariant

The full skill must remain a project-context bootstrap and context-evolution system.

It must not become a generic coding guide.

## Experience Sources

Use:

- managed project `AGENTS.md`
- managed project `.agent/project/`
- managed project `.agent/skills/project-context-evolution/SKILL.md`
- managed project `.agent/experience/`
- managed project `.agent/iteration/`
- managed project `.agent/evals/`
- explicit user instructions
- approved external references

## Promotion Rule

A managed-project lesson may be promoted into the full skill only if:

- it appears across multiple managed projects
- it fixes repeated context drift
- it improves project independence
- it improves review or rollback boundaries
- it improves eval coverage
- the user explicitly asks to promote it

## Update Procedure

1. Collect managed project evidence.
2. Classify lessons as local or generalizable.
3. Update protocols/templates minimally.
4. Preserve project independence.
5. Record the update in `PROJECT_REFERENCES.md`.

## Anti-Drift

Do not drift toward:

- generic software advice
- project management theory
- permanent runtime dependency
- uncontrolled self-modification
- user emotion optimization as sole objective

## Scheduled Update Reality

This full skill is not a daemon. It updates only when invoked by a user, coding agent, scheduler, CI job, or local script.
