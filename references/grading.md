# Question Design & Comprehension Evaluation

This is the core of the mastery learning loop. Questions are not quizzes — they are tools for deepening understanding and diagnosing comprehension gaps.

## Question Design Philosophy

**A good question makes the user THINK, not RECALL.**

- Never ask questions that can be answered by copying text from the document.
- Every question should require the user to process, rephrase, or apply what they learned.
- Questions serve two purposes: (1) help the user consolidate understanding, (2) give you signal about their comprehension level.

## Cross-Difficulty Pattern

Every question set follows a "confidence sandwich" to maintain motivation:

### Q1: Accessible (Confidence Builder)

The user should be able to answer this if they understood the document. Requires rephrasing, not copying.

Good examples:
- "Explain [concept] to a friend in your own words."
- "If someone asks you what [topic] is about, what would you say?"
- "What problem does [concept] solve? Why does it matter?"

Bad examples:
- "What is the definition of [X]?" (pure recall)
- "List three features of [X]." (copy-paste)

### Q2: Application (Deeper Understanding)

Requires using the concept in a new context the document didn't directly address.

Good examples:
- "Imagine you encounter [new scenario]. How would [concept] apply here?"
- "[A] and [B] seem similar. What's the key difference, and when would you choose one over the other?"
- "What would happen if [condition] changed? How would the outcome differ?"

### Q3: Challenge (Optional — Synthesis/Evaluation)

Only include when the topic warrants deeper thinking. Skip for simpler topics or early-stage documents.

Good examples:
- "What do you think is the biggest limitation of [approach]?"
- "If you combined [concept A from doc 2] with [concept B from this doc], what possibilities open up?"
- "Someone claims [plausible but wrong statement]. Do you agree? Why or why not?"

## Motivation-Aware Design

- **After a hard topic**: Make Q1 even easier than usual. The user needs a win.
- **After the user struggled**: Start the next set gentler. Don't punish.
- **Occasionally**: Include a fun/real-life connection question. Learning should feel rewarding.
- **Never**: Put two hard questions back-to-back. Never start with the hardest question.
- **Exam Review mode**: Can have more questions (5-8) with wider difficulty range, since the goal is testing.

## Comprehension Evaluation Framework

When reading the user's answers, do NOT score per question. Instead, evaluate holistically:

### Dimensions

| Dimension | What to look for |
|-----------|-----------------|
| **Core grasp** | Can they explain the main idea in their own words? |
| **Boundary awareness** | Do they know what the concept is NOT? |
| **Transfer ability** | Can they apply it to a new context? |
| **Connection making** | Do they link it to previously learned concepts? |

### Decision Logic

| Situation | Action |
|-----------|--------|
| Core grasp is solid | Advance to next topic |
| Core grasp OK but boundaries fuzzy | Advance, include clarification in feedback |
| Core grasp weak | Stay on this topic, explain differently |
| Specific misconception detected | Address it directly in feedback, then decide based on severity |

**Key principle**: The question is not "did they get the answer right?" but "would their current understanding block future learning?" If not blocking, correct the misconception in feedback and move forward.

## Feedback Format

Write at the top of the next document. Keep it under 150 words.

```markdown
## Previous Answers Feedback

**Overall**: [One sentence — e.g., "Solid grasp of the core idea, one point to clarify."]

**What you got right**: [1-2 sentences affirming correct understanding]

**To clarify**: [Only if needed. State the misconception briefly, then give the correct understanding. Skip this section entirely if everything was correct.]

→ Based on your understanding, this document [advances to X / revisits Y from a different angle].
```

### Rules

- Always start with what's correct. Positive reinforcement first.
- Only mention errors that matter for future learning. Ignore trivial imprecisions.
- Give the correct understanding, not just "this is wrong."
- If all answers are good, keep feedback to 2 sentences: affirmation + what's next.
- Do NOT reproduce the original questions in feedback (the user just answered them, they remember).

## 2-Sigma Adaptive Pacing

Like a 1-on-1 tutor, adapt to THIS user:

- **Breezing through**: Increase depth, add harder Q3s, cover more per document.
- **Struggling**: Slow down, more examples, easier Q1, consider splitting the next topic into two documents.
- **Inconsistent** (some topics easy, some hard): Note which concept types are harder, adjust analogies and examples for those.

Track cumulative performance in `_progress.md` with brief notes:

```markdown
- [x] Basics (01.md) — solid understanding
- [x] Branch B1 (03.md) — struggled with [concept], clarified in 04.md
```
