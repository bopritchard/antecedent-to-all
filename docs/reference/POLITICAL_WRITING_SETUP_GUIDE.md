# Political Writing Repository — Complete Setup Guide

A comprehensive guide for setting up a Cursor-based political writing project, adapted from proven patterns in theological writing workflows.

---

## 📁 Recommended Directory Structure

```
political-writing-repo/
├── README.md                    # Project overview
├── .cursorrules                 # Cursor-specific rules
├── articles/                    # Published/canonical articles (frozen)
│   ├── 01-article-title.md
│   └── series-page.md
├── drafts/                      # Working copies for editing
│   └── 01-article-title-edit-YYYY-MM-DD.md
├── context/                     # Context files for AI
│   ├── writing-voice.md
│   ├── political-frameworks.md
│   ├── author-intent.md
│   ├── rhetorical-frames.md
│   └── terminology-guide.md
├── prompts/                    # Reusable prompts and templates
│   ├── session-boilerplate.md
│   ├── editing_template.md
│   └── tasks/
│       ├── critique.md
│       ├── line-edit.md
│       ├── research.md
│       ├── fact-check.md
│       └── continuity-check.md
├── notes/                      # Research and thinking space
│   ├── research-questions.md
│   ├── sources.md
│   ├── quotes.md
│   └── working-notes.md
├── sources/                    # PDFs, documents, references
└── scripts/                    # Helper scripts (optional)
    └── new-article.sh
```

---

## 🎯 Core Principles (Canonical vs Working)

### The Two-Tier System

**Canonical (Frozen):** `articles/` contains published/final articles. Treat as read-only during normal work.

**Working (Editable):** `drafts/` holds per-session working copies you actually edit.

### Why This Works

- AI "sees" canonical text but never rewrites it unless you explicitly work in `drafts/`
- You keep exact wording stable while getting AI help for critique, research, and edits
- Prevents accidental drift from your established voice
- Clear separation between "source of truth" and "work in progress"

---

## 📝 Writing Style Guide

### Voice & Tone

**Do:**
- Write with clarity and precision
- Use active voice
- Prefer concrete examples over abstractions
- Let evidence speak; avoid over-explanation
- Maintain consistent political framing throughout
- Use precise terminology (define once, use consistently)

**Don't:**
- Don't stack synonyms for emphasis
- Don't explain metaphors immediately after using them
- Don't shift register mid-paragraph
- Don't use jargon without context
- Don't make claims without evidence

### Micro-Rules

- One main idea per paragraph
- Pronouns must track unambiguously to nearest named referent
- Italics for emphasis sparingly (max one per paragraph)
- Use specific examples, not generic statements
- Quote sources precisely with attribution

### Political Writing Specifics

- **Framing:** Establish your political lens early and consistently
- **Evidence:** Cite sources, data, or examples for claims
- **Nuance:** Acknowledge complexity; avoid false binaries
- **Audience:** Write for your intended reader (general public, policy makers, activists, etc.)
- **Terminology:** Define key terms early; use consistently

---

## 🤖 Cursor Setup Files

### `.cursorrules` File

Create this in your repo root:

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

### Context Files

#### `context/writing-voice.md`

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
```

#### `context/author-intent.md`

```markdown
# Author Intent & Political Framing

