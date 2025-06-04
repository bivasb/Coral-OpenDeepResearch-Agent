## Open Deep Research Agent

- **Responsibility**:
The Open Deep Research agent is an open-source research assistant that automates comprehensive report generation using a graph-based workflow or multi-agent architecture.It can perform in-depth web searches, generate structured reports, support human-in-the-loop feedback, and integrate with APIs like Tavily, Linkup, DuckDuckGo, and Azure AI Search, using customizable LLMs for tailored, high-quality research outputs.

- **Details**
  - **Framework**: LangChain
  - **Tools used**: OpenDeepResearch Tools, Coral server tools
  - **AI model**: GPT-4o
  - **Date added**: June 4, 2025
  - **License**: MIT 
- **Install Dependencies**:

  ```bash
  pip install langchain langchain-openai langgraph python-dotenv anyio
  ```
- **Configure Environment Variables**:

  ```bash
  # Create .env file in project root
  echo "OPENAI_API_KEY=your_openai_api_key" > .env
  ```
- **Run agent command**:

  ```bash
  python langchain_open_deep_research.py
  ```
- **Example output**:

  ```
   (Sample too big to post, check temp folder) 
   
  ```
- **Creator details**
  - **Name**: Suman
  - **Affiliation**: LangChain AI
  - **Contact**: suman@coralprotocol.org