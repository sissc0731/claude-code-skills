---
name: release-notes
description: Generate release notes from git commits. Use when user says "generate release notes", "write changelog for this release", "summarize what's in vX.X".
---

# Release Notes Generator

Generate structured, user-friendly release notes from git commit history.

## Workflow

1. Determine the version range (default: since last tag to HEAD)
2. Run `git log <last_tag>..HEAD --oneline` or similar
3. Categorize commits by type
4. Generate a release notes document

## Output Format

```markdown
# 🚀 Release v2.1.0 (2026-06-15)

## ✨ New Features
- Feature description (#123)
- Feature description (#124)

## 🐛 Bug Fixes
- Fix description (#125)

## 🚀 Performance
- Optimization description

## 📝 Documentation
- Doc update description

## 🔧 Maintenance
- Deps update, config changes, etc.

## 💥 Breaking Changes
- Migration guide if applicable

---

**Full Changelog**: https://github.com/user/repo/compare/v2.0.0...v2.1.0
```

## Rules
- Group commits by type (feat→Features, fix→Bugs, etc.)
- Write in user-facing language, not commit message language
- Exclude trivial commits (chore, style, ci unless significant)
- Link to issues/PRs where possible
- If no previous tag, include all commits since repo start
- Mark breaking changes with 💥 emoji and migration instructions
