# :memo: Notes
## CURSOR
### Rule ship-it Command

---
description: Trigger full commit workflow when user types "ship-it"
alwaysApply: true
---

# ship-it Command

## CRITICAL: When to Commit

> **NEVER commit automatically.** Only commit when the user explicitly types **ship-it**.

| User Says                       | Agent Action                                                                                                                |
| ------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| "implement X", "add Y", "fix Z" | Show code changes (per `permissions.mdc`), wait for "Apply this", apply changes, verify they work, **STOP** — do NOT commit |
| "ship-it"                       | Execute the commit workflow below                                                                                           |
| "implement X and commit"        | Show code changes, wait for "Apply this", apply changes AND commit (explicit request)                                       |

After completing any implementation task (without explicit commit request):

1. Show what was done
2. Verify it works (run tests, linters if relevant)
3. Say: **"Type ship-it when ready to commit."**
4. **Wait for user to type ship-it**

---

## Workflow

When the user types **ship-it** (exactly), execute this workflow:

## Workflow Steps

1. **Check for changes**: Run `git status` to see what changed

2. **Ensure documentation exists** (CRITICAL STEP):
   - Check if `docs/` directory exists, create it if missing
   - **Early-stage check** (before creating any missing doc): Check for **analyzable content** — dependency/manifest files (package managers, lockfiles, build configs) OR application/implementation code (source dirs, modules, packages, entry points). If **neither exists** (only README, rules, or planning docs): create **minimal placeholders** with `To be defined once [relevant aspect] exists in the codebase.` Do **not** infer from README or planning docs. If **at least one exists**: proceed with analysis below.
   - Check if `docs/architecture.md` exists:
     - If **missing**: (and not early-stage) Deep analyze the project (entry points, layers, patterns, data flow, security, deployment) and create it with plaintext tree structures
     - If **exists**: Skip creation, proceed to step 3 for updates
   - Check if `docs/stack.md` exists:
     - If **missing**: (and not early-stage) Analyze dependency files, build configs, runtime configs, and create it with technology stack tree
     - If **exists**: Skip creation, proceed to step 3 for updates
   - Check if `docs/structure.md` exists:
     - If **missing**: (and not early-stage) Analyze entire project structure (folders, files, naming conventions, organization) and create it with complete directory tree
     - If **exists**: Skip creation, proceed to step 3 for updates

3. **Update documentation** (if relevant changes exist):
   - `README.md` — Update if stack, scripts, setup changed, OR if new docs files added (link them in Documentation section)
   - `docs/architecture.md` — Update if (only if file exists from step 2):
     - New files added/removed in core application directories (services, components, controllers, handlers, business logic layers, etc.)
     - Routing files changed (routes, routers, navigation configs, etc.)
     - New architectural patterns introduced
     - New layers or components added
     - Data flow changed
     - Security architecture modified
     - Deployment architecture changed
   - `docs/stack.md` — Update if (only if file exists from step 2):
     - Dependency files changed (`package.json`, `requirements.txt`, `pom.xml`, `Cargo.toml`, `go.mod`, `Gemfile`, `composer.json`, etc.)
     - Build configs changed (`tsconfig.json`, `webpack.config.js`, `Makefile`, `CMakeLists.txt`, `build.gradle`, `Cargo.toml`, etc.)
     - Runtime versions changed
     - New technologies integrated
   - `docs/structure.md` — Update if (only if file exists from step 2):
     - New directories created or removed
     - Files moved to different directories
     - Folder names changed
     - File naming conventions changed
     - New domain entities added
     - Import patterns changed

4. **Handle README.md separately** (CRITICAL - CHECK FIRST):
   - If `README.md` or `README` is in the changed files:
     - Stage ONLY `README.md` or `README`: `git add README.md` (or `git add README`)
     - Commit with message exactly: **Update README file** (no prefix, no other text, no body)
     - Check if there are remaining uncommitted files: `git status`
     - If there are remaining files, continue to step 5
     - If no remaining files (only README was changed), skip to step 6
   - If `README.md` or `README` is NOT in changed files:
     - Stage all changes: `git add -A`
     - Continue to step 5

5. **Commit** with proper message following `commit-conventions.mdc`:
   - Verify there are staged changes: `git status` should show files ready to commit
   - If no staged changes, skip to step 6 (this should not happen if step 4 logic was followed correctly)
   - Commit remaining files with appropriate conventional commit message

