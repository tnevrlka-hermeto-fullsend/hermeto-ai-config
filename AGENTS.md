# AGENTS.md

Hermeto is a Python CLI tool that pre-fetches project dependencies for hermetic
(network-isolated) container builds and generates SBOMs (Software Bill of Materials).

## Build and test

```shell
nox              # run all checks (lint + unit tests)
nox -s lint      # ruff check, ruff format, mypy
nox -s python-3.10 -- tests/unit/<path>  # run specific tests
```

## Code style

- Ruff for formatting, import sorting, and linting (line length 100)
- mypy with full type annotations required on all new code
- pytest for unit tests — aim for near-full coverage
- Each new `.py` file needs: `# SPDX-License-Identifier: GPL-3.0-only`
- See `pyproject.toml` for all tool configuration

## Tests

- Add new test cases rather than modifying existing ones
- Prefer `pytest.mark.parametrize` over duplicate test functions
- Do not string-match against output
- Cover positive and negative scenarios

## Commits and PRs

- Write clear commit messages explaining the "why"
- Sign off all commits with DCO: `git commit -s`
- Split changes into self-contained commits
- No gitmojis
- See CONTRIBUTING.md for full guidelines
- See AI_CONTRIBUTION_POLICY.md for AI disclosure requirements
