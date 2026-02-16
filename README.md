# Antecedent to All

A Substack article writing project with research, quotes, and supporting materials.

## Structure

- `articles/` - Published/canonical articles (frozen, read-only during editing)
- `drafts/` - Working copies for editing
- `context/` - Context files for AI (voice, intent, terminology)
- `prompts/` - Reusable prompts and templates
- `notes/` - Research questions and working notes
- `research/` - Research notes, findings, and analysis
- `quotes/` - Collected quotes organized by topic or article
- `sources/` - PDFs, documents, and reference materials
- `docs/reference/` - Setup guides and documentation

## Workflow

1. Create/edit articles in `drafts/`
2. Use Cursor Chat with session boilerplate from `prompts/session-boilerplate.md`
3. Reference research from `research/` and quotes from `quotes/`
4. Merge approved changes to `articles/`
5. Commit with clear messages following format: `type(scope): subject`

## Quick Start

### Starting a New Article

1. Create canonical file: `articles/article-title.md`
2. Create working draft: `drafts/article-title-edit-YYYY-MM-DD.md`
3. Open Cursor Chat and paste:
   - `prompts/session-boilerplate.md`
   - Relevant task prompt from `prompts/tasks/`
   - Specify file and line range

### Common Tasks

- **Critique:** Use `prompts/tasks/critique.md`
- **Line Edit:** Use `prompts/tasks/line-edit.md`
- **Research:** Use `prompts/tasks/research.md`
- **Fact Check:** Use `prompts/tasks/fact-check.md`
- **Integrate Research:** Use `prompts/tasks/integrate-research.md`

## Documentation

See `docs/reference/` for:
- `POLITICAL_WRITING_SETUP_GUIDE.md` - Complete setup guide
- `POLITICAL_WRITING_QUICK_REFERENCE.md` - Quick reference card
- `POLITICAL_WRITING_TEMPLATES.md` - Ready-to-use templates

## Key Principles

1. **Canonical = Frozen** - Never edit `articles/` directly
2. **Work in Drafts** - All editing in `drafts/`
3. **Use Prompts** - Always paste session boilerplate
4. **Be Specific** - "lines 45-67" not "this section"
5. **Reference Context** - Mention context files in prompts
6. **Support with Research** - Use materials from `research/` and `quotes/`
