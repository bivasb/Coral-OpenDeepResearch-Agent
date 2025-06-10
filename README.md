## [Open Deep Research Coral Agent](https://github.com/Coral-Protocol/open-deep-research-coral-agent)

The Open Deep Research agent is an open-source AI assistant that automates in-depth research and report generation via multi-agent workflows, supporting web search, structured reporting, human feedback, and API/LLM integration.

## Responsibility
The Open Deep Research agent is an open-source research assistant that automates comprehensive report generation using a graph-based workflow or multi-agent architecture. It can perform in-depth web searches, generate structured reports, support human-in-the-loop feedback, and integrate with APIs like Tavily, Linkup, DuckDuckGo, and Azure AI Search, using customizable LLMs for tailored, high-quality research outputs.

## Details
- **Framework**: LangChain
- **Tools used**: OpenDeepResearch Tools, Coral server tools
- **AI model**: GPT-4o
- **Date added**: June 4, 2025
- **Reference**: [Open Deep Research Repo](https://github.com/langchain-ai/open_deep_research)
- **License**: MIT 

## Use the agent

### 1. Clone & Install Dependencies

1.1. Run [Coral Server](https://github.com/Coral-Protocol/coral-server) (Expand drop-down below)
<details>


This agent runs on Coral Server, follow the instrcutions below to run the server. In a new terminal clone the repository:


```bash
git clone https://github.com/Coral-Protocol/coral-server.git
```

Navigate to the project directory:
```bash
cd coral-server
```
Run the server
```bash
./gradlew run
```
</details>

1.2. Run [Interface Agent](https://github.com/Coral-Protocol/Coral-Interface-Agent)
<details>


If you are trying to run Open Deep Research agent and require an input, you can either create your agent which communicates on the coral server or run and register the Interface Agent on the Coral Server. In a new terminal clone the repository:


```bash
git clone https://github.com/Coral-Protocol/Coral-Interface-Agent.git
```
Navigate to the project directory:
```bash
cd Coral-Interface-Agent
```

Install `uv`:
```bash
pip install uv
```
Install dependencies from `pyproject.toml` using `uv`:
```bash
uv sync
```

Configure API Key
```bash
export OPENAI_API_KEY=
```

Run the agent using `uv`:
```bash
uv run python 0-langchain-interface.py
```

</details>


1.3. Agent Installation

<details>

In a new terminal clone the repository:
```bash
git clone https://github.com/Coral-Protocol/Coral-OpenDeepResearch-Agent.git
```

Navigate to the project directory:
```bash
cd Coral-OpenDeepResearch-Agent
```

Install `uv`:
```bash
pip install uv
```

Install dependencies from `pyproject.toml` using `uv`:
```bash
uv sync
```

This command will read the `pyproject.toml` file and install all specified dependencies in a virtual environment managed by `uv`.

</details>

### 2. Configure Environment Variables
Get the API Key:
[Linkup](https://app.linkup.so/api-keys)
[OpenAI](https://platform.openai.com/api-keys)


Create .env file in project root
<details>

```bash
cp -r .env_sample .env
```
</details>

### 3. Run Agent

Run the agent using `uv`:

<details>

```bash
uv run python langchain_open_deep_research.py
```
</details>

### 4. Example

Input

<details>

```bash
Write me a report on Model Context Protocol.
```
</details>

Output
<details>

```bash
The research report will be displayed directly in the console output when you run the agent.
```
</details>

## Creator Details
- **Name**: Suman Deb
- **Affiliation**: Coral Protocol
- **Contact**: [Discord](https://discord.com/invite/Xjm892dtt3)
