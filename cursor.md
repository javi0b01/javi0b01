# :memo: Notes
## CURSOR
### Learn
1. What is it
2. What does it do
3. Why to use it
4. Getting started
5. Concepts
6. Code samples
7. Documentation
### Resources
- [Cursor](https://cursor.com)
- [Documentation](https://cursor.com/docs)
### Terms and concepts
- Chat
- Agent
* Rule
  * Structure
    - YAML
    - Markdown
### Roadmap
Cursor Learning Roadmap  
A simple, sequential guide for learning to use an AI code editor like Cursor, from basic to complex.
#### Level 1: Getting Started - The Fundamentals
1. **Installation & Setup:**
  * Download and install Cursor on your operating system.
  * Open an existing project or a new folder.
2. **UI Familiarization:**
  * Identify the main AI feature: the Chat panel.
  * Notice how it's built on a familiar editor (VS Code), so file browsing, terminal, and basic editing are the same.
3. **Your First AI Interaction ("Hello, World!"):**
  * Open any code file.
  * Highlight a function or a block of code.
  * In the chat panel, type "Explain this code" and press Enter.
#### Level 2: Core AI-Assisted Coding
1. **AI Chat for Q&A:**
  * Ask general programming questions (e.g., "what's the difference between `let`, `const`, and `var` in JavaScript?").
  * Paste an error message from your terminal into the chat and ask the AI to explain it and suggest a fix.
2. **Generating New Code:**
  * In an empty file, ask the AI to create boilerplate code (e.g., "Create a simple Express server in Node.js").
  * Use "Ctrl+K" (or "Cmd+K") to open an inline prompt to generate code right where your cursor is.
3. **Editing & Refactoring Existing Code:**
  * Highlight a block of code.
  * Press "Ctrl+K" (or "Cmd+K") to open the inline prompt.
  * Tell the AI what to do (e.g., "Convert this to an async/await function," "Refactor this to be more readable," or "Add error handling").
#### Level 3: Leveraging Your Full Codebase
1. **Chatting with Your Codebase:**
  * Use the `@` symbol in the chat to reference specific files or folders (e.g., "What is the purpose of the `@/src/utils/api.js` file?").
  * Ask questions about the entire project (e.g., "Where is the user authentication logic handled in this codebase?").
2. **Context-Aware Code Generation:**
  * Ask the AI to write new code that follows existing patterns in your project (e.g., "Create a new function that fetches user data, following the style of the functions in `@/src/api/`").
3. **AI-Powered Debugging:**
  * Select a piece of code that has a bug.
  * Use the "Fix & Diff" feature to have the AI find the issue and propose a change, which you can review before applying.
#### Level 4: Advanced Techniques & Workflow Integration
1. **Writing Tests:**
  * Point the AI to a function or class using the `@` symbol.
  * Ask it to generate unit tests (e.g., "Write Jest tests for the `@calculateTotal` function").
2. **Large-Scale Changes:**
  * Use the AI to help with migrating code (e.g., "Help me convert this class-based React component to a functional component with Hooks").
3. **Customizing AI Behavior (Rules):**
  * Create rules for the AI to follow for your project, ensuring it generates code that adheres to your team's specific conventions and style guides.
### Setup
VS Code Settings
```
{
  "[css]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode",
  },
  "[html]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode",
  },
  "[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode",
  },
  "[json]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode",
  },
  "[jsonc]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode",
  },
  "[markdown]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode",
  },
  "[python]": {
    "editor.defaultFormatter": "charliermarsh.ruff",
    "editor.codeActionsOnSave": {
      "source.fixAll.ruff": "explicit",
    },
  },
  "editor.accessibilitySupport": "off",
  "editor.bracketPairColorization.independentColorPoolPerBracketType": true,
  "editor.bracketPairColorization.enabled": true,
  "editor.codeActionsOnSave": ["source.fixAll.eslint"],
  "editor.cursorBlinking": "expand",
  "editor.cursorStyle": "line",
  "editor.cursorWidth": 1,
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.detectIndentation": true,
  "editor.fontFamily": "JetBrains Mono",
  "editor.fontLigatures": false,
  "editor.fontSize": 13,
  "editor.formatOnSave": true,
  "editor.formatOnPaste": true,
  "editor.guides.bracketPairs": true,
  "editor.lineHeight": 1.3,
  "editor.minimap.enabled": false,
  "editor.minimap.maxColumn": 80,
  "editor.multiCursorModifier": "ctrlCmd",
  "editor.renderWhitespace": "all",
  "editor.rulers": [
    {
      "column": 80,
      "color": "#FF00FF",
    },
  ],
  "editor.snippetSuggestions": "top",
  "editor.suggestSelection": "first",
  "editor.tabSize": 2,
  "editor.wordWrap": "wordWrapColumn",
  "extensions.ignoreRecommendations": true,
  "files.insertFinalNewline": true,
  "files.trimTrailingWhitespace": true,
  "git.openRepositoryInParentFolders": "never",
  "javascript.preferences.quoteStyle": "single",
  "javascript.updateImportsOnFileMove.enabled": "always",
  "prettier.singleQuote": true,
  "terminal.integrated.copyOnSelection": true,
  "terminal.integrated.cursorBlinking": true,
  "terminal.integrated.env.linux": {},
  "terminal.integrated.fontFamily": "JetBrains Mono",
  "terminal.integrated.fontSize": 13,
  "window.commandCenter": true,
  "prettier.proseWrap": "preserve",
  "python.defaultInterpreterPath": "/bin/python3",
  "workbench.colorTheme": "One Dark Pro",
  "workbench.iconTheme": "material-icon-theme",
  "cursor.composer.shouldChimeAfterChatFinishes": true,
}
```
### Rules
Agnostic
- [Agent](./cursor-rule-agent.md)
- [commit-conventions](./cursor-rule-commit-conventions.md)
- [git-workflow](./cursor-rule-git-workflow.md)
- [language-preference](./cursor-rule-language-preference.md)
- [learning-first](./cursor-rule-learning-first.md)
- [permissions](./cursor-rule-permissions.md)
- [senior-conventions](./cursor-rule-senior-conventions.md)
- [ship-it-command](./cursor-rule-ship-it-command.md)
Specific
```
Create a new Cursor rule named "project-overview" in `.cursor/rules/`.

This rule must be **project-specific** (not architecture-agnostic or stack-agnostic).
Other rules in the project may stay generic; this one should reflect THIS project's:

- Main programming language
- Technology stack (frameworks, DB, tools)
- Structure and file placement conventions
- Naming conventions
- Any domain-specific patterns (e.g. response formats, API conventions)

**Requirements:**
1. Analyze in depth the project (entry point, config, structure, docs, existing rules) to infer conventions
2. Point to existing docs as source of truth for structure/stack — avoid duplicating them
3. Include only what's NOT in docs (e.g. response shapes, formatting, schema options)
4. Add any language/locale rules (e.g. "UI text in HTML templates must be in Spanish") if applicable
5. All other content in English: Comments, documentation, code (variable names, strings in TS/SCSS), and any non-UI text must always be in English.
6. Keep the rule lean (< 30 lines). One concern per bullet
7. Do NOT touch other files — only create the new rule
8. Avoid redundancy

Output a concise rule that an AI can follow to stay consistent with this project's standards.
```
## Software Developer
Built by [JAVI](https://github.com/javi0b01/) :copyright: 2026  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javi0b01/).
