# CAMEL Open Deep Research

A CAMEL (Conversational Agents and Machine Learning) integration of the Open Deep Research system for automated, collaboration in the Coral-Marketing-System.

## Overview

This project creates a CAMEL based Agent with Open Deep Research's capabilities to create an automated research assistant that can:
- Generate comprehensive research reports on any topic
- Collaborate with other agents in a multi-agent system
- Automatically plan, research, and compile structured reports
- Generated report is saved in the temp folder and its path is returned by the research agent for further actions

## Components

1. **MCP Example CAMEL Research** (`mcp_example_camel_research.py`)
   - Implements a research agent using CAMEL framework
   - Connects to a Coral server for agent communication
   - Integrates OpenDeepResearch toolkit for report generation
   - Uses GPT-4 for intelligent processing

2. **Open Deep Research Implementation** (`odr.py`)
   - Provides the core research functionality
   - Uses LangGraph for workflow management
   - Implements a structured report generation pipeline
   - Automatically saves reports to the temp directory

## Prerequisites

- Python 3.10/11/12 installed
- Access to OpenAI API (for GPT-4)
- Coral server

## Setup Instructions

1. **Clone Open Deep Research Repository**
   ```bash
   # Inside the camel-open-deep-research directory
   git clone https://github.com/langchain-ai/open_deep_research.git
   ```

2. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Configure Environment**
   ```bash
   # Create .env file in project root and add:
   OPENAI_API_KEY=your_openai_api_key_here
   # Add any other required environment variables
   ```

4. **Start the Coral Server**
   - Follow the Coral server setup instructions from the [main README](../../README.md)
   - Ensure the server is running at `http://localhost:3001/sse`
   - Verify the server status before proceeding

[Previous sections remain the same until Running the System]

## Running the System

1. **Start the Interface Agent**
   ```bash
   # In the camel-open-deep-research directory
   python mcp_example_camel_interface.py
   ```
   The interface agent will:
   - Connect to the Coral server
   - Provide a command-line interface for interactions
   - Allow you to send research requests and receive responses

2. **Launch the Research Agent**
   ```bash
   python mcp_example_camel_research.py
   ```
   The agent will:
   - Register itself as "research_agent"
   - Connect to the Coral server
   - Begin listening for research requests

3. **Launch Additional Agents (Optional)**
   - Start any other desired communication agents
   - Ensure proper Coral server configuration

## System Interaction

1. **Using the Interface Agent**
   - Once both agents are running, use the interface agent's command line
   - Type your research requests when prompted
   - The research agent will process your request and return the report path
   - Reports are saved in the `temp/` directory

2. **Monitor Output**
   - Connection status in both terminal windows
   - Agent interactions
   - Research progress
   - Generated report locations

## Customization

The Open Deep Research system can be customized via the thread configuration in `odr.py`. To modify planning and writing models:

1. **Set Environment Variables**
   ```bash
   OPENAI_API_KEY=your_key_here      # For GPT-4 planning
   ANTHROPIC_API_KEY=your_key_here   # For Claude writing
   ```

2. **Update Thread Configuration**
   ```python
   "planner_provider": "openai",
   "planner_model": "gpt-4",
   "writer_provider": "anthropic",
   "writer_model": "claude-2"
   ```

For more configuration options, refer to the README in the cloned 'open-deep-research' repository.

## Troubleshooting

- Verify all required services are running
- Check Coral server logs for connection issues
- Confirm environment variables are set correctly
- Monitor `temp/` directory for generated reports
- Ensure open-deep-research repository is properly cloned and in the correct directory