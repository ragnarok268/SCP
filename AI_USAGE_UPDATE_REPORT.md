# AI Usage Update Report

## Files Changed

- `AGENTS.md`
- `docs/AI_USAGE.md`
- `README.md`
- `AI_USAGE_UPDATE_REPORT.md`

## Sections Added

- repository-level SCP agent guidance
- AI usage guide for Codex, Cursor, and Claude-style workflows
- README link section for AI coding agent usage

## Verification Results

- `python -m pytest` passed: 62 tests.
- `python -m pytest tests\test_scp.py tests\test_scp_cli.py` passed: 18 tests.
- `$env:PYTHONPATH=(Resolve-Path src); python -m scp.cli validate examples\scp` passed: validated 5 files.
- `git diff --check` passed.

## Confirmation

- Canon unchanged.
- No source behavior changed.
- No telemetry, cloud, or LLM dependencies added.
