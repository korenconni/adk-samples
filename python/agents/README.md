# ADK Sample Agents

This directory contains sample agents built with the [Agent Development Kit (ADK)](https://github.com/google/adk-python).

## Overview

Each subdirectory contains a self-contained agent sample demonstrating different capabilities and patterns for building agents with ADK.

## Available Agents

| Agent | Description | Complexity |
|-------|-------------|------------|
| *(coming soon)* | | |

## Getting Started

### Prerequisites

- Python 3.11+
- [uv](https://docs.astral.sh/uv/) (recommended) or pip
- Google Cloud project with Vertex AI enabled

### Running an Agent

Each agent directory contains its own `README.md` with specific setup instructions. Generally:

```bash
# Navigate to the agent directory
cd <agent-name>

# Install dependencies
uv sync

# Set up environment variables
cp .env.example .env
# Edit .env with your configuration

# Run the agent
uv run adk run .
```

### Running with the ADK Web UI

```bash
uv run adk web
```

Then open your browser to `http://localhost:8000`.

## Structure

Each agent sample follows this structure:

```
agent-name/
├── README.md              # Agent-specific documentation
├── pyproject.toml         # Python project configuration
├── .env.example           # Example environment variables
└── agent_name/
    ├── __init__.py
    ├── agent.py           # Main agent definition
    └── ...                # Additional modules
```

## Contributing

See the root [README.md](../../README.md) and [CONTRIBUTING.md](../../CONTRIBUTING.md) for contribution guidelines.

When adding a new agent sample:
1. Create a new directory under `python/agents/`
2. Follow the structure outlined above
3. Include a comprehensive `README.md`
4. Add tests under a `tests/` subdirectory
5. Update the table in this file
