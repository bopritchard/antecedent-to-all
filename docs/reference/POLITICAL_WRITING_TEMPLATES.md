# Political Writing Repository — Ready-to-Use Templates

Copy these files directly into your new political writing repository.

---

## `.cursorrules` (Root Directory)

```markdown
# Political Writing Project Rules

## File Structure
- `articles/` contains CANONICAL (frozen) articles. Do not rewrite or propose edits to them.
- All writing/editing happens in `drafts/` working copies.
- Maintain exact voice, cadence, and political framing found in canonical text.

## Writing Style
- Prefer active voice and concrete examples
- Use precise political terminology (see context/terminology-guide.md)
- Cite sources accurately
- Maintain consistent framing throughout

## Editing Scope
- CRITIQUE: numbered notes on clarity/logic/rhythm. No rewrites unless asked.
- LINE-EDIT: surgical changes only; preserve meaning & cadence.
- RESEARCH: provide verifiable citations; no fabricated quotes.
- FACT-CHECK: verify claims, dates, statistics, quotes.

## Red Flags to Call Out
- Unintended political claims or implications
- Drift from established voice
- Over-explanation that weakens argument
- Logical inconsistencies
- Unsupported assertions
- Missing citations for claims

## When Suggesting Changes
- Output unified diff patches against the drafts/* file
- Never "continue the article"; only revise the provided section on request
- Quote canonical lines only when necessary; otherwise reference by heading/line
```

---

## `context/writing-voice.md`

```markdown
# Writing Voice Guide

## Core Voice Principles
- Clear, direct, precise
- Evidence-based arguments
- Acknowledges complexity
- Respectful but unflinching

## Do
- Use active voice
- Prefer concrete examples
- Let evidence speak
- Define key terms early
- Maintain consistent framing

## Don't
- Don't stack synonyms
- Don't explain metaphors immediately
- Don't shift register mid-paragraph
- Don't use jargon without context
- Don't make unsupported claims

## Political Writing Specifics
- Establish framing early
- Cite sources for claims
- Acknowledge nuance
- Avoid false binaries
- Use precise terminology

## Micro-Rules
- One main idea per paragraph
- Pronouns must track unambiguously
- Italics for emphasis sparingly (max one per paragraph)
- Use specific examples, not generic statements
- Quote sources precisely with attribution
```

---

## `context/author-intent.md`

```markdown
# Author Intent & Political Framing

## Core Mission
[Define your political perspective, goals, and what you're trying to accomplish]

Example:
- Exposing how political systems maintain power
- Advocating for specific policy changes
- Analyzing political rhetoric and framing
- Documenting political history/patterns

## Key Themes
- [Theme 1: e.g., "Power structures and their maintenance"]
- [Theme 2: e.g., "Rhetorical framing and manipulation"]
- [Theme 3: e.g., "Historical patterns and cycles"]

## Target Audience
[Who are you writing for?]
- General public interested in politics
- Policy makers and activists
- Academics and researchers
- Specific political community

## What You're NOT Doing
- [What you're avoiding]
- [What you're not trying to accomplish]

## Political Lens
[Your specific political framework, ideology, or perspective]

Example:
- Critical analysis of power structures
- Democratic socialist perspective
- Libertarian framework
- Non-partisan policy analysis
- Historical materialist analysis
```

---

## `context/terminology-guide.md`

```markdown
# Terminology Guide

## Key Terms (Define Once, Use Consistently)

**Power Structure:** [Your definition]
- Use when: [context]
- Avoid: [common misuse]

**Political Framing:** [Your definition]
- Use when: [context]
- Avoid: [common misuse]

**Institution:** [Your definition]
- Use when: [context]
- Avoid: [common misuse]

## Preferred Language
- Use "power structure" instead of "the system" (more precise)
- Prefer "political framing" over "narrative" (more specific)
- Avoid "establishment" (too vague/loaded)

## Political Framing Terms
- [Your specific terminology]
- [How you frame political concepts]
- [Preferred alternatives to common terms]

## Terms to Avoid
- [Overly loaded terms]
- [Ambiguous language]
- [Jargon without definition]
```

---

## `prompts/session-boilerplate.md`

```markdown
CONTEXT / GUARDRAILS
- Files under articles/ are CANONICAL. Do not rewrite or propose edits to them.
- All writing/editing happens in drafts/ working copies.
- Maintain exact voice, cadence, and political framing found in canonical text.
- Quote canonical lines only when necessary; otherwise reference by heading/line.
- When suggesting changes, output unified diff patches against the drafts/* file.
- Never "continue the article"; only revise the provided section on request.

REFERENCE FILES:
- context/writing-voice.md
- context/author-intent.md
- context/terminology-guide.md
```

---

## `prompts/tasks/critique.md`

```markdown
TASK: Targeted critique only.
Scope: the selected section in drafts/<file>.md
Deliverable: numbered notes on:
- Clarity (is the argument clear?)
- Logic (does it flow logically?)
- Evidence (are claims supported?)
- Rhythm (does it read well?)
- Political framing (is it consistent?)

Do NOT rewrite sentences unless asked.
```

