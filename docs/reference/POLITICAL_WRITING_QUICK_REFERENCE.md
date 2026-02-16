# Political Writing — Quick Reference Card

## 🚀 Daily Workflow

### Start Editing Session
1. Open `drafts/your-file.md`
2. Open Cursor Chat
3. Paste:
   ```
   [session-boilerplate.md]
   [task-prompt.md]
   Working on lines X-Y in drafts/your-file.md
   ```

### Common Tasks

**Critique:**
```
[session-boilerplate.md]
[prompts/tasks/critique.md]
Critique lines 45-67 in drafts/article.md
```

**Line Edit:**
```
[session-boilerplate.md]
[prompts/tasks/line-edit.md]
Edit lines 45-67 in drafts/article.md for clarity
```

**Research:**
```
[session-boilerplate.md]
[prompts/tasks/research.md]
Research and verify claims in drafts/article.md
```

**Fact Check:**
```
[session-boilerplate.md]
[prompts/tasks/fact-check.md]
Fact-check entire drafts/article.md
```

**Continuity Check:**
```
[session-boilerplate.md]
[prompts/tasks/continuity-check.md]
Check continuity of drafts/article.md against articles/
```

---

## 📁 File Locations

- **Canonical:** `articles/` (frozen, read-only)
- **Working:** `drafts/` (editable)
- **Context:** `context/` (voice, intent, terminology)
- **Prompts:** `prompts/` (templates, tasks)
- **Notes:** `notes/` (research, questions)

---

## ✅ Pre-Publish Checklist

- [ ] All claims supported with evidence
- [ ] Political framing consistent
- [ ] Terminology used correctly
- [ ] Voice/tone consistent
- [ ] Logic flows clearly
- [ ] Sources cited accurately
- [ ] Fact-checked
- [ ] Stands alone (if not series)

---

## 🎯 Key Principles

1. **Canonical = Frozen** - Never edit `articles/` directly
2. **Work in Drafts** - All editing in `drafts/`
3. **Use Prompts** - Always paste session boilerplate
4. **Be Specific** - "lines 45-67" not "this section"
5. **Reference Context** - Mention context files in prompts

---

## 📝 Citation Format

**In-text:**
> "Quote" (Source, Date)

**Footnotes:**
[^1]: Source details

**Links:**
[Link text](URL)

---

## 🔄 Merge Process

1. Review `drafts/file.md`
2. Copy approved changes to `articles/file.md`
3. Commit: `git commit -m "article: merged edits YYYY-MM-DD"`

---

## 💡 Pro Tips

- Start every session with session-boilerplate.md
- Use task prompts for focused work
- Reference context files when needed
- Fact-check before publishing
- Use continuity-check for series

---

**Full guide:** See `POLITICAL_WRITING_SETUP_GUIDE.md`
**Templates:** See `POLITICAL_WRITING_TEMPLATES.md`
