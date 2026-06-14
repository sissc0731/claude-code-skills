---
name: sql-format
description: Format and optimize SQL queries. Use when user pastes SQL, says "format this SQL", "optimize this query", or "beautify SQL".
---

# SQL Formatter & Optimizer

Format SQL queries for readability and suggest optimizations.

## Workflow

1. Read the SQL query
2. Detect dialect (MySQL, PostgreSQL, SQLite, MSSQL, Oracle)
3. Format with consistent style
4. Suggest optimizations if applicable

## Formatting Rules

### Keywords
- SQL keywords UPPERCASE: SELECT, FROM, WHERE, JOIN, etc.
- Function names lowercase: count(), sum(), coalesce()
- Table/column names: keep original case

### Indentation
```sql
SELECT
    t1.column1,
    t1.column2,
    COUNT(t2.id) AS count_alias
FROM schema.table_name AS t1
LEFT JOIN other_table AS t2
    ON t1.id = t2.foreign_id
    AND t2.status = 'active'
WHERE t1.created_at >= '2025-01-01'
    AND t1.deleted = FALSE
GROUP BY t1.column1, t1.column2
HAVING COUNT(t2.id) > 5
ORDER BY count_alias DESC
LIMIT 20;
```

### Rules
- One column/condition per line
- Commas at end of line (trailing)
- JOIN conditions on separate lines
- Subqueries indented one level
- WITH (CTE) clauses: each CTE on its own

## Optimization Tips

After formatting, suggest optimizations if you notice:
- `SELECT *` → list specific columns
- Missing indexes for WHERE/JOIN columns
- N+1 patterns (correlated subqueries that could be JOINs)
- `OR` conditions that could use UNION
- Missing `LIMIT` on large result sets

## Rules
- Never change query logic — only format
- Keep existing aliases
- Optimization suggestions are advisory, not changes
