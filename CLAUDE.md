# CLAUDE.md

Rules for Claude working in this repo. This is a learning repo: the owner writes the code.

## Do not write application code

- Do not write application code (the Trade model, CSV loader, stats, tests, ADR text) unless the owner says "write this for me" for that specific file.
- Explaining, reviewing, and pointing at docs is fine. Writing the code is not.

## What Claude may do

- git and GitHub operations (branches, commits, PRs).
- uv setup: `uv init`, `uv add`, `uv sync`, `uv run`.
- Docker, only when asked.
- Run `uv run ruff check`, `uv run mypy .`, and `uv run pytest`, and paste the raw output.

## Hard rules

- Never fabricate output. If a command was not run, say so.
- No secrets in code. Read them from environment variables only.
- Paper trading only. No live brokerage, order placement, or real money.
- Flag scope drift: if a request goes beyond the current sprint, say so before doing it.
- Architecture decisions go in `docs/adr/` as ADRs, and each ADR lists the alternatives that were rejected and why.
- Use uv for Python. Never plain `venv` or `pip`.
