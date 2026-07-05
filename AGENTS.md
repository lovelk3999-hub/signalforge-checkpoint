# AGENTS

This file defines the operating protocol for AI agents working in this project.

## Core Rule

File state wins over chat memory.

Before acting, read `STATUS.md`. If the state is unclear, stale, or inconsistent with the user request, stop and refresh the status first.

## Operating Protocol

1. Read `AGENTS.md`.
2. Read `STATUS.md`.
3. Identify the next concrete step.
4. Do not invent project state.
5. Do not skip required setup, validation, or checkpoint steps.
6. After a meaningful step, update `STATUS.md`.
7. Append `LOG.md` with what changed and why.

## Skill And Tool Protocol

Before answering or acting, check whether the user request triggers a local skill, tool, script, workflow, or project rule.

If a skill or workflow is triggered:

1. Read the full instruction file.
2. Check its scripts or commands.
3. Prefer existing scripts over rewriting logic.
4. Run required setup or PreFlight checks before the task.
5. Only continue after the protocol has been followed.

## Adapter Policy

Adapters may inject this file and `STATUS.md` before model requests.

Adapters should not inject `LOG.md` by default, because it can grow large. Use `LOG.md` for recovery, audit, and deeper context only when needed.

If `STATUS.md` is stale or unclear, adapters should stop the agent and request a status refresh.
