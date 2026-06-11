# Using SCP With AI Coding Agents

## What AI agents should do first

AI agents should start by reading the repository framing in `README.md`, then the Canon in `docs/SCP_CANON.md`, then the schema in `docs/SCP_SCHEMA.md`.

If `.scp/origin.yaml` exists, the agent should read it before generating or consuming SCP records.

If relevant SCP records exist under `.scp/` or `examples/scp/`, the agent should read those records before making decisions that may already be preserved.

## How AI agents should use SCP

SCP is not retroactive.

It preserves reasoning from adoption forward and does not reconstruct old project history automatically.

SCP does not preserve every change.

The Canon defines meaning. The AI classifies changes using the Canon and should not guess outside those definitions.

The AI should:

- read the Canon before classifying project changes
- read the Origin Card when present
- read relevant SCP records before revisiting a decision
- create a record only when a Canon event applies
- avoid creating records for trivial changes or approved non-preservation events
- validate SCP records before finishing

## How Codex can use `AGENTS.md`

`AGENTS.md` provides concise repository-level instructions for Codex-style coding agents.

After cloning the repository, Codex can use `AGENTS.md` as an always-on guide for what to read first, what SCP rules to preserve, and how to validate SCP records before finishing work.

## How Cursor or Claude users can use the same guidance

Cursor and Claude users can copy the guidance from `AGENTS.md` into their project rules, workspace instructions, or agent bootstrap prompts.

The guidance is intentionally short so the same rules can be reused across tools without changing SCP semantics.

## SCP boundaries for AI agents

AI agents should remember these boundaries:

- SCP works from adoption forward only.
- SCP does not invent or reconstruct missing history.
- SCP does not preserve every change.
- The Canon defines event types, lifecycle states, card layers, and field meanings.
- Humans remain the decision makers and reviewers.
- AI maintains the reasoning layer rather than owning project decisions.

## Validation reminder

Before finishing SCP-related work, validate SCP records:

`$env:PYTHONPATH=(Resolve-Path src); python -m scp.cli validate examples\scp`
