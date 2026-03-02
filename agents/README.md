# Agents

Agent configuration files for each provider. Each file follows the same schema regardless of provider.

## Schema

| Field | Description |
|---|---|
| `provider` | Provider identifier (`anthropic`, `google`, `openai`, etc.) |
| `model` | Model ID string |
| `max_tokens` | Maximum output tokens |
| `temperature` | Sampling temperature |
| `system_prompt_file` | Path to the system prompt (relative to repo root) |
| `description` | Human-readable description |

## Adding an Agent

Create `agents/<name>.json` using the schema above. Point `system_prompt_file` at `prompts/system/default.md` or a custom prompt if needed.
