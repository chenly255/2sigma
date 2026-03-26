# Learning Modes

## Mode 1: Paper Reading

### Goal
Turn an unfamiliar research paper into knowledge the user can explain in their own words.

### Paper Acquisition (in priority order)

1. **User provides PDF** → Convert using `scripts/pdf_to_sections.py`. This creates a folder of per-section markdown files.
2. **User has Zotero** (profile says so) → Try Zotero MCP tools: `zotero_search_items` → `zotero_get_item_children` → read markdown attachment or `zotero_get_item_fulltext`. If Zotero tools unavailable, fall back to option 3.
3. **User provides title/DOI** → Search via Semantic Scholar, PubMed, or web search. Try to find open-access full text.
4. **None of the above** → Ask the user to provide the paper content.

Learning notes are written to the user's specified folder, never into Zotero or the paper source.

### Document Sequence

**01.md — What problem is this paper solving?**
- Hook with a relatable analogy for the research background
- What did people do before this paper? (status quo)
- What's wrong with the status quo? (pain point)
- The core question this paper addresses (one sentence)
- No methods, no results yet
- Questions: confirm user understands the "why"

**02.md — The core idea (how do they solve it?)**
- Explain the paper's key insight using analogy
- How is it different from previous approaches?
- If complex prerequisites are needed, ask the user first before diving in
- Questions: confirm user grasps the core idea

**03.md+ — Deep dives (user chooses direction)**
- Key experimental results (only the most important conclusions)
- Important technical details
- Comparisons with other work
- Limitations and future impact
- Branch into subtopics using the knowledge tree

### Style
- Like a collaborator explaining a paper in the lab over coffee
- Focus on "what they wanted to do, how they thought of it, why they did it this way"
- Not a translation of the paper. Do not paraphrase paragraph by paragraph.

---

## Mode 2: Concept Learning

### Goal
Take a single concept from zero to "I can explain this to someone else."

### Document Sequence

**01.md — What is this concept, really?**
- Start with a concrete scenario or problem (not a definition)
- Build intuition with analogy
- Then give the formal definition
- Explain why this concept exists (what problem it solves)
- Questions: "Explain [concept] in your own words"

**02.md — Details and distinctions**
- Subtypes or variations of the concept
- Common misconceptions
- How it differs from related concepts
- Questions: comparison and distinction

**03.md+ — Application and connections**
- Real-world usage
- Relationship to other concepts
- Deeper mechanics (if user is interested)

### Style
- Intuition first, terminology second
- Every abstract point gets a life-like example

---

## Mode 3: Domain Introduction

### Goal
Build a knowledge framework for an entirely new field.

### Document Sequence

**00-roadmap.md — Learning Roadmap** (required)

```markdown
# [Domain] Learning Roadmap

## What You'll Learn
- [Core concept 1]: one-line description
- [Core concept 2]: one-line description
- ...

## Suggested Order
1. [Concept A] ← we start here
2. [Concept B] ← requires A
3. [Concept C] ← requires A and B
...

## Estimated Documents: ~X
```

**01.md — The core question of this field**
- Why does this field exist? What big question is it trying to answer?
- Connect to everyday experience
- Questions: confirm user understands the field's core concern

**02.md+ — Concept by concept, following the roadmap**
- Each document covers one concept
- Follow Mode 2 (Concept Learning) document structure
- Additionally emphasize connections between concepts
- After completing a concept, update `_progress.md` and ask which branch to explore next

### Style
- Like a mentor introducing a newcomer
- Forest first, then trees — always maintain the big picture

---

## Mode 4: Tech Stack Learning

### Goal
Help user understand a framework/tool's design philosophy and core usage.

### Document Sequence

**01.md — Why does this tool exist?**
- What was painful before this tool? (the problem)
- Core philosophy/design principle
- The simplest example (Hello World level)
- Questions: confirm user understands the tool's position

**02.md — Core concepts and workflow**
- Key concepts of the tool
- How they work together
- Walk through a concrete example end-to-end
- Questions: describe the workflow

**03.md+ — Deep dives**
- Common features/APIs
- Real project usage patterns
- Comparison with alternatives
- Best practices and common pitfalls

### Style
- Like an experienced colleague sharing their experience with the tool
- Code examples allowed but keep them short; comments explain "why" not "what"

