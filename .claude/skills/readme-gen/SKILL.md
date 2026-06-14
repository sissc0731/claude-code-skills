---
name: readme-gen
description: Generate project README from codebase analysis. Use when user says "write a README", "create README for this project", or initializing a new repo.
---

# README Generator

Generate a comprehensive, well-structured README.md by analyzing the project codebase.

## Workflow

1. Scan project structure (Glob for key files)
2. Read package.json/Cargo.toml/go.mod/pyproject.toml etc.
3. Identify: project type, language, frameworks, entry points
4. Generate README sections

## Output Format

```markdown
# Project Name

<p align="center">
  <img src="badges" alt="badges">
</p>

Brief one-line description.

## ✨ Features
- Feature 1
- Feature 2

## 🚀 Quick Start

### Prerequisites
- Node.js >= 18
- etc.

### Installation
```bash
git clone ...
cd project
npm install
```

### Usage
```bash
npm start
```

## 📖 Documentation
Link or brief guide.

## 🧪 Testing
```bash
npm test
```

## 🏗 Architecture
Brief overview of project structure.

## 🤝 Contributing
How to contribute.

## 📜 License
MIT
```

## Rules
- Read actual project files, don't invent features
- Auto-detect: language, package manager, test framework, build tool
- Include real commands that work for this specific project
- If package.json has `scripts`, list the most important ones
- Keep it concise — don't write a novel
