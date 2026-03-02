# Prompt Templates

Reusable prompt fragments and templates.

## Conventions

- Use `{{variable_name}}` for placeholders.
- Name files descriptively: `summarize.md`, `extract-json.md`, `translate.md`.
- Include a comment block at the top of each template:

```
<!--
Name: Template Name
Description: What this template does
Variables: {{var1}} - description, {{var2}} - description
Compatible: claude, gemini, openai
-->
```
