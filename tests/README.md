# Tests

Tests for skills and agent configurations. All tests live directly in this directory.

## Running Tests

```bash
# Python
pytest tests/

# Node
npm test
```

## Writing a Test

Each test should:

1. Load the skill template from `skills/<skill-name>.md`
2. Fill in the `{{variable}}` placeholders with test inputs
3. Call the agent using the config from `agents/<agent>.json`
4. Assert the output matches expected shape or content

## File Naming

Use `test-<skill-name>.py` or `test-<skill-name>.js`. Example: `test-summarize.py`.