---

## Mode 5: Code Repo Reading

### Goal
Make an unfamiliar codebase understandable. Same approach as reading a paper: core first, details on demand.

### Exploration Phase (before generating documents)

1. Browse project structure: directory tree, README, entry files, config files
2. Identify the project's core: what it does, how it's organized, key modules
3. Build knowledge tree by module/function, write to `_progress.md`

### Document Sequence

**01.md — What does this project do?**
- One sentence: what problem does this project solve?
- Core philosophy/approach (use analogy, like explaining a paper's "scientific question")
- Overall architecture: main modules and their responsibilities
- Simplified module relationship diagram (text description)
- No implementation details, no large code blocks
- Questions: confirm user understands project purpose and architecture

**02.md — Core workflow**
- Trace a typical user operation through the code (input → processing → output)
- Connect key modules, explain data flow
- Short code snippets OK (<20 lines) with comments explaining "why"
- Questions: describe an operation's execution path through the project

**03.md+ — Module deep dives (branching)**
- Let user choose which module to explore via `_progress.md`
- Each document focuses on one module:
  - What it's responsible for
  - Core components and what they do
  - How it interacts with other modules
  - Notable design decisions

### Paper+Code Cross-Reference
If the project has a companion paper (mentioned by user or cited in README), offer cross-referencing:
- Paper method → corresponding code module
- Code implementation detail → paper justification
- Ask user if they want this cross-referencing

### Style
- Like a colleague who knows the project walking you through the code
- Focus on "why this design" not line-by-line explanation

---

## Mode 6: Exam Review

### Goal
Help users consolidate and test their understanding of a book or study material through structured, progressive testing based on 2-sigma mastery learning.

### Input Processing

1. **User provides a book/textbook** (PDF, markdown, or text):
   - If PDF: convert using `scripts/pdf_to_sections.py`
   - If already structured: read directly
2. **Build chapter structure** from table of contents or section headings
3. **Generate `00-roadmap.md`** showing all chapters and key concepts

### Document Sequence

**00-roadmap.md — Book Overview & Test Plan**

```markdown
# [Book Title] — Exam Review Plan

## Chapters
1. [Chapter 1]: key concepts A, B, C
2. [Chapter 2]: key concepts D, E
...

## Review Strategy
- Chapter-by-chapter tests → Comprehensive test → Weak area drilling
- Estimated test documents: ~X

## Choose Your Path
- [ ] Full sequential review (recommended)
- [ ] Specific chapters only: [list]
- [ ] Jump to comprehensive test
```

**01.md — First Chapter Test**
- Brief context (2-3 sentences about what this chapter covers — not a summary)
- 5-8 questions of mixed difficulty:
  - 2-3 accessible (basic understanding, rephrase-level)
  - 2-3 application/analysis (apply concepts to new scenarios)
  - 1-2 synthesis (cross-concept or critical thinking)
- User answers in the file

**02.md — Feedback + Next Chapter**
- Feedback on chapter 1 answers (using the standard evaluation framework)
- Identify weak areas for later review
- Chapter 2 test questions
- Include 1-2 cross-chapter questions linking chapters 1 and 2

**Progressive Pattern**:
- Each subsequent test adds cross-chapter questions
- Weak areas from previous chapters reappear in new contexts
- Difficulty gradually increases as the user builds confidence

**Comprehensive Test** (after all chapters):
- Generate a comprehensive test covering all chapters
- Extra focus on previously weak areas
- Synthesis questions requiring connections across multiple chapters
- Simulate exam conditions if user requests

**Weak Area Drilling** (after comprehensive test):
- Generate targeted mini-tests for identified weak areas
- Provide brief explanations for concepts the user still struggles with
- Re-test until mastery or user is satisfied

### 2-Sigma Application in Exam Review

The key difference from learning modes:
- **Learning mode**: explain → test → feedback → next
- **Exam review**: test → feedback → explain gaps → re-test → next

This means:
- Start by testing, not teaching (the user has already read the material)
- Only explain when the user demonstrates a gap
- Explanations should be targeted and concise, not full lessons
- Track weak areas across all tests for spaced repetition effect

### Style
- More concise than learning mode (user already has the material)
- Questions should match actual exam style if the user specifies the exam type
- Include answer-key-style feedback: correct answer + brief explanation
