# LangMem-Lab

Experiments and hands-on explorations with long-term memory in LLM agent workflows using [LangMem](https://github.com/langchain-ai/langmem), [LangGraph](https://github.com/langchain-ai/langgraph), Groq, and Google Generative AI embeddings.

## Overview

This repository explores agent memory architectures:
- **Long-term semantic memory storage**: Storing and recalling user preferences and contextual memories using embeddings (`GoogleGenerativeAIEmbeddings`).
- **Memory-augmented Agent**: Combining `ChatGroq` LLM with `langmem` memory management tools (`create_manage_memory_tool`) and `InMemoryStore`.
- **Dynamic System Prompts**: Injecting relevant retrieved memories into system instructions before agent invocation.

## Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/MustafaKocamann/LangMem-Lab.git
   cd LangMem-Lab
   ```

2. **Set up the virtual environment:**
   Using `uv`:
   ```bash
   uv sync
   ```
   Or standard virtualenv:
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate
   pip install -r pyproject.toml
   ```

3. **Configure Environment Variables:**
   Copy `.env.example` to `.env` and fill in your API keys:
   ```env
   GROQ_API_KEY="your-groq-api-key"
   GEMINI_API_KEY="your-gemini-api-key"
   ```

4. **Run Experiments:**
   Open and execute `langmem_experiments.ipynb` in your Jupyter environment.
