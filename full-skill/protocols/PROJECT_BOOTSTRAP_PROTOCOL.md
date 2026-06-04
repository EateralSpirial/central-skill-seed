# Project Bootstrap Protocol

## Goal

Create an independent project-level agent context.

## Procedure

1. Inspect project language, framework, package manager, commands, tests, docs, and existing agent instructions.
2. Identify architecture boundaries, generated files, secrets policy, and risk surfaces.
3. Preserve useful existing rules and quarantine contradictions.
4. Create or update `AGENTS.md`.
5. Create `.agent/project/`.
6. Install `.agent/skills/project-context-evolution/SKILL.md`.
7. Create `.agent/experience/`, `.agent/iteration/`, and `.agent/evals/`.
8. Register the project in the full skill's `PROJECT_REFERENCES.md`.
9. Report created files and unresolved gaps.

## Success criteria

Future agents can continue through project-local context without reading `self-evolving-project-bootstrap`.
