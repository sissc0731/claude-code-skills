---
name: changelog
description: Generate CHANGELOG.md from git history. Use when user says "update changelog", "generate changelog", or "what's changed in this project".
---

# Changelog Generator

Generate or update CHANGELOG.md following the Keep a Changelog format.

## Workflow

1. Check if CHANGELOG.md exists
2. Run `git log` or `git tag` to get version history
3. Categorize commits by type
4. Generate/update CHANGELOG.md

## Format (Keep a Changelog)

```markdown
# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- New feature X (#123)

### Changed
- Updated Y to use Z

### Deprecated
- Old API endpoint `/v1/foo`

### Removed
- Legacy auth module

### Fixed
- Bug where X caused Y (#456)

### Security
- Patched vulnerability in Z

## [1.0.0] - 2025-01-01

### Added
- Initial release
```

## Rules
- Use Keep a Changelog format (linked above)
- Group by: Added, Changed, Deprecated, Removed, Fixed, Security
- Reference issue/PR numbers when available
- Use ISO dates: YYYY-MM-DD
- Latest version first
- If updating existing changelog, only add new entries under [Unreleased]
- Don't duplicate content already in release notes
