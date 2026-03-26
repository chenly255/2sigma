# First-Time Onboarding

When no `_user_profile.md` is found in the course folder or its parent directory, run this onboarding flow before generating any content.

## Onboarding Questions

Ask all questions in a single interaction. Present them as a structured set of choices.

### Q1: Language

> What language do you prefer for learning documents?

- Chinese (中文)
- English
- Japanese (日本語)
- Other (let user specify)

### Q2: Background

> What is your primary field/background? This helps me choose better analogies.

- Natural sciences (biology, chemistry, physics, medicine...)
- Engineering / Computer science
- Social sciences / Humanities
- Business / Finance
- Student (specify grade level or major)
- Other (let user specify)

### Q3: Document Length

> How long do you prefer each learning document to be?

- Short (~600 words) — quick reads, good for busy schedules
- Medium (~1000 words) — **recommended**, balanced depth and readability
- Long (~1800 words) — detailed exploration, fewer total documents

### Q4: Paper/Book Source (ask only if mode is Paper Reading or Exam Review)

> How do you usually access papers or books?

- I have a PDF file I can provide
- I use Zotero (with MCP integration)
- Search online (I'll give you a title or DOI)
- Other

If the user selects PDF, inform them about the PDF conversion tool:
> When you provide a PDF, I can split it into per-section markdown files for easier navigation. This requires `uv` to be installed. I'll guide you through it when needed.

If the user selects Zotero, note this in the profile. The skill will try Zotero MCP tools first (e.g., `zotero_search_items`, `zotero_get_item_fulltext`). If Zotero tools are not available at runtime, fall back to online search.

### Q5: Learning Goal (optional, ask if context is unclear)

> What's your goal with this topic?

- Quick overview (just need the gist)
- Systematic mastery (deep understanding)
- Practical application (need to use it for work/study)
- Exam preparation

## Saving the Profile

After collecting answers, write `_user_profile.md` in the course folder:

```markdown
# User Profile

> Created: YYYY-MM-DD
> Last updated: YYYY-MM-DD

## Preferences

- **Language**: [user's choice]
- **Background**: [user's field]
- **Document length**: [short/medium/long with word count]
- **Paper source**: [PDF / Zotero / Online / Other]
- **Learning goal**: [overview / mastery / application / exam prep]

## Background Details

[Any additional context the user shared, e.g., "biology major, 3rd year", "high school student preparing for college entrance exam"]
```

## Returning Users

On subsequent sessions:

1. Check for `_user_profile.md` in the current course folder.
2. If not found, check the parent directory (covers multiple courses under one root).
3. If found, read it silently. Do NOT re-ask preference questions.
4. If the user says "update my preferences" or similar, re-run relevant questions and update the file.

## Copying Profiles Across Courses

When creating a new course folder, if a `_user_profile.md` exists in the parent directory or a sibling course folder, copy it to the new course folder automatically. Briefly notify the user:

> Using your saved preferences from [previous course]. Say "update preferences" if you want to change anything.
