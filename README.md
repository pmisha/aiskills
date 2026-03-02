# AI Skills

An agent-agnostic AI skills library. Skills work across Claude, Gemini, and other providers.

## Structure

```
aiskills/
├── .claude/
│   └── commands/          # Claude Code slash command skills
├── agents/                # One config file per provider
│   ├── claude.json
│   └── gemini.json
├── skills/                # All skills (flat, no subdirectories)
│   ├── summarize.md
│   └── extract-json.md
├── prompts/
│   ├── system/            # System prompts
│   ├── templates/         # Reusable prompt templates
│   └── chains/            # Multi-step prompt chains
├── tools/
│   ├── mcp/               # MCP server tool definitions
│   └── functions/         # Function/tool calling definitions
├── tests/                 # Tests for skills
└── docs/                  # Documentation and guides
```

## Getting Started

1. Copy `.env.example` to `.env` and fill in your API keys.
2. Browse `skills/` for ready-to-use skills.
3. See `docs/adding-a-skill.md` to add your own.

## Agents

| Agent  | Provider  | Config             |
|--------|-----------|--------------------|
| Claude | Anthropic | `agents/claude.json` |
| Gemini | Google    | `agents/gemini.json` |

## Contributing

- Add new skills directly in `skills/` — all skills are agent-agnostic.
- Use `<skill-name>.md` for prompt-based skills, `<skill-name>.py` for code-based.
- Include a header comment block with name, description, and inputs.
