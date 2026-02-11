# :memo: Notes
## CURSOR
### Rule Permissions

---
description: Control permissions - always ask before making file changes
alwaysApply: true
---

# CONTROL & PERMISSIONS

## File Modification Policy

- **DO NOT** use any tools to create, update, or delete files automatically.
- **ALWAYS** provide code snippets inside the chat interface first.
- **WAIT** for explicit verbal "Apply this" before using any editing tools.
- If you think a file needs to be deleted, explain the reasoning and ask for my permission first.

## Workflow

1. Show code changes in chat as code blocks
2. Explain what will change and why
3. Wait for explicit approval ("Apply this", "Go ahead", "Yes, apply", etc.)
4. Only then use editing tools

## Exception

Only apply changes automatically if the user explicitly requests it with phrases like:

- "Apply this"
- "Go ahead and make the change"
- "Yes, update the file"
- "Implement this" (still requires showing code first, then applying after approval)

**Note**: Even with "Implement this", you must still show code changes first, wait for "Apply this" approval, then apply the changes. The exception only means the user wants you to proceed with implementation, not skip the approval step.

## Relationship with Other Rules

- **Code changes** require "Apply this" approval (this rule)
- **Committing changes** requires "ship-it" command (see `ship-it-command.mdc`)
- These are **separate steps**: apply code first, then commit separately

## Software Developer
Built by [JAVI](https://github.com/javi0b01/) :copyright: 2026  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javi0b01/).
