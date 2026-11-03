# Instructions for AI coding agents

## Project
`gradecalc` — a course grade calculator service. Start by reading `docs/REQUEST.md`.

## Constraints
- Python 3.10+. Standard library only at runtime; `pytest` for tests.
- The web interface must use the standard library (`http.server`), no frameworks.
- Keep the integration contract in `docs/REQUEST.md` exactly as written.

## Workflow
- We work in phases: spec → design and tasks → code → tests → CI → pull request → deploy.
  Do **only** the phase you are asked for, then stop and summarise.
- Project documents live in `docs/`: `spec.md`, `design.md`, `tasks.md`.
- Run the tests with `python -m pytest -q`.
- Never edit files in `tests/acceptance/` — those tests are owned by humans.
- Use small commits with clear messages. Never push to `main`; open a pull request.
- Never deploy unless all tests pass.