6. **Error Handling**: If any git command fails (status, add, commit), stop the workflow and inform the user with the error message. Do not proceed with subsequent steps.

7. **Show summary**: List files changed, commit hash(es), brief explanation

## Commit Message Rules

**IMPORTANT**: Always follow `commit-conventions.mdc` strictly. Check these rules in order:

### 1. README.md Special Case (HIGHEST PRIORITY - NO EXCEPTIONS)

**CRITICAL**: This rule applies ALWAYS, regardless of other changes.

- If `README.md` or `README` is modified (alone OR with other files):
  - **MANDATORY**: Commit message MUST be exactly: **Update README file**
  - No prefix (no `docs:`, `update:`, etc.)
  - No other text
  - No body
  - No variations
  - **MANDATORY**: Commit README separately from other files
  - If other files also changed, make two commits:
    1. First: `README.md` only → message: **Update README file**
    2. Second: Other files → appropriate conventional commit message

### 2. Standard Commits

For all other changes (when README is not involved):

- Use appropriate type prefix (`feat`, `fix`, `refactor`, `docs`, etc.)
- Keep subject concise, imperative mood
- Add body only if multiple logical changes

## Output Format

After completing, show:

## Summary: [Brief description]

**Commit**: [hash] [message]

### Files Changed

| File | Change |
| ---- | ------ |
| .... | ...... |

### What Was Done

[1-3 sentence explanation of the changes]

## Documentation Analysis Guidelines

When creating or updating documentation files, adapt to the project's stack and structure:

### For `docs/architecture.md`

- **Analyze**: Entry points, application structure, layers/components, routing/handlers, middleware/interceptors, services/business logic, data access layer, external integrations
- **Document**: System architecture, layers/components, data flow, authentication/authorization flow, background jobs/scheduled tasks, external integrations, security architecture, deployment architecture
- **Use**: Plaintext tree structures, ASCII diagrams, clear sections
- **Adapt to stack**:
  - Web frameworks: Express.js, Django, Flask, Spring Boot, Rails, etc.
  - Microservices: Service boundaries, API gateways, message queues
  - Mobile: App architecture, navigation, state management
  - Desktop: Application structure, UI frameworks

### For `docs/stack.md`

- **Analyze**:
  - Dependency files: `package.json` (Node.js), `requirements.txt`/`pyproject.toml` (Python), `pom.xml`/`build.gradle` (Java), `Cargo.toml` (Rust), `go.mod` (Go), `Gemfile` (Ruby), `composer.json` (PHP), etc.
  - Build configs: `tsconfig.json`, `webpack.config.js`, `Makefile`, `CMakeLists.txt`, `build.gradle`, `Cargo.toml`, etc.
  - Container files: `Dockerfile`, `docker-compose.yml`, `Kubernetes` manifests
  - CI/CD configs: `.github/workflows`, `.gitlab-ci.yml`, `Jenkinsfile`, etc.
  - Runtime configs: Environment files, config files
- **Document**: Runtime environment, programming language, frameworks/libraries, databases, tools, build systems, deployment tools, versions
- **Use**: Plaintext tree structures showing technology hierarchy

### For `docs/structure.md`

- **Analyze**: Entire project directory structure, file naming patterns, layer organization, module/package structure
- **Document**: Complete directory tree, file purposes, naming conventions, domain entities/modules, import/include patterns, build output structure
- **Use**: Plaintext tree structures showing folder hierarchy
- **Adapt to patterns**:
  - MVC, MVVM, Clean Architecture, Hexagonal Architecture
  - Monorepo vs single-repo structures
  - Language-specific conventions (Python packages, Java packages, Go modules, etc.)

## Important

- Do NOT push to remote unless explicitly asked
- If no changes exist at step 1, inform the user: "Nothing to commit, working tree clean" and stop workflow
- If documentation doesn't need updates, skip that step silently
- **Always ensure documentation files exist** before committing — this keeps projects documented
- If documentation creation/update fails, log the error but continue with commit workflow (documentation is important but shouldn't block commits)
- If git operations fail, stop immediately and report the error to the user

## Software Developer
Built by [JAVI](https://github.com/javi0b01/) :copyright: 2026  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javi0b01/).
