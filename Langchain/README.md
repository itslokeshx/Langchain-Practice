# LangChain — RAG Fundamentals 🧠📚

> A structured, hands-on notebook workspace for mastering the **core building blocks of Retrieval-Augmented Generation (RAG)** with LangChain — from raw document loading all the way to querying a vector database.

---

## 📚 Notebook Series

| # | Module | Notebooks | What You Learn |
|---|--------|-----------|---------------|
| 01 | **Data Ingestion** | `data_ingestion.ipynb` | Load documents from files, URLs, and other sources |
| 02 | **Text Splitting** | `01_recursive_character_splitter.ipynb` · `02_json_splitter.ipynb` · `03_html_header_splitter.ipynb` | Chunk text intelligently for downstream retrieval |
| 03 | **Embeddings** | `01_huggingface_embeddings.ipynb` · `02_ollama_embeddings.ipynb` | Convert text chunks to semantic vectors |
| 04 | **Vector Databases** | `01_chroma_db.ipynb` · `02_faiss_db.ipynb` | Store and query embeddings for similarity search |

---

## 🗂️ Workspace Structure

```text
Langchain/
├── .env.example                         # API key template
├── requirements.txt                     # All dependencies
├── data/
│   └── speech.txt                       # Sample text for experiments
├── 01_Data_Ingestion/
│   └── data_ingestion.ipynb             # Document loading techniques
├── 02_Text_Splitting/
│   ├── 01_recursive_character_splitter.ipynb
│   ├── 02_json_splitter.ipynb
│   └── 03_html_header_splitter.ipynb
├── 03_Embeddings/
│   ├── 01_huggingface_embeddings.ipynb
│   └── 02_ollama_embeddings.ipynb
└── 04_Vector_Databases/
    ├── 01_chroma_db.ipynb
    └── 02_faiss_db.ipynb
```

---

## 🧠 What You'll Learn

### 01 — Data Ingestion
Learn how to load raw documents into LangChain's `Document` format using a variety of **document loaders** — text files, PDFs, web pages, and more. This is the entry point of every RAG pipeline.

### 02 — Text Splitting
Documents that are too large to embed in one shot need to be **chunked** intelligently. Explore three splitting strategies:
- **Recursive Character Splitter** — the most versatile, language-aware chunker
- **JSON Splitter** — preserves JSON structure when splitting nested data
- **HTML Header Splitter** — uses HTML heading hierarchy to create semantically coherent chunks

### 03 — Embeddings
Transform text chunks into dense **vector representations** that capture semantic meaning. Compare two local/open-source embedding options:
- **Hugging Face Embeddings** — leverage `sentence-transformers` models via the Hub
- **Ollama Embeddings** — run embedding models fully **offline** on your local machine

### 04 — Vector Databases
Store your embeddings in a searchable **vector store** and retrieve the most relevant chunks at query time. Covers:
- **ChromaDB** — lightweight local vector database, zero infrastructure required
- **FAISS** — Facebook AI Similarity Search, blazing-fast in-memory retrieval

---

## ⚙️ Setup

### Prerequisites
- Python **3.9+**
- For Ollama embeddings: [Ollama](https://ollama.com) installed and running locally

### 1. Install dependencies

```bash
pip install -r requirements.txt
```

### 2. Configure API Keys

```bash
cp .env.example .env
```

Then edit `.env`:

```dotenv
HF_TOKEN=your_huggingface_token_here
```

> **Note:** A Hugging Face token is only needed for gated models on the Hub. Public embedding models like `all-MiniLM-L6-v2` work without authentication.

| Provider | Where to get key |
|----------|-----------------|
| Hugging Face | [huggingface.co/settings/tokens](https://huggingface.co/settings/tokens) |

### 3. Run the notebooks

Open any `.ipynb` in **VS Code** or **Jupyter** and run cells top to bottom.

---

## 🚀 Recommended Learning Path

Follow this sequence for the most logical progression through RAG concepts:

```
01_Data_Ingestion  →  02_Text_Splitting  →  03_Embeddings  →  04_Vector_Databases
```

Each stage feeds directly into the next — you load data, split it, embed it, then store and retrieve it.

---

## 📦 Dependencies

```
langchain             # Core LangChain framework
langchain-community   # Community loaders & integrations
langchain-huggingface # Hugging Face embedding models
langchain-ollama      # Ollama local model support
langchain-chroma      # ChromaDB vector store
faiss-cpu             # FAISS similarity search
python-dotenv         # .env file loading
```

---

## 🔑 RAG Pipeline at a Glance

```
Raw Documents
      │
      ▼  [01_Data_Ingestion]
  LangChain Documents
      │
      ▼  [02_Text_Splitting]
  Chunks (smaller Document objects)
      │
      ▼  [03_Embeddings]
  Dense Vectors
      │
      ▼  [04_Vector_Databases]
  Vector Store  ──── Query ──▶  Relevant Chunks ──▶  LLM ──▶  Answer
```

---

## 🗒️ Notes

- Use `data/speech.txt` as the included sample text to run all experiments without needing external data.
- Ollama notebooks require the Ollama daemon to be running (`ollama serve`) and the relevant model pulled locally.
- ChromaDB and FAISS both persist data locally — you can reuse stored embeddings across sessions.
