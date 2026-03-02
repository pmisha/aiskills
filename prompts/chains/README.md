# Prompt Chains

Multi-step prompt sequences where the output of one step feeds the next.

## Structure

Each chain is a folder containing:
- `chain.json` — step definitions and order
- `step-1.md`, `step-2.md`, ... — individual step prompts

## Example `chain.json`

```json
{
  "name": "research-and-summarize",
  "description": "Research a topic then produce a summary",
  "steps": [
    { "id": "step-1", "prompt": "step-1.md", "output_var": "research" },
    { "id": "step-2", "prompt": "step-2.md", "input_var": "research", "output_var": "summary" }
  ]
}
```