---

## `prompts/tasks/line-edit.md`

```markdown
TASK: Surgical line editing.
Scope: the selected section in drafts/<file>.md
Deliverable:
- Minimal, precise changes
- Preserve meaning & cadence
- Maintain political framing
- Show diff format (what changed, why)

Focus on:
- Clarity
- Precision
- Flow
- Voice consistency
```

---

## `prompts/tasks/research.md`

```markdown
TASK: Research and fact-checking.
Scope: claims in drafts/<file>.md
Deliverable:
- Verify claims, statistics, dates
- Provide verifiable citations
- Flag unsupported assertions
- Suggest sources for missing citations

Requirements:
- Use credible sources
- Provide links or citations
- No fabricated quotes or data
- Note any uncertainty or conflicting information
```

---

## `prompts/tasks/fact-check.md`

```markdown
TASK: Fact-checking pass.
Scope: entire drafts/<file>.md
Deliverable:
- Verify all claims
- Check dates, statistics, quotes
- Verify source citations
- Flag any unverified assertions

Format:
- [Line X] Claim: "..." — Status: [Verified/Unverified/Needs Citation]
- [Line Y] Statistic: "..." — Source: [if provided, verify; if missing, flag]
```

---

## `prompts/tasks/continuity-check.md`

```markdown
TASK: Continuity check across articles.
Scope: drafts/<file>.md against articles/
Deliverable:
- Flag contradictions with previous articles
- Note inconsistencies in framing
- Suggest cross-references
- Check terminology consistency

Focus on:
- Political framing consistency
- Terminology usage
- Argument coherence across series
- Cross-referencing opportunities
```

---

## `articles/series-page.md` (Template)

```markdown
# [Series Title]

![Series Image](IMAGE_URL_HERE)

[Series description]

---

## The Series

1. **[Article Title](link)**
   *Subtitle*

   [Brief description]

2. **[Article Title](link)**
   *Subtitle*

   [Brief description]

---

*Each article builds on the last. They are not isolated observations; they are one reading.*
```

---

## `articles/ARTICLE_TEMPLATE.md`

```markdown
# Article Title
*Subtitle or tagline*

---

[Series connection if applicable]

- [Previous article](link) — [what it established]
- [Previous article](link) — [what it showed]

This one [what this article does].

---

## Opening Section

[Engaging opening - hook, question, scene, or statement]

---

## Main Sections

### Section Heading

[Content]

---

## Conclusion

[Wrap-up that ties back to opening and main argument]

---

[Sources/Citations if needed]
```

---

## `README.md` (Template)

```markdown
# [Project Name]

[Brief project description]

## Structure

- `articles/` - Published/canonical articles (frozen)
- `drafts/` - Working copies for editing
- `context/` - Context files for AI (voice, intent, terminology)
- `prompts/` - Reusable prompts and templates
- `notes/` - Research and thinking space
- `sources/` - PDFs, documents, references

## Workflow

1. Create/edit articles in `drafts/`
2. Use Cursor Chat with session boilerplate
3. Merge approved changes to `articles/`
4. Commit with clear messages

See `POLITICAL_WRITING_SETUP_GUIDE.md` for complete setup instructions.
```

---

## Quick Setup Script

Create `scripts/setup-new-repo.sh`:

```bash
#!/bin/bash

# Create directory structure
mkdir -p articles drafts context prompts/tasks notes sources scripts

# Create core files
touch .cursorrules
touch README.md
touch context/writing-voice.md
touch context/author-intent.md
touch context/terminology-guide.md
touch prompts/session-boilerplate.md
touch prompts/tasks/{critique,line-edit,research,fact-check,continuity-check}.md

echo "Repository structure created!"
echo "Next steps:"
echo "1. Copy templates from POLITICAL_WRITING_TEMPLATES.md"
echo "2. Customize context files with your voice and intent"
echo "3. Start writing!"
```

---

## Usage Example

### Starting a New Article

1. **Create files:**
   ```bash
   touch articles/01-article-title.md
   cp articles/01-article-title.md drafts/01-article-title-edit-$(date +%Y-%m-%d).md
   ```

2. **Open in Cursor:**
   - Open `drafts/01-article-title-edit-YYYY-MM-DD.md`
   - Open Cursor Chat

3. **Paste prompts:**
   ```
   [Paste session-boilerplate.md]

   [Paste task prompt - e.g., critique.md]

   I'm working on lines 1-50 in drafts/01-article-title-edit-YYYY-MM-DD.md
   ```

4. **Work iteratively:**
   - Use critique for feedback
   - Use line-edit for changes
   - Use research for citations
   - Use fact-check before publishing

5. **Merge back:**
   - Review changes
   - Copy to `articles/01-article-title.md`
   - Commit: `git commit -m "article: merged edits YYYY-MM-DD"`

---

All templates are ready to copy and customize for your political writing project!
