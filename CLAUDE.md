# CLAUDE.md

## Available Skills

This project includes custom skills in `.claude/skills/`:

- **commit** — Generate Conventional Commit messages from staged git changes
- **explain** — Explain selected code in plain Chinese or English
- **docstring** — Generate JSDoc/Python docstring/JavaDoc comments
- **test-gen** — Generate unit tests for selected code
- **refactor** — Analyze code and suggest refactoring improvements
- **translate** — Translate Markdown files between Chinese and English
- **release-notes** — Generate release notes from git commits
- **pr-desc** — Generate pull request description from diff
- **readme-gen** — Generate project README from codebase analysis
- **sql-format** — Format and optimize SQL queries
- **env-gen** — Generate .env.example from codebase scanning
- **changelog** — Generate CHANGELOG.md from git history

Invoke skills by describing the task naturally (e.g., "generate a commit message", "explain this code", "add comments to this function").
