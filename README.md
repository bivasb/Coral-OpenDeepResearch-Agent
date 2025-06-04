# Open Deep Research Agent

The Open Deep Research agent is an open-source research assistant that automates comprehensive report generation using a graph-based workflow or multi-agent architecture.It can perform in-depth web searches, generate structured reports, support human-in-the-loop feedback, and integrate with APIs like Tavily, Linkup, DuckDuckGo, and Azure AI Search, using customizable LLMs for tailored, high-quality research outputs.

## Overview

The Open Deep Research Agent:
- Generates comprehensive research reports on any topic
- Collaborates with other agents in a multi-agent system
- Plans, researches, and compiles structured reports
- Saves reports in `temp/` and returns the file path

## Components

1. **LangChain Open Deep Research** (`langchain_open_deep_research.py`)
   - Research agent using LangChain
   - Connects to Coral server
   - Uses OpenDeepResearch for report generation
   - Employs GPT-4o-mini for processing

2. **Open Deep Research** (`odr.py`)
   - Core research functionality
   - Uses LangGraph for workflow
   - Saves structured reports in `temp/`

## Prerequisites

- Python 3.10, 3.11, or 3.12
- OpenAI API key (for GPT-4o-mini)
- Coral server at `http://localhost:5555/devmode/exampleApplication/privkey/session1/sse`

## Setup

1. **Install Dependencies**
   ```bash
   pip install langchain langchain-openai langgraph python-dotenv anyio
   ```

2. **Configure Environment**
   ```bash
   # Create .env file in project root:
   OPENAI_API_KEY=your_openai_api_key
   ```

3. **Start Coral Server**
   - Follow [main README](../../README.md) for setup
   - Ensure server runs at `http://localhost:5555/devmode/exampleApplication/privkey/session1/sse`

## Running the System

1. **Start Interface Agent**
   ```bash
   python interface.py
   ```
   - Connects to Coral server
   - Provides command-line interface for research requests

2. **Launch Research Agent**
   ```bash
   python langchain_open_deep_research.py
   ```
   - Registers as "open_deepresearch_agent"
   - Listens for research requests

## Interaction

- Use interface agent's command line to send research requests
- Research agent returns report path (saved in `temp/`)
- Monitor terminal for connection status and report locations

## Troubleshooting

- Verify Coral server is running
- Check server logs for connection issues
- Ensure `.env` variables are set
- Monitor `temp/` for reports