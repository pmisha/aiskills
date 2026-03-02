# AI Skills

A multi-agent AI skills library for Claude, Gemini, and other AI agents.

## Structure

```
aiskills/
├── .claude/
│   └── commands/          # Claude Code slash command skills
├── agents/
│   ├── claude/            # Claude agent configurations & system prompts
│   ├── gemini/            # Gemini agent configurations
│   └── shared/            # Cross-agent shared configs
├── skills/
│   ├── claude/            # Claude-specific skills
│   ├── gemini/            # Gemini-specific skills
│   └── shared/            # Skills usable across multiple agents
├── prompts/
│   ├── system/            # System prompts per agent/use case
│   ├── templates/         # Reusable prompt templates
│   └── chains/            # Multi-step prompt chains
├── tools/
│   ├── mcp/               # MCP server tool definitions
│   └── functions/         # Function/tool calling definitions
├── tests/                 # Tests for skills and prompts
├── docs/                  # Documentation and guides
└── config/                # Shared configuration files
```

## Getting Started

1. Copy `.env.example` to `.env` and fill in your API keys.
2. Browse `skills/` for ready-to-use skills.
3. See `docs/` for guides on each agent.

## Agents

| Agent   | Provider  | Config Location      |
|---------|-----------|----------------------|
| Claude  | Anthropic | `agents/claude/`     |
| Gemini  | Google    | `agents/gemini/`     |

## Contributing

- Add new skills under `skills/<agent>/` or `skills/shared/` if cross-agent compatible.
- Follow the naming convention: `<skill-name>.md` for prompt-based skills, `<skill-name>.py` for code-based skills.
- Document each skill with a header comment describing its purpose, inputs, and outputs.
