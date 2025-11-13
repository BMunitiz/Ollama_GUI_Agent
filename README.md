# Agno Assist Agent - Streamlit GUI

This project implements an AI agent specialized in the Agno framework, providing an interactive web interface using Streamlit.

## Overview

The code creates an AI agent named "Agno Assist" that helps developers understand and use the Agno framework - a lightweight framework for building multi-modal, reasoning agents.

## Key Features

### 🤖 Intelligent Agent
- **Model**: Uses Ollama with `deepseek-coder-v2:16b` model
- **Specialization**: Agno framework and AI agent development
- **Capabilities**:
  - Knowledge base search
  - Web search with DuckDuckGo
  - Code generation
  - Technical explanations

### 📚 Knowledge Base
- **Source**: Agno documentation (`https://docs.agno.com/llms-full.txt`)
- **Vector DB**: ChromaDB with `snowflake-arctic-embed2` embeddings
- **Documents**: 408 loaded documents
- **Search**: Iterative knowledge base search capability

### 🎨 User Interface
- **Framework**: Streamlit
- **Title**: "Whitecurls, your legal assistant" (in Spanish)
- **Features**:
  - Text input for queries
  - Real-time streaming responses
  - Loading indicator during processing

## Technical Architecture

### Core Components

```python
# Main agent
agent = Agent(
    name="Agno Assist",
    model=Ollama("deepseek-coder-v2:16b"),
    tools=[DuckDuckGoTools()],
    knowledge=knowledge_base,
    # Additional configurations...
)

# Knowledge base
knowledge_base = UrlKnowledge(
    urls=["https://docs.agno.com/llms-full.txt"],
    vector_db=ChromaDb(...)
)
```

### Agent Configuration

- **Memory**: Conversation history (last 3 messages)
- **Personalization**: Agentic memory enabled
- **Format**: Markdown responses
- **Debug**: Debug mode activated

## Installation & Usage

### Prerequisites
```bash
pip install agno streamlit chromadb ollama
```

### Execution
```bash
streamlit run Ollama_GUI-Agent.ipynb
```

### Development Features

The agent is designed to:
1. **Understand requests** related to Agno
2. **Iteratively search** the knowledge base
3. **Generate functional code** with complete examples
4. **Provide best practices** and development patterns

## Project Structure

- `Ollama_GUI-Agent.ipynb`: Main notebook with implementation
- Agent configured for specialized technical assistance
- Minimalist and functional web interface
- Integration with local models via Ollama

## Main Dependencies

- `agno`: AI agent framework
- `streamlit`: Web interface
- `chromadb`: Vector database
- `ollama`: Local model integration
- `langchain`: Document processing

## Development Notes

The agent is optimized for:
- Precise technical responses about Agno
- Ready-to-use code generation
- Contextual documentation search
- Real-time assistance via streaming

---

*Project designed for developers working with the Agno framework who need specialized technical assistance.*
