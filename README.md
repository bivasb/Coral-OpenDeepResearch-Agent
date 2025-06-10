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


## 1. Clone & Install Dependencies

<details>

- Run [Interface Agent](https://github.com/Coral-Protocol/Coral-Interface-Agent)


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

- Agent Installation


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
 

## 2. Configure Environment Variables

<details>
Get the API Key:
[Linkup](https://app.linkup.so/api-keys)
[OpenAI](https://platform.openai.com/api-keys)


Create .env file in project root

```bash
cp -r .env_sample .env
```
</details>


## 3. Run Agent

<details>

Run the agent using `uv`:

```bash
uv run python langchain_open_deep_research.py
```
</details>


## 4. Example

<details>

Input:

```bash
Write me a report on Model Context Protocol.
```
Output:

```bash
The research report will be displayed directly in the console output when you run the agent.
```
</details>


## Creator Details
- **Name**: Suman Deb
- **Affiliation**: Coral Protocol
- **Contact**: [Discord](https://discord.com/invite/Xjm892dtt3)
