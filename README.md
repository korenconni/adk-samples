# ADK Samples

A collection of sample agents and applications built with [Google Agent Development Kit (ADK)](https://google.github.io/adk-docs/).

> This is a fork of [google/adk-samples](https://github.com/google/adk-samples).

## Overview

This repository contains ready-to-use sample agents demonstrating various capabilities of the ADK framework, including:

- **Multi-turn conversations** — Agents that maintain context across interactions
- **Tool use** — Agents that call external APIs and built-in tools
- **Multi-agent workflows** — Orchestration of multiple specialized agents
- **RAG (Retrieval-Augmented Generation)** — Agents grounded in custom knowledge bases

## Prerequisites

- Python 3.10+
- [Google ADK](https://pypi.org/project/google-adk/) (`pip install google-adk`)
- A Google Cloud project with the Vertex AI API enabled
- Application Default Credentials configured (`gcloud auth application-default login`)

> **Personal note:** I've been testing these samples with Python 3.11 — works great. Also confirmed working on Python 3.13 as of June 2025.

## Repository Structure

```
adk-samples/
├── agents/                  # Individual agent samples
│   ├── customer-service/    # Customer service agent example
│   ├── data-analyst/        # Data analysis agent example
│   └── travel-planner/      # Travel planning multi-agent example
├── .github/                 # GitHub Actions workflows and templates
└── README.md
```

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/your-org/adk-samples.git
cd adk-samples
```

### 2. Set up a virtual environment

```bash
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
```

### 3. Install dependencies for a sample

Each sample has its own `requirements.txt`. For example:

```bash
cd agents/travel-planner
pip install -r requirements.txt
```

### 4. Configure environment variables

Copy the sample environment file and fill in your values:

```bash
cp .env.example .env
# Edit .env with your project ID and other settings
```

### 5. Run the agent

```bash
adk run .
```

Or launch the interactive web UI:

```bash
adk web
```

> **Tip:** `adk web` binds to `localhost:8000` by default. To use a different port, run `adk web --port 8080`.

## Contributing

Contributions are welcome! Please read our [contribution guidelines](CONTRIBUTING.md) and check the [issue tracker](https://github.com/your-org/adk-samples/issues) for open tasks.

When submitting a new sample, ensure it:
- Includes a `README.md` with setup instructions
- Has a `requirements.txt` pinning all dependencies
- Passes linting (`flake8`)
- Includes at least one unit test

## License

This project is licensed under the Apache 2.0 License — see the [LICENSE](LICENSE) file for details.
