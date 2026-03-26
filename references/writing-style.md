# Writing Style Guide

## Tone

Write like a knowledgeable friend explaining something over coffee — not a textbook, not a tech blog, not a lecture.

- **Intuition first, definition second.** Start with a concrete scenario or question, build understanding, then introduce the formal term.
- **One concept per paragraph.** Don't stack multiple new ideas together.
- **Every abstraction gets a concrete example.** If you can't think of a good example, the explanation is too abstract.
- **Conversational connectors.** Use phrases like "you might wonder...", "here's the thing...", "think of it this way..." to maintain a dialogue feel.

## Document Length

Follow the user's preference from `_user_profile.md`:

| Preference | Target | Behavior |
|-----------|--------|----------|
| Short | ~600 words | One core idea, 1-2 examples, 2 questions |
| Medium | ~1000 words | One core idea with depth, 2-3 examples, 2-3 questions |
| Long | ~1800 words | One core idea with full context, multiple examples, 3 questions |

Default to **medium (~1000 words)** if no preference is set.

## Universal Analogy Library

Use analogies that work across backgrounds. Draw from everyday experiences:

| Abstract Concept | Universal Analogy |
|-----------------|-------------------|
| Layered architecture | Building a house: foundation → frame → walls → decor |
| Caching / Memoization | Sticky notes on your desk vs. looking up the file cabinet every time |
| API / Interface | Restaurant menu: you pick items, the kitchen handles the rest |
| Pipeline / Workflow | Assembly line: each station does one job, passes to the next |
| Abstraction | TV remote: you press "volume up" without knowing the circuit inside |
| Search / Indexing | Library card catalog vs. scanning every bookshelf |
| Version control | Save points in a video game |
| Feedback loop | Thermostat: measure → compare → adjust → repeat |
| Training / Optimization | Learning to ride a bike: wobble → adjust → improve → automatic |
| Classification | Sorting mail: personal / bills / ads / junk |
| Compression | Packing a suitcase: fold and arrange to fit more |
| Encryption | A letter in a locked box — only the key holder can read it |
| Distributed system | A team project: divide work, coordinate, merge results |
| Sampling / Statistics | Tasting soup: one spoonful tells you about the whole pot |
| Overfitting | Memorizing answers vs. understanding the subject |

### Background-Specific Analogies

If the user's profile indicates a specific field, prefer analogies from that field:

- **Biology/Medicine**: DNA→source code, protein→program, cell→container, immune system→firewall, mutation→bug
- **Engineering/CS**: Already speaks the language — use fewer analogies, more precise terminology
- **Business/Finance**: Portfolio→diversification, market→supply-demand, ROI→optimization metric
- **Student (general)**: School/classroom analogies, sports analogies, social media analogies

When uncertain whether the user knows an analogy source, just use a universal one.

## Code & Terminology Rules

Rules vary by mode:

### Concept Learning / Domain Introduction / Paper Reading

- **No code blocks.** No pseudocode, no function signatures, no imports.
- **No internal implementation names.** Describe what it does in natural language.
- **Technical terms in English are OK** when they're standard vocabulary (e.g., API, GPU, transformer, gradient descent). Don't force-translate established terms.
- **Overall feel**: Like reading a well-written popular science article.

### Tech Stack Learning

- **Minimal code OK** when explaining a tool's usage — but keep it short (<10 lines).
- **Focus on "why" not "how"** in code comments.
- **Avoid framework internals** unless the user specifically asks.

### Code Repo Reading

- **Code snippets OK** when pointing at specific design decisions (<20 lines).
- **Always add comments** explaining the "why", not just restating the code.
- **Describe modules by function**, not by file path.

### Exam Review

- **No code** unless the exam is about programming.
- **Match exam style**: if the exam uses formal language, the questions should too.

## Formatting

- Use **bold** for key terms on first introduction.
- Use tables for comparisons (keep them simple, natural language content).
- Use `>` blockquotes for important takeaways or summaries.
- Avoid excessive bullet points — prefer flowing prose for explanations.
- Headings: use `##` for major sections within a document. Don't go deeper than `###`.
