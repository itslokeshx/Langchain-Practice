# LangChain Practice 🦜🔗

> A curated, progressive learning workspace for mastering **LangChain** — from RAG fundamentals and embeddings to agents, multi-provider LLMs, structured outputs, and production middleware patterns.

---

## 🗂️ Repository Structure

```text
Langchain-Practice/
├── 01_rag_fundamentals/    # RAG pipeline — data ingestion, text splitting,
│                           # embeddings & vector databases
└── 02_agents_and_tools/    # LangChain v1.x — agents, tools, messages,
                            # structured output & middleware
```

---

## 📂 Workspaces

### [`01_rag_fundamentals/`](./01_rag_fundamentals/README.md) — RAG Fundamentals

Build the essential **Retrieval-Augmented Generation** pipeline from the ground up. Four progressive modules take you from raw files to a fully queryable semantic search engine.

| Module | Focus |
|--------|-------|
| `01_data_ingestion` | Load documents from files, URLs, and other sources |
| `02_text_splitting` | Chunk text with recursive, JSON, and HTML-aware splitters |
| `03_embeddings` | Vectorize text using Hugging Face and Ollama models |
| `04_vector_databases` | Store and retrieve vectors with ChromaDB and FAISS |

---

### [`02_agents_and_tools/`](./02_agents_and_tools/README.md) — Agents, Tools & Advanced Patterns

Go beyond RAG and explore the full power of **LangChain 1.x**. Six notebooks take you through agent construction, multi-provider LLM integration, and production-grade patterns.

| Notebook | Focus |
|----------|-------|
| `01_intro_and_agents.ipynb` | Agent creation and the tool-calling loop |
| `02_model_integration.ipynb` | OpenAI · Google Gemini · Groq — unified model interface |
| `03_tools.ipynb` | Custom tools, schemas, and execution loops |
| `04_messages.ipynb` | The LangChain message system — roles, content, metadata |
| `05_structured_output.ipynb` | Pydantic-enforced structured model responses |
| `06_middleware.ipynb` | Logging, summarization, guardrails & token management |

---

## 🧠 Learning Path

Start with the RAG fundamentals to understand how LangChain handles data and retrieval, then move to `02_agents_and_tools` to build fully autonomous agents on top of that foundation.

```
┌─────────────────────────────────────────────────────────────┐
│              01_rag_fundamentals/ (RAG Core)                │
│                                                             │
│  Data Ingestion → Text Splitting → Embeddings → Vector DBs  │
└──────────────────────────────┬──────────────────────────────┘
                               │
                               ▼
┌─────────────────────────────────────────────────────────────┐
│           02_agents_and_tools/ (Agents & Advanced)          │
│                                                             │
│  Intro & Agents → Model Integration → Tools → Messages      │
│       → Structured Output → Middleware                      │
└─────────────────────────────────────────────────────────────┘
```

---

## ⚙️ Quick Start

### RAG Fundamentals

```bash
cd 01_rag_fundamentals
pip install -r requirements.txt
cp .env.example .env   # add your HF_TOKEN
# Open any notebook in VS Code or Jupyter
```

### Agents & Tools

```bash
cd 02_agents_and_tools
uv sync                # or: pip install -r requirements.txt
# Create .env with your OPENAI_API_KEY, GOOGLE_API_KEY, GROQ_API_KEY
# Open any notebook in VS Code and select the .venv kernel
```

---

## 🔑 API Keys Reference

| Provider | Used In | Where to Get |
|----------|---------|-------------|
| OpenAI | `02_agents_and_tools` | [platform.openai.com/api-keys](https://platform.openai.com/api-keys) |
| Google Gemini | `02_agents_and_tools` | [aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey) |
| Groq | `02_agents_and_tools` | [console.groq.com/keys](https://console.groq.com/keys) |
| Hugging Face | `01_rag_fundamentals` | [huggingface.co/settings/tokens](https://huggingface.co/settings/tokens) |

> **Note:** You only need keys for the providers you intend to use.

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| **LangChain 1.x** | Core framework |
| **LangChain Community** | Extended loaders & integrations |
| **OpenAI / Gemini / Groq** | LLM providers |
| **ChromaDB / FAISS** | Vector stores |
| **Hugging Face / Ollama** | Local & open-source embeddings |
| **Pydantic** | Structured output validation |
| **uv** | Fast Python dependency management |
| **python-dotenv** | Secrets management |

---

## 📁 Key Files

| File | Description |
|------|-------------|
| `01_rag_fundamentals/.env.example` | Template for RAG workspace secrets |
| `01_rag_fundamentals/requirements.txt` | RAG workspace dependencies |
| `01_rag_fundamentals/data/speech.txt` | Sample document for experiments |
| `01_rag_fundamentals/data/attention.pdf` | "Attention Is All You Need" paper |
| `02_agents_and_tools/requirements.txt` | Agent workspace pip dependencies |
| `02_agents_and_tools/pyproject.toml` | uv project config |
| `02_agents_and_tools/main.py` | Standalone script entry point |

---

## 🗒️ Notes

- All notebooks are **self-contained** — run cells top to bottom in any environment.
- The `02_agents_and_tools/.venv` directory is managed by `uv` and excluded from version control.
- Ollama-based embedding notebooks require the [Ollama](https://ollama.com) daemon running locally.
- LangChain version in `02_agents_and_tools`: **1.3.11**
