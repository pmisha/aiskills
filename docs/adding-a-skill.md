# How to Add a New Skill

## 1. Create the skill file

Add a `.md` file directly in `skills/`. Skills are agent-agnostic by default.

For prompt-based skills, include a header block:

```markdown
<!--
Name: Your Skill Name
Description: What it does
Inputs: {{input1}} - description, {{input2}} - description
-->

Your prompt here using {{input1}} and {{input2}}.
```

For code-based skills, use `.py` or `.js`.

## 2. Add a Claude Code slash command (optional)

If you want the skill accessible via `/skill-name` in Claude Code, create `.claude/commands/skill-name.md`:

```markdown
# Skill Name

Brief description of what this skill does.

## Usage

$ARGUMENTS

---

[Paste or reference your skill prompt here]
```

## 3. Test it

Add a test file in `tests/` named `test-<skill-name>.py` (or `.js`) to verify the skill works as expected.
