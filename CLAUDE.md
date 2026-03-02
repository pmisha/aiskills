# CLAUDE.md

Instructions for Claude Code when working in this repository.

## Project Purpose

This repo contains AI skills, prompt templates, and agent configurations for multiple AI providers (Claude, Gemini, and others).

## Conventions

- **Skills**: Prompt-based skills use `.md` files; code-based skills use `.py` or `.js`.
- **Naming**: Use kebab-case for all file and folder names (e.g., `summarize-text.md`).
- **All skills are agent-agnostic**: Skills go directly in `skills/` — no provider subdirectories.
- **Prompts**: System prompts live in `prompts/system/`. Reusable templates in `prompts/templates/`.

## Key Directories

- `skills/` — All skills (flat, no subdirectories)
- `agents/` — One config file per provider (e.g., `agents/claude.json`)
- `prompts/` — Prompt templates and system prompts
- `tools/` — Tool/function definitions for function calling and MCP
- `.claude/commands/` — Claude Code slash commands (skills invokable via `/skill-name`)

## Environment

- Copy `.env.example` to `.env` for local API keys.
- Never commit `.env` or files containing real API keys.

## Adding a New Skill

1. Create `skills/<skill-name>.md` with a header block (name, description, inputs).
2. Optionally add a Claude Code slash command in `.claude/commands/<skill-name>.md`.
3. Add a test in `tests/test-<skill-name>.py`.
