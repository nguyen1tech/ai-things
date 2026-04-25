---
applyTo: "**/*.py"
---

# Python Coding Standards

## Core Formatting

- **PEP 8**: Follow standard PEP 8 guidelines for all code.
- **Indentation**: Use exactly 4 spaces (never tabs).
- **Line Length**: Limit code to 88 characters to align with [Ruff](https://astral.sh) or Black formatters.
- **Naming**:
  - `snake_case` for functions, variables, and modules.
  - `PascalCase` for classes.
  - `UPPER_CASE` for constants.
  - Use descriptive names (e.g., `user_id` instead of `uid`).

## Modern Features & Performance

- **Type Hinting**: Mandatory type annotations for all function signatures (Python 3.10+ syntax preferred).
- **Docstrings**: Use [Google-style docstrings](https://github.io) for all public methods and classes.
- **F-Strings**: Use f-strings for all string formatting instead of `.format()` or `%`.
- **Imports**: Organize imports into groups (Standard Library, Third-party, Local) separated by blank lines.

## Quality Constraints

- **Explicit Errors**: Never use bare `except:` blocks; always catch specific exceptions.
- **No Print**: Use the standard `logging` library instead of `print()` for production code.
- **Cleanup**: Always close resources using context managers (`with` statements).
