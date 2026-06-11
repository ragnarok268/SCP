# Agent guidance for SCP

Before making changes:

1. Read `README.md`.
2. Read `docs/SCP_CANON.md`.
3. Read `docs/SCP_SCHEMA.md`.
4. If `.scp/origin.yaml` exists, read it before generating or consuming SCP records.
5. Read relevant SCP records under `.scp/` or `examples/scp/` when they apply to the task.

## SCP rules

- SCP works from adoption forward only.
- Do not invent missing project history.
- Do not infer Canon meanings.
- Use only Canon-defined event types, lifecycle states, card layers, and fields.
- Create SCP records only when a Canon event applies.
- Do not create SCP records for typo fixes, formatting changes, comment edits, routine refactors, trivial code movement, or dependency lockfile noise.
- If no Canon event applies, do not create an SCP record by default.
- Treat humans as decision makers and reviewers.
- Treat AI as maintainer of the reasoning layer, not owner of project decisions.

## When preserving a decision

1. Classify the event using `docs/SCP_CANON.md`.
2. Generate or update an SCP record using approved schema fields.
3. Include `why`, `evidence`, `constraints`, `impact`, `future_trap`, and `revisit_if` when available.
4. Validate SCP records before finishing:
   `$env:PYTHONPATH=(Resolve-Path src); python -m scp.cli validate examples\scp`
