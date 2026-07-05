# STATUS

> Updated: 2026-07-05
> Current task: fight-on-memory v0.1.0 is published.
> Next step: Plan v0.2 adapter wrapper or checkpoint scripts.

## Current State

fight-on-memory is a lightweight file protocol for keeping long-running AI agents aligned with project state and operating rules.

## Core Files

| File | Purpose | Status |
|---|---|---|
| `AGENTS.md` | Agent operating rules | Draft |
| `STATUS.md` | Current worksite state | Draft |
| `LOG.md` | Append-only work history | Draft |
| `.fightonmemory.toml` | Optional adapter config | Draft |
| `templates/` | Copyable starter templates | Draft |

## Decisions

- Keep the public MVP small: `AGENTS.md`, `STATUS.md`, `LOG.md`.
- Keep `.fightonmemory.toml` optional.
- Treat Codex + relay as the first adapter, not the whole project.
- Include protocol compliance as part of anti-drift, not as a separate project.
- Use MIT License for the first public release.
- Use repository name `fight-on-memory`.
- Ship v0.1 as protocol, templates, and docs before adding a working adapter.

## Open Questions

- Should v0.2 add a working relay wrapper, minimal checkpoint scripts, or both?
