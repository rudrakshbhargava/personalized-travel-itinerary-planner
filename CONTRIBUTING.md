# Contributing

Thanks for helping improve Wayfarer.

## Development setup
1. Follow the local setup steps in [`README.md`](README.md).
2. Keep `.env` files local; copy the safe examples instead.
3. Use the demo path for tests and development unless working explicitly on configured Supabase/AI integration.

## Before opening a pull request
- Run frontend type checking, linting, tests, and production build.
- Run backend Ruff and pytest.
- Add tests for new endpoints, persistence rules, validation, and UI flows.
- Ensure every primary button performs its labelled action.
- Keep all estimates clearly marked, and never imply a booking or live data lookup that did not occur.
- Check keyboard operation and responsive layouts.

## Style
- Prefer small, typed modules and straightforward implementation.
- Do not add infrastructure or duplicate dependencies without a concrete need.
- Keep API error messages informative but free of secrets and private prompt content.
