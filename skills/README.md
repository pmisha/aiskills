# Skills

All skills live directly in this directory. Skills are agent-agnostic and work across any provider.

## File Format

Prompt-based skills use `.md` files with a header comment block:

```markdown
<!--
Name: Skill Name
Description: What the skill does
Inputs: {{variable_one}}, {{variable_two}}
-->

Prompt body using {{variable_one}} and {{variable_two}}...
```

Code-based skills use `.py` or `.js` files.

## Adding a Skill

See `docs/adding-a-skill.md` for the full guide.
