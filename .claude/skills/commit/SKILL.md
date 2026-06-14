---
name: commit
description: Generate Conventional Commit messages from staged git changes. Use when the user asks "generate commit message", "what should I commit", or after making code changes.
---

# Commit Message Generator

Generate a well-formatted Conventional Commit message based on staged changes.

## Workflow

1. Run `git diff --staged` to see what changed
2. Analyze the diff: identify the type of change, scope, and core modification
3. Generate a commit message following the Conventional Commits format

## Commit Format

```
<type>(<scope>): <subject>

<body>
```

### Types
- `feat` — new feature
- `fix` — bug fix
- `docs` — documentation
- `style` — formatting, semicolons, etc.
- `refactor` — code restructuring without feature changes
- `perf` — performance improvement
- `test` — adding tests
- `chore` — maintenance, deps, config
- `ci` — CI/CD changes

### Rules
- Subject: max 50 chars, imperative mood, no period at end
- Body: explain WHAT and WHY, not HOW
- If breaking change: add `BREAKING CHANGE:` in body or `!` after type
- Reference issues: `Closes #123` or `Refs #456`

## Output

Present ONE commit message. If the diff spans multiple concerns, suggest splitting into separate commits and list each message.
