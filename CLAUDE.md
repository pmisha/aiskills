# CLAUDE.md

Instructions for Claude Code when working in this repository.

## Project Purpose

This repo contains AI skills, prompt templates, and agent configurations for multiple AI providers (Claude, Gemini, and others).

## Conventions

- **Skills**: Prompt-based skills use `.md` files; code-based skills use `.py` or `.js`.
- **Naming**: Use kebab-case for all file and folder names (e.g., `summarize-text.md`).
- **Agent-specific vs shared**: Place skills that only work with one agent under `skills/<agent>/`. Cross-compatible skills go in `skills/shared/`.
- **Prompts**: System prompts live in `prompts/system/`. Reusable templates in `prompts/templates/`.

## Key Directories

- `skills/` — Main library of AI skills
- `agents/` — Agent configuration files (models, parameters, system prompts)
- `prompts/` — Raw prompt templates
- `tools/` — Tool/function definitions for function calling and MCP
- `.claude/commands/` — Claude Code slash commands (skills invokable via `/skill-name`)

## Environment

- Copy `.env.example` to `.env` for local API keys.
- Never commit `.env` or files containing real API keys.

## Adding a New Skill

1. Decide: agent-specific or shared?
2. Create file in the appropriate `skills/<agent>/` or `skills/shared/` directory.
3. Add a header block with: description, inputs, outputs, and example usage.
4. If it should be a Claude Code slash command, add it to `.claude/commands/`.
