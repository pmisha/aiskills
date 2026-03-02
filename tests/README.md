# Tests

Tests for skills, prompts, and agent configurations.

## Structure

```
tests/
├── claude/        # Tests for Claude-specific skills
├── gemini/        # Tests for Gemini-specific skills
└── shared/        # Tests for shared/cross-agent skills
```

## Running Tests

```bash
# Python (pytest)
pytest tests/

# Node (if applicable)
npm test
```

## Test Format

Each test file tests a skill by:
1. Loading the prompt template
2. Filling in test inputs
3. Calling the agent
4. Asserting the output matches expectations
