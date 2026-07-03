<div align="center">

# 🦜🔗 LangChain Practice

### A progressive, hands-on learning workspace for mastering LangChain —
### from RAG pipelines to autonomous agents, multi-provider LLMs, and production patterns.

<br/>

![Python](https://img.shields.io/badge/Python-3.12-3776AB?style=for-the-badge&logo=python&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1.3.11-1C3C3C?style=for-the-badge&logo=chainlink&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebooks-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![uv](https://img.shields.io/badge/uv-package%20manager-DE5FE9?style=for-the-badge&logo=astral&logoColor=white)

<br/>

</div>

---

## 🗺️ What's Inside

This repo is split into **two focused workspaces**, designed to be followed in order:

```
Langchain-Practice/
│
├── 01_rag_fundamentals/     ← Start here · Build the RAG pipeline from scratch
│
└── 02_agents_and_tools/     ← Level up · Agents, tools, LLMs & production patterns
```

---

## 📦 Workspace 1 — RAG Fundamentals

> **Path:** [`01_rag_fundamentals/`](./01_rag_fundamentals/README.md)

Build a complete **Retrieval-Augmented Generation** pipeline from scratch — loading documents, chunking them intelligently, converting them to vectors, and querying a local vector store.

<br/>

| # | Module | What You Build |
|---|--------|----------------|
| `01` | **Data Ingestion** | Load `.txt`, `.pdf`, and web sources into LangChain `Document` objects |
| `02` | **Text Splitting** | Chunk documents using recursive, JSON, and HTML-aware splitters |
| `03` | **Embeddings** | Vectorize text with Hugging Face (`sentence-transformers`) and Ollama |
| `04` | **Vector Databases** | Store & retrieve embeddings using ChromaDB and FAISS |

<br/>

**Quick start:**
```bash
cd 01_rag_fundamentals
pip install -r requirements.txt
cp .env.example .env        # paste your HF_TOKEN
# open any notebook in VS Code and run top-to-bottom
```

---

## 🤖 Workspace 2 — Agents & Tools

> **Path:** [`02_agents_and_tools/`](./02_agents_and_tools/README.md)

Go beyond RAG. Build autonomous **LangChain agents**, wire up custom tools, swap between three LLM providers, enforce structured outputs with Pydantic, and add middleware for production-grade control.

<br/>

| # | Notebook | What You Learn |
|---|----------|----------------|
| `01` | `01_intro_and_agents.ipynb` | `create_agent`, tool calling loop, reading agent messages |
| `02` | `02_model_integration.ipynb` | OpenAI · Google Gemini · Groq via unified interface |
| `03` | `03_tools.ipynb` | Tool schemas, custom callables, multi-tool execution |
| `04` | `04_messages.ipynb` | `HumanMessage`, `AIMessage`, `ToolMessage`, metadata |
| `05` | `05_structured_output.ipynb` | `.with_structured_output()`, Pydantic validation, nested schemas |
| `06` | `06_middleware.ipynb` | Logging, token-aware summarization, guardrails, retries |

<br/>

**Quick start:**
```bash
cd 02_agents_and_tools
uv sync                     # or: pip install -r requirements.txt
# create a .env with your API keys (see below)
# open any .ipynb and select the .venv kernel
```

---

## 🧠 Learning Path

Follow this sequence for the most logical progression through LangChain concepts:

```
 ╔══════════════════════════════════════════════════════════════════╗
 ║             01_rag_fundamentals  (Foundation)                   ║
 ║                                                                  ║
 ║   01_data_ingestion                                             ║
 ║        │                                                         ║
 ║        ▼                                                         ║
 ║   02_text_splitting                                             ║
 ║        │                                                         ║
 ║        ▼                                                         ║
 ║   03_embeddings                                                 ║
 ║        │                                                         ║
 ║        ▼                                                         ║
 ║   04_vector_databases                                           ║
 ╚══════════════════════════════╦═══════════════════════════════════╝
                                ║
                                ▼
 ╔══════════════════════════════════════════════════════════════════╗
 ║            02_agents_and_tools  (Advanced)                      ║
 ║                                                                  ║
 ║   01_intro_and_agents  →  02_model_integration  →  03_tools     ║
 ║                                              ↓                   ║
 ║          06_middleware  ←  05_structured_output  ←  04_messages  ║
 ╚══════════════════════════════════════════════════════════════════╝
```

---

## 🔑 API Keys

You only need keys for the providers you plan to use. None are required for the RAG workspace except an optional Hugging Face token for gated models.

| Provider | Workspace | Get Your Key |
|----------|-----------|-------------|
| 🤖 OpenAI | `02_agents_and_tools` | [platform.openai.com/api-keys](https://platform.openai.com/api-keys) |
| 🔷 Google Gemini | `02_agents_and_tools` | [aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey) |
| ⚡ Groq | `02_agents_and_tools` | [console.groq.com/keys](https://console.groq.com/keys) |
| 🤗 Hugging Face | `01_rag_fundamentals` | [huggingface.co/settings/tokens](https://huggingface.co/settings/tokens) |

**`.env` template for `02_agents_and_tools/`:**
```dotenv
OPENAI_API_KEY=sk-...
GOOGLE_API_KEY=AIza...
GROQ_API_KEY=gsk_...
```

---

## 🛠️ Tech Stack

<div align="center">

![LangChain](https://img.shields.io/badge/LangChain-Core-1C3C3C?style=flat-square&logo=chainlink)
![OpenAI](https://img.shields.io/badge/OpenAI-GPT-412991?style=flat-square&logo=openai)
![Google Gemini](https://img.shields.io/badge/Google-Gemini-4285F4?style=flat-square&logo=google)
![Groq](https://img.shields.io/badge/Groq-LPU-F55036?style=flat-square)
![ChromaDB](https://img.shields.io/badge/ChromaDB-Vector%20Store-orange?style=flat-square)
![FAISS](https://img.shields.io/badge/FAISS-Similarity%20Search-blue?style=flat-square)
![HuggingFace](https://img.shields.io/badge/Hugging%20Face-Embeddings-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![Ollama](https://img.shields.io/badge/Ollama-Local%20Models-white?style=flat-square)
![Pydantic](https://img.shields.io/badge/Pydantic-Validation-E92063?style=flat-square&logo=pydantic)

</div>

---

## 📁 Key Files at a Glance

```
01_rag_fundamentals/
├── .env.example                 ← copy to .env and add HF_TOKEN
├── requirements.txt             ← pip dependencies
└── data/
    ├── speech.txt               ← sample text for all experiments
    └── attention.pdf            ← "Attention Is All You Need" for PDF ingestion demos

02_agents_and_tools/
├── pyproject.toml               ← uv project config
├── requirements.txt             ← pip dependencies
└── main.py                      ← standalone script entry point
```

---

## 📝 Notes

- All notebooks are **self-contained** — open any one and run top-to-bottom with no setup beyond installing dependencies.
- The `02_agents_and_tools/.venv` is managed by `uv` and is excluded from version control via `.gitignore`.
- Ollama notebooks require the [Ollama](https://ollama.com) daemon running locally (`ollama serve`).
- Git history is fully preserved across the rename — all file renames were tracked, not delete+recreate.

---

<div align="center">

Made with 🦜 and a lot of ☕

</div>
