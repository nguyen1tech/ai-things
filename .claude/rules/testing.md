---
applyTo: "**/*.py"
---

# Testing Standards

## Framework & Discovery

- **Framework**: Use `pytest` exclusively for all tests.
- **Naming**: Test files must match the `test_*.py` pattern to ensure automatic discovery.
- **Organization**: Place unit tests in `tests/unit/` and integration tests in `tests/integration/`.

## Execution Rules

- **Pre-verification**: Before writing code, state the verification method you will use (e.g., "I will verify this by running `pytest tests/test_module.py`").
- **Auto-check**: Always run relevant tests after modifying logic. Never consider a task "done" until tests pass.
- **Isolated Runs**: Use `-k` to run specific tests if the suite is large to save time and context.

## Quality & Style

- **Pattern**: Follow the **Arrange-Act-Assert** pattern for clear test structure.
- **Mocking**: Use `pytest-mock` to simulate external dependencies like APIs or databases.
- **No Unexplained Literals**: Parameterize test inputs instead of using "magic numbers" or hardcoded strings.
- **Coverage**: Maintain a high bar for new features; every new function or class **must** have a corresponding unit test.

## Safety

- **No Silent Failures**: If a test fails, you must debug the root cause before moving on.
- **Persistence**: Never run "throwaway" test code in the terminal; always save verification logic as a discrete test file.
