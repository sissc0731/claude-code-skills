---
name: explain
description: Explain selected code in plain language. Use when the user asks "explain this code", "what does this do", or highlights code they want to understand.
---

# Code Explainer

Explain the selected code in clear, plain language.

## Workflow

1. Read the selected/highlighted code
2. Identify: language, patterns, purpose
3. Explain in structured format

## Output Format

```
## 📋 代码概览
[One sentence: what this code does]

## 🔍 逐行分析
- `line X`: [explanation]
- `line Y`: [explanation]

## 🏗 设计模式
[Patterns used: singleton, factory, observer, etc.]

## ⚠️ 注意事项
- [edge cases, potential bugs]
- [performance considerations]

## 💡 改进建议
- [if any obvious improvements]
```

## Rules
- Explain in the same language the user uses
- For beginners: explain basic concepts
- For experienced devs: focus on patterns and gotchas
- Never say "obviously" or "clearly" — explain everything
