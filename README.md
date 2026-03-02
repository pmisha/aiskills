# AI Skills

A provider-agnostic library of reusable AI skills, prompt templates, and agent configurations. Write a skill once — run it with Claude, Gemini, OpenAI, or any other provider.

## Structure

```
aiskills/
├── skills/                # All skills — flat, no provider subdirectories
│   ├── summarize.md
│   └── extract-json.md
├── agents/                # One config file per provider
│   ├── claude.json
│   └── gemini.json
├── prompts/
│   ├── system/            # Shared system prompts
│   ├── templates/         # Reusable prompt templates
│   └── chains/            # Multi-step prompt chains
├── tools/
│   ├── mcp/               # MCP server tool definitions
│   └── functions/         # Function/tool calling definitions
├── tests/                 # Skill tests
└── docs/                  # Documentation and guides
```

## Getting Started

1. Copy `.env.example` to `.env` and add your API keys.
2. Browse `skills/` for ready-to-use skills.
3. Pick a provider config from `agents/` to run them.
4. See `docs/adding-a-skill.md` to write your own.

## Supported Providers

| Provider  | Config               |
|-----------|----------------------|
| Anthropic | `agents/claude.json` |
| Google    | `agents/gemini.json` |

Adding a new provider takes one config file in `agents/`.

## Contributing

See [`docs/adding-a-skill.md`](docs/adding-a-skill.md) for the full guide.
