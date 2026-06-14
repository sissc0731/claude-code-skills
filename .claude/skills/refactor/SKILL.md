---
name: refactor
description: Analyze code and suggest refactoring improvements. Use when user says "refactor this", "improve this code", "clean up", or "any suggestions for this code".
---

# Code Refactoring Advisor

Analyze the selected code and suggest specific, actionable refactoring improvements.

## Workflow

1. Read the selected code thoroughly
2. Identify smells, anti-patterns, inefficiencies
3. Suggest specific refactorings with before/after examples
4. Rate each suggestion: 🔴 critical / 🟡 improvement / 🟢 optional

## What to Look For

### Code Smells
- Long functions (>30 lines)
- Deep nesting (>3 levels)
- Duplicated code
- Magic numbers/strings
- Too many parameters (>4)
- God classes (too many responsibilities)
- Feature envy (method using another class's data too much)

### Performance
- N+1 queries
- Unnecessary loops
- Repeated expensive operations
- Missing memoization
- Large bundle imports (JS)

### Readability
- Poor variable names
- Missing early returns
- Complex conditionals
- Mixed abstraction levels
- Comments explaining WHAT instead of WHY

## Output Format

```
## 🔍 重构分析: `filename.ts`

### 🔴 关键问题
**问题**: [description]
**建议**: [specific fix]
```diff
- old code
+ new code
```

### 🟡 改进建议
[Same format]

### 🟢 可选优化
[Same format]

## 📊 总结
- 复杂度: [low/medium/high]
- 建议优先处理 [N] 个问题
```

## Rules
- Never suggest rewrites — suggest incremental improvements
- Each suggestion must have concrete before/after code
- Don't suggest features the user didn't ask for
- Match existing code style
- If the code is fine, say so — don't force suggestions
