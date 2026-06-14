---
name: env-gen
description: Generate .env.example from codebase scanning. Use when user says "create .env.example", "generate env template", "what env vars does this project need".
---

# .env.example Generator

Scan the codebase for environment variables and generate a `.env.example` file.

## Workflow

1. Search codebase for env var references:
   - `process.env.X` (Node.js)
   - `os.getenv("X")` (Python)
   - `System.getenv("X")` (Java)
   - `env.X` (Go)
   - `import.meta.env.X` (Vite)
   - `$ENV{X}` (Perl)
   - `env!("X")` (Rust)
2. Also check: `.env`, `.env.example`, `.env.template`, `env.d.ts`
3. Group by category
4. Generate `.env.example`

## Output Format

```bash
# ===========================================
# Project Name — Environment Variables
# Copy: cp .env.example .env
# ===========================================

# --- App ---
NODE_ENV=development
PORT=3000
HOST=0.0.0.0

# --- Database ---
DATABASE_URL=postgresql://user:password@localhost:5432/dbname
DATABASE_POOL_MAX=10

# --- Auth ---
JWT_SECRET=change-me-to-a-random-string
SESSION_TTL=86400

# --- External APIs ---
OPENAI_API_KEY=sk-...
STRIPE_SECRET_KEY=sk_test_...

# --- Redis ---
REDIS_URL=redis://localhost:6379

# --- Email ---
SMTP_HOST=smtp.example.com
SMTP_PORT=587
SMTP_USER=user@example.com
SMTP_PASS=
```

## Rules
- Include ALL env vars found in codebase
- Add descriptive comments for each variable
- Use placeholder values (not real secrets)
- Group by category (App, DB, Auth, APIs, etc.)
- Mark required vs optional vars
- If env vars have defaults in code, use the default value
- Never include real API keys or secrets in the output
