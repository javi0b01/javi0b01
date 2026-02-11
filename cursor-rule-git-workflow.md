# :memo: Notes
## CURSOR
### Rule Git Workflow

---
description: Git commit and push behavior rules
alwaysApply: true
---

# Git Workflow Rules

## Commit Control

> **The user controls when commits happen, not the agent.**

### Do NOT commit when:

- User asks to "implement", "add", "fix", "create", "update" something
- User asks to "make changes" or "modify" code
- After completing any coding task (unless explicitly asked)

### DO commit when:

- User types **ship-it** (triggers full commit workflow)
- User explicitly says "commit", "commit this", "commit the changes"
- User says "implement X **and commit**" (explicit combined request)

## Push Control

> **Never push unless explicitly asked.**

- After all commits are complete (including separate README commits), inform user: "Your branch is X commits ahead. Want me to push?"
- Only push when user says "yes", "push", "push it", or similar

## Related Rules

- For commit message format, see `commit-conventions.mdc`
- For full commit workflow details, see `ship-it-command.mdc`
- For file modification permissions, see `permissions.mdc`

## Summary

```
implement X     → Show code, wait for "Apply this", apply changes, STOP, wait for ship-it
ship-it         → Update docs, commit, show summary
push            → Push to remote
```

## Software Developer
Built by [JAVI](https://github.com/javi0b01/) :copyright: 2026  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javi0b01/).
