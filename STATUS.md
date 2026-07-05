# STATUS

> Updated: 2026-07-05
> Current task: Rename the public repository to fight-on-memory.
> Next step: Push the rename commit and update GitHub repository metadata.

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

## Open Questions

- Decide whether the first release should include a working relay wrapper or only protocol templates.
