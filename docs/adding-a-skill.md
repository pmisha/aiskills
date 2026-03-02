# How to Add a New Skill

A skill is a reusable, self-contained prompt or script that teaches an AI agent how to perform a specific task — step by step, with your preferred methods, tools, and constraints. Skills are most valuable when you have:

- A repeatable workflow
- A process that requires consistency
- Domain knowledge the model doesn't inherently have
- Multi-step tasks that benefit from structure

---

## 1. Define the workflow

Before writing anything, clarify:

- **Purpose** — what the skill does and why
- **Inputs** — what the user (or caller) provides
- **Steps** — the exact sequence the model should follow
- **Output** — format, length, and quality criteria
- **Edge cases** — what to do when inputs are missing or ambiguous

---

## 2. Create the skill file

Add a file directly in `skills/`. Skills are agent-agnostic by default — no provider subdirectories.

**Prompt-based skills** use `.md` with a header comment block:

```markdown
<!--
Name: Your Skill Name
Description: What it does
Inputs: {{input1}} - description, {{input2}} - description
-->

Your prompt here using {{input1}} and {{input2}}.

Steps:
1. ...
2. ...

Output format: ...
```

**Code-based skills** use `.py` or `.js`.

---

## 3. Add supporting assets (optional)

If the skill relies on reference material, templates, or schemas, place them alongside the skill or in a dedicated subfolder:

```
skills/
├── my-skill.md
└── my-skill/
    └── schema.json   # or template.md, examples.md, etc.
```

---

## 4. Add a slash command (optional)

To invoke the skill via `/skill-name` in Claude Code, create `.claude/commands/skill-name.md`:

```markdown
# Skill Name

Brief description.

## Usage

$ARGUMENTS

---

[Skill prompt here]
```

---

## 5. Test it

Add a test in `tests/` named `test-<skill-name>.py` (or `.js`):

1. Load the template from `skills/<skill-name>.md`
2. Fill in `{{variables}}` with test inputs
3. Call the agent using a config from `agents/`
4. Assert the output matches expected shape or content

---

## 6. Iterate

Run the skill against varied inputs and refine the prompt until it behaves consistently. Pay particular attention to edge cases identified in step 1.
