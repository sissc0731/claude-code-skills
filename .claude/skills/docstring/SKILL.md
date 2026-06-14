---
name: docstring
description: Generate documentation comments for code. Use when user says "add comments", "generate docs", "add JSDoc/docstring/JavaDoc", or highlights undocumented code.
---

# Documentation Generator

Generate proper documentation comments for the selected code.

## Workflow

1. Read the selected code
2. Detect the language
3. Generate appropriate documentation format
4. Insert comments without changing any code logic

## Format by Language

### JavaScript/TypeScript → JSDoc
```js
/**
 * Description of what the function does.
 * @param {string} name - Parameter description
 * @returns {Object} Return value description
 * @throws {Error} When something goes wrong
 * @example
 * // Usage example
 */
```

### Python → Docstring
```python
def function_name(param1, param2):
    """
    Description of what the function does.

    Args:
        param1 (str): Description
        param2 (int): Description

    Returns:
        dict: Description of return value

    Raises:
        ValueError: When conditions

    Example:
        >>> function_name("hello", 42)
        {"result": "ok"}
    """
```

### Java → JavaDoc
```java
/**
 * Description.
 * @param name description
 * @return description
 * @throws Exception description
 */
```

### Go → GoDoc
```go
// FunctionName does X with Y.
// It returns Z on success, or an error.
```

## Rules
- Don't change the code, only add comments
- Don't over-document obvious things (e.g., `// i++ increments i`)
- Focus on WHAT and WHY, not HOW
- Document edge cases and assumptions
- Keep existing comments intact
