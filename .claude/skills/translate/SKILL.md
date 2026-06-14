---
name: translate
description: Translate Markdown files between Chinese and English. Use when user says "translate this document", "翻译这个文档", "中译英", "英译中".
---

# Markdown Translator

Translate Markdown files between Chinese and English while preserving all formatting.

## Workflow

1. Read the Markdown file
2. Detect source and target languages (ask if unclear)
3. Translate content while preserving ALL Markdown syntax
4. Keep code blocks, URLs, technical terms unchanged

## Preservation Rules

### Keep Untranslated
- Code blocks (``` ... ```) — preserve exactly
- Inline code (`...`) — preserve exactly
- URLs and links — keep href, translate link text
- Image paths — keep src, translate alt text
- HTML tags — keep tags, translate content
- Frontmatter — keep keys, translate values if appropriate
- Technical terms: API, JSON, HTML, CSS, Git, npm, etc.

### Translate
- Headings, paragraphs, list items
- Table content (not table syntax)
- Link text (not URLs)
- Image alt text (not src)
- Blockquote content

## Language Pairs

| Direction | When to use |
|-----------|-------------|
| EN → ZH | English README/docs for Chinese audience |
| ZH → EN | Chinese docs for international audience |

## Output

1. Show a brief diff summary (lines changed, preserved)
2. Write the translated file as `<original-name>.<lang>.md`
   - EN→ZH: `README.zh.md`
   - ZH→EN: `README.en.md`

## Rules
- Never translate code or commands
- Keep the same heading levels and structure
- Preserve blank lines for readability
- If a term has an established Chinese translation, use it (e.g., "请求" not "request")
