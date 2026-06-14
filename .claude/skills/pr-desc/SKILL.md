---
name: pr-desc
description: Generate pull request description from git diff. Use when user says "generate PR description", "write PR summary", or before opening a pull request.
---

# PR Description Generator

Generate a comprehensive pull request description from the current branch's diff.

## Workflow

1. Run `git diff origin/main...HEAD` (or base branch)
2. Analyze the diff: files changed, types of changes, impact
3. Generate a structured PR description

## Output Format

```markdown
## 📝 Summary
[One paragraph: what this PR does and why]

## 🎯 Motivation
[Link to issue or describe the problem being solved]

## 🔧 Changes
- `file1.ts`: [what changed and why]
- `file2.ts`: [what changed and why]

## 📸 Screenshots
<!-- If UI changes, add screenshots -->

## ✅ Testing
- [ ] Unit tests added/updated
- [ ] Manually tested on [browser/device]
- [ ] Edge cases: [list]

## ⚠️ Breaking Changes
<!-- If any, describe migration steps -->

## 📋 Checklist
- [ ] Code follows project style
- [ ] Self-reviewed
- [ ] No unnecessary changes
- [ ] Documentation updated
```

## Rules
- Read the actual diff, don't guess
- Mention every changed file with a brief explanation
- If the diff is empty or trivial, say so
- Include testing instructions specific to the changes
- Flag anything that might be controversial or needs discussion
