# Extending: Adding New Learning Modes

This skill is designed to be extensible. You can add new learning modes by following the template below.

## Mode Definition Template

To add a new mode, append a section to `references/learning-modes.md` following this structure:

```markdown
## Mode N: [Mode Name]

### Goal
[One sentence: what this mode helps the user achieve.]

### Trigger
[What user expressions activate this mode. Add these to the mode table in SKILL.md as well.]

### Input Processing
[How to acquire/prepare the source material for this mode.]

### Document Sequence
[Define the document sequence:]
- **01.md — [First document purpose]**
  - What to cover
  - What NOT to cover
  - Question focus for this stage

- **02.md — [Second document purpose]**
  - ...

- **03.md+ — [Pattern for subsequent documents]**
  - ...

### 2-Sigma Application
[How does the mastery loop apply to this mode? What's different from the default?]

### Style
[Any mode-specific writing rules. Reference writing-style.md for defaults.]
```

## Steps to Add a New Mode

1. **Write the mode definition** in `references/learning-modes.md` using the template above.
2. **Update the mode table** in `SKILL.md` (Step 1: Detect Mode) to include the new trigger expressions.
3. **Add mode-specific style rules** to `references/writing-style.md` if the mode needs different code/terminology handling.
4. **Test** by triggering the skill with the new mode's trigger expressions.

## Example: Adding a "Debate Preparation" Mode

```markdown
## Mode 7: Debate Preparation

### Goal
Help user understand both sides of a topic deeply enough to argue either position.

### Trigger
"Help me prepare for a debate about X", "What are the arguments for and against X"

### Document Sequence
- **01.md — The landscape**: Present the core disagreement, why people care, main camps
- **02.md — Side A deep dive**: Strongest arguments, evidence, common rebuttals
- **03.md — Side B deep dive**: Same structure for the opposing view
- **04.md+ — Cross-examination**: Practice questions from both sides

### 2-Sigma Application
Instead of testing understanding of facts, test ability to argue both sides.
Questions should ask user to argue AGAINST their natural position.

### Style
Present both sides fairly. No editorial bias. Use "Side A argues..." not "The correct view is..."
```

## Design Principles for New Modes

- **Every mode should have a clear document sequence.** The user should know what to expect.
- **Every mode uses the mastery loop.** Questions + feedback + adaptive progression.
- **Modes can share components.** For example, a new mode might use Mode 2's concept explanation style for part of its sequence.
- **Keep modes focused.** If a mode tries to do too many things, consider splitting it.
