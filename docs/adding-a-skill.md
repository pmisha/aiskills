# How to Add a New Skill

## 1. Choose the right location

| Scenario | Location |
|---|---|
| Works with any AI agent | `skills/shared/` |
| Claude-specific | `skills/claude/` |
| Gemini-specific | `skills/gemini/` |

## 2. Create the skill file

For prompt-based skills, create a `.md` file with a header block:

```markdown
<!--
Name: Your Skill Name
Description: What it does
Inputs: {{input1}} - description, {{input2}} - description
Compatible: claude, gemini   (or just one)
-->

Your prompt here using {{input1}} and {{input2}}.
```

## 3. Add a Claude Code slash command (optional)

If you want the skill accessible via `/skill-name` in Claude Code:

Create `.claude/commands/skill-name.md`:

```markdown
# Skill Name

Brief description of what this skill does.

## Usage

$ARGUMENTS

---

[Paste or reference your skill prompt here]
```

## 4. Test it

Add a test in `tests/shared/` or `tests/<agent>/` to verify the skill works as expected.
