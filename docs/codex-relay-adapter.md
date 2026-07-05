# Codex Relay Adapter

This adapter is for Codex using an OpenAI-compatible model through a relay, such as DeepSeek via `codex-relay`.

The relay adapter is not the protocol itself. It is one way to enforce the protocol more consistently.

## Goal

Before each model request, inject a short project anchor so the model keeps seeing the current operating rules and worksite state.

## Anchor Inputs

By default, read:

```text
AGENTS.md
STATUS.md
```

Do not inject:

```text
LOG.md
```

`LOG.md` is for recovery and audit. It can be too large for every request.

## Expected Behavior

1. Find the project root.
2. Read `.signalforge.toml` if present.
3. Load the configured anchor files.
4. Stop if `STATUS.md` is stale or missing required fields.
5. Prepend the anchor to the model request.
6. Forward the request to the upstream model.

## Notes

Existing relay tools usually translate protocol shapes. They do not understand project status, local skills, or PreFlight rules by themselves.

SignalForge Checkpoint can be implemented as a wrapper before the relay, or as a feature inside a custom relay.

