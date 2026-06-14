---
name: test-gen
description: Generate unit tests for selected code. Use when user says "add tests", "write unit tests", "generate test cases", or highlights code needing test coverage.
---

# Unit Test Generator

Generate comprehensive unit tests for the selected code.

## Workflow

1. Read the selected function/class
2. Identify: inputs, outputs, edge cases, dependencies
3. Generate tests in the appropriate framework
4. Cover: happy path, edge cases, error cases, boundary values

## Framework by Language

| Language | Framework |
|----------|-----------|
| JavaScript | Jest / Vitest |
| TypeScript | Jest / Vitest |
| Python | pytest |
| Java | JUnit 5 |
| Go | testing |
| Rust | #[test] |
| Ruby | RSpec |

## Coverage Checklist

For each function, generate tests for:
- ✅ **Happy path** — normal input → expected output
- ✅ **Edge cases** — empty, null, undefined, 0, -1
- ✅ **Error cases** — invalid input, exceptions
- ✅ **Boundary values** — max, min, off-by-one
- ✅ **Async** — promise resolve/reject (if applicable)

## Output Format

```typescript
// filename.test.ts
import { describe, it, expect } from 'vitest';

describe('functionName', () => {
  // Happy path
  it('should return expected result for normal input', () => {
    expect(functionName(input)).toBe(expected);
  });

  // Edge cases
  it('should handle empty input', () => {
    expect(functionName('')).toBe(expected);
  });

  // Error cases
  it('should throw for invalid input', () => {
    expect(() => functionName(invalid)).toThrow();
  });
});
```

## Rules
- Use the project's existing test framework, don't introduce new ones
- Match existing test style (naming, structure, assertions)
- Mock external dependencies (API calls, DB, file system)
- Tests should be runnable immediately — don't reference undefined fixtures
