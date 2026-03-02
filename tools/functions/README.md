# Function / Tool Calling Definitions

JSON schemas and descriptions for tools used in function calling across agents.

## Format

Each file defines one or more tools as JSON following the provider's schema.

### Claude (Anthropic) tool format
```json
{
  "name": "tool_name",
  "description": "What the tool does",
  "input_schema": {
    "type": "object",
    "properties": {
      "param": { "type": "string", "description": "..." }
    },
    "required": ["param"]
  }
}
```

### Gemini (Google) tool format
```json
{
  "name": "tool_name",
  "description": "What the tool does",
  "parameters": {
    "type": "OBJECT",
    "properties": {
      "param": { "type": "STRING", "description": "..." }
    },
    "required": ["param"]
  }
}
```
