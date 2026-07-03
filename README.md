# LangChain Practice 🦜🔗

> A curated, progressive learning workspace for mastering **LangChain** — from RAG fundamentals and embeddings to agents, multi-provider LLMs, structured outputs, and production middleware patterns.

---

## 🗂️ Repository Structure

```text
Langchain-Practice/
├── Langchain/          # RAG fundamentals — data ingestion, text splitting,
│                       # embeddings & vector databases
└── Langchain_v1/       # LangChain v1.x — agents, tools, messages,
                        # structured output & middleware
```

---

## 📂 Workspaces

### [`Langchain/`](./Langchain/README.md) — RAG Fundamentals

Build the essential **Retrieval-Augmented Generation** pipeline from the ground up. Four progressive modules take you from raw files to a fully queryable semantic search engine.

| Module | Focus |
|--------|-------|
| `01_Data_Ingestion` | Load documents from files, URLs, and other sources |
| `02_Text_Splitting` | Chunk text with recursive, JSON, and HTML-aware splitters |
| `03_Embeddings` | Vectorize text using Hugging Face and Ollama models |
| `04_Vector_Databases` | Store and retrieve vectors with ChromaDB and FAISS |

---

### [`Langchain_v1/`](./Langchain_v1/README.md) — Agents, Tools & Advanced Patterns

Go beyond RAG and explore the full power of **LangChain 1.x**. Six notebooks take you through agent construction, multi-provider LLM integration, and production-grade patterns.

| Notebook | Focus |
|----------|-------|
| `1-langchainintro.ipynb` | Agent creation and the tool-calling loop |
| `2-modelintegration.ipynb` | OpenAI · Google Gemini · Groq — unified model interface |
| `3-tools.ipynb` | Custom tools, schemas, and execution loops |
| `4-messages.ipynb` | The LangChain message system — roles, content, metadata |
| `5-structuredoutput.ipynb` | Pydantic-enforced structured model responses |
| `6-middleware.ipynb` | Logging, summarization, guardrails & token management |

---

## 🧠 Learning Path

This repo is designed to be followed in order — start with the RAG fundamentals to understand how LangChain handles data and retrieval, then move to `Langchain_v1` to build fully autonomous agents on top of that foundation.

```
┌─────────────────────────────────────────────────────────────┐
│                     Langchain/ (RAG Core)                   │
│                                                             │
│  Data Ingestion → Text Splitting → Embeddings → Vector DBs  │
└──────────────────────────────┬──────────────────────────────┘
                               │
                               ▼
┌─────────────────────────────────────────────────────────────┐
│               Langchain_v1/ (Agents & Advanced)             │
│                                                             │
│  Intro & Agents → Model Integration → Tools → Messages      │
│       → Structured Output → Middleware                      │
└─────────────────────────────────────────────────────────────┘
```

---

## ⚙️ Quick Start

### Langchain (RAG workspace)

```bash
cd Langchain
pip install -r requirements.txt
cp .env.example .env   # add your HF_TOKEN
# Open any notebook in VS Code or Jupyter
```

### Langchain_v1 (Agents workspace)

```bash
cd Langchain_v1
uv sync                # or: pip install -r requirements.txt
# Create .env with your OPENAI_API_KEY, GOOGLE_API_KEY, GROQ_API_KEY
# Open any notebook in VS Code and select the .venv kernel
```

---

## 🔑 API Keys Reference

| Provider | Used In | Where to Get |
|----------|---------|-------------|
| OpenAI | `Langchain_v1` | [platform.openai.com/api-keys](https://platform.openai.com/api-keys) |
| Google Gemini | `Langchain_v1` | [aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey) |
| Groq | `Langchain_v1` | [console.groq.com/keys](https://console.groq.com/keys) |
| Hugging Face | `Langchain` | [huggingface.co/settings/tokens](https://huggingface.co/settings/tokens) |

> **Note:** You only need the keys for providers you intend to use — notebooks degrade gracefully if a key is missing for an unused provider.

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

## 📁 What's in Each Workspace

| File | Description |
|------|-------------|
| `Langchain/.env.example` | Template for Langchain workspace secrets |
| `Langchain/requirements.txt` | RAG workspace dependencies |
| `Langchain/data/speech.txt` | Sample document for experiments |
| `Langchain_v1/requirements.txt` | Agent workspace pip dependencies |
| `Langchain_v1/pyproject.toml` | uv project config |
| `Langchain_v1/main.py` | Standalone script entry point |

---

## 🗒️ Notes

- All notebooks are **self-contained** — run cells top to bottom in any environment.
- The `Langchain_v1/.venv` directory is managed by `uv` and is excluded from version control.
- Ollama-based embedding notebooks require the [Ollama](https://ollama.com) daemon running locally.
- LangChain version in `Langchain_v1`: **1.3.11**
