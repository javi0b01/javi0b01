# :memo: Notes
## CURSOR
### Rule Commit Conventions

---
description: Commit message prefixes and format (Conventional Commits style)
alwaysApply: true
---

# Commit Message Conventions

## Special case (CHECK FIRST)

> **Priority**: Always check this rule BEFORE applying standard format.
> **CRITICAL**: This rule has NO exceptions. It applies ALWAYS.

- **README changes**: When `README` or `README.md` is modified:
  - **MANDATORY**: The commit message MUST be exactly: **Update README file**
    - No prefix (no `docs:`, `update:`, etc.)
    - No other text
    - No body
    - No variations
    - This applies ALWAYS, regardless of what changed in README.md
  - **MANDATORY**: Always commit README separately from other file changes
  - If other files also changed, make **two separate commits**:
    1. First commit: ONLY `README.md` or `README` with message: **Update README file**
    2. Second commit: All other files with appropriate conventional commit message

## Format

- **Pattern**: `type: subject` or `type(scope): subject`. Example: `feat(auth): add login view`.
- **Subject**: Imperative, lowercase after the colon, no period. Optional body below for _what_ / _why_.
- **Capitalization**: Subject should be lowercase after the colon, except for proper nouns, acronyms, or technical terms that are conventionally capitalized (e.g., `feat: add API endpoint`, `fix: handle JSON parsing`, `feat: integrate PayPal SDK`).

## Allowed types

| Type       | Use for                                               |
| ---------- | ----------------------------------------------------- |
| `init`     | Initial project setup                                 |
| `feat`     | New feature                                           |
| `fix`      | Bug fix                                               |
| `refactor` | Code structure (no feature, no fix)                   |
| `style`    | Format only (no logic change)                         |
| `docs`     | Documentation (except README; use special case above) |
| `test`     | Add or update tests                                   |
| `chore`    | Cleanup, maintenance                                  |
| `build`    | Build / tooling config                                |
| `release`  | Version release                                       |
| `update`   | General update                                        |
| `wip`      | Work in progress                                      |
| `temp`     | Temporary (revert before merge)                       |
| `debug`    | Debug logs (remove before merge)                      |
| `remove`   | Delete unused code                                    |
| `ci`       | CI config                                             |
| `deps`     | Dependencies                                          |
| `cleanup`  | Remove unused files                                   |
| `optimize` | Performance                                           |
| `config`   | Configuration                                         |

When suggesting commit messages: use these types and format; for README-only changes use **Update README file** only.

## Software Developer
Built by [JAVI](https://github.com/javi0b01/) :copyright: 2026  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javi0b01/).