## Core Mission
[Define your political perspective, goals, and what you're trying to accomplish]

## Key Themes
- [Theme 1]
- [Theme 2]
- [Theme 3]

## Target Audience
[Who are you writing for?]

## What You're NOT Doing
- [What you're avoiding]
- [What you're not trying to accomplish]

## Political Lens
[Your specific political framework, ideology, or perspective]
```

#### `context/terminology-guide.md`

```markdown
# Terminology Guide

## Key Terms (Define Once, Use Consistently)

**Term 1:** [Definition]
- Use when: [context]
- Avoid: [common misuse]

**Term 2:** [Definition]
- Use when: [context]
- Avoid: [common misuse]

## Preferred Language
- Use X instead of Y
- Prefer A over B
- Avoid Z (too loaded/ambiguous)

## Political Framing Terms
- [Your specific terminology]
```

---

## 📋 Prompt Templates

### `prompts/session-boilerplate.md`

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

### `prompts/tasks/critique.md`

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

### `prompts/tasks/line-edit.md`

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

### `prompts/tasks/research.md`

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

### `prompts/tasks/fact-check.md`

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

### `prompts/tasks/continuity-check.md`

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

## 🔄 Daily Workflow

### Starting a New Article

1. **Create canonical file:**
   ```
   articles/01-article-title.md
   ```

2. **Create working draft:**
   ```
   drafts/01-article-title-edit-YYYY-MM-DD.md
   ```
   (Copy from canonical or start fresh)

3. **Open Cursor Chat:**
   - Paste `prompts/session-boilerplate.md`
   - Paste relevant task prompt
   - Specify file + line range

4. **Work in drafts/ only**

### Editing Existing Article

1. **Copy canonical to drafts:**
   ```
   articles/01-article-title.md → drafts/01-article-title-edit-YYYY-MM-DD.md
   ```

2. **Open Cursor Chat:**
   - Paste session boilerplate
   - Paste task prompt (critique, line-edit, etc.)
   - Work in drafts/

3. **Merge back when satisfied:**
   - Review changes carefully
   - Copy approved sections to canonical
   - Commit with message: `article: merged edits YYYY-MM-DD`

---

## 🎨 Article Format Template

```markdown
# Article Title
*Subtitle or tagline*

---

[Series connection if applicable]

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

## ✅ Quality Checklist

Before publishing:

- [ ] All claims are supported with evidence/citations
- [ ] Political framing is consistent throughout
- [ ] Terminology is used correctly and consistently
- [ ] Voice and tone are consistent
- [ ] Logic flows clearly
- [ ] No unsupported assertions
- [ ] Sources are cited accurately
- [ ] Cross-references to other articles are accurate
- [ ] Article stands alone (if not part of series)

---

## 🚀 Cursor-Specific Features

### Using Cursor Chat Effectively

1. **Always start with session boilerplate** - prevents accidental edits to canonical
2. **Be specific about scope** - "lines 45-67 in drafts/article.md"
3. **Use task prompts** - gives AI clear instructions
4. **Reference context files** - "see context/writing-voice.md"

### Cursor Snippets (Optional)

Create snippets in Cursor for:
- Session boilerplate
- Task prompts
- Article template
- Citation format

### Code References

When showing existing code/text:
```startLine:endLine:filepath
// content
```

When proposing new text:
```markdown
# content
```

---

## 📚 Additional Resources

### For Research
- `notes/research-questions.md` - Track questions to investigate
- `notes/sources.md` - List of sources
- `notes/quotes.md` - Useful quotes
- `sources/` - PDFs, documents

### For Series Work
- `articles/series-page.md` - Index of series articles
- Use continuity-check task to maintain consistency

### For Editing
- Use critique for big-picture feedback
- Use line-edit for precise changes
- Use fact-check before publishing
- Use research to fill gaps

---

## 🎯 Quick Start Commands

### Create New Article
```bash
# Create canonical
touch articles/01-article-title.md

# Create working draft
cp articles/01-article-title.md drafts/01-article-title-edit-$(date +%Y-%m-%d).md
```

### Start Editing Session
1. Open `drafts/your-file.md`
2. Open Cursor Chat
3. Paste session boilerplate
4. Paste task prompt
5. Specify scope

### Merge Back
1. Review `drafts/your-file.md`
2. Copy approved changes to `articles/your-file.md`
3. Commit: `git commit -m "article: merged edits YYYY-MM-DD"`

---

## 💡 Pro Tips

1. **Use the two-tier system religiously** - keeps canonical safe
2. **Be specific in prompts** - "critique lines 45-67" not "improve this"
3. **Reference context files** - helps AI understand your voice
4. **Use task prompts** - gives clear instructions
5. **Fact-check before publishing** - use fact-check task
6. **Maintain terminology consistency** - update terminology-guide.md
7. **Track research questions** - use notes/research-questions.md
8. **Use continuity-check for series** - maintains consistency

---

This setup gives you:
- ✅ Clear separation of canonical vs working files
- ✅ Reusable prompts and templates
- ✅ Context files for consistent voice
- ✅ Task-specific prompts for focused work
- ✅ Quality checklists
- ✅ Cursor-optimized workflow

Adapt these patterns to your specific political writing needs!
