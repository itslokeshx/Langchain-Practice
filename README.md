# LangChain RAG Fundamentals 🧠🤖

Welcome to the **LangChain RAG Fundamentals** repository! This is a structured, hands-on playground designed for practicing and mastering the core concepts of Retrieval-Augmented Generation (RAG) pipelines using Python and LangChain.

The repository is organized sequentially, taking you step-by-step from raw data ingestion to vector storage and retrieval.

---

## 📂 Repository Structure

The repository is split into clean, sequentially numbered modules:

```
├── 01_Data_Ingestion/           # Load raw data from PDF, XML, Text, etc.
│   └── data_ingestion.ipynb
├── 02_Text_Splitting/           # Chunk documents for optimal token limits
│   ├── 01_recursive_character_splitter.ipynb
│   ├── 02_json_splitter.ipynb
│   └── 03_html_header_splitter.ipynb
├── 03_Embeddings/               # Convert chunks into numerical vectors
│   ├── 01_huggingface_embeddings.ipynb
│   └── 02_ollama_embeddings.ipynb
├── 04_Vector_Databases/         # Store and perform semantic searches
│   ├── 01_chroma_db.ipynb
│   └── 02_faiss_db.ipynb
├── data/                        # Shared sample datasets and documents
│   ├── attention.pdf            # "Attention Is All You Need" research paper
│   ├── records.xml              # Structured XML test data
│   └── speech.txt               # Sample historical text speeches
├── .env.example                 # Template for API keys and environment variables
├── requirements.txt             # Project Python dependencies
└── README.md                    # Project documentation
```

---

## 🚀 Suggested Repository Names

If you are publishing this to GitHub/GitLab, here are some clean name suggestions:
1. `langchain-rag-fundamentals` (Recommended)
2. `rag-learning-pathway`
3. `langchain-rag-playground`
4. `learn-rag-step-by-step`

---

## 🛠️ Getting Started

### 1. Clone & Navigate
```bash
git clone <your-repo-url>
cd langchain-rag-fundamentals
```

### 2. Set Up Virtual Environment
Create and activate a virtual environment to manage dependencies locally:
```bash
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Configure Environment Variables
Copy the `.env.example` file to `.env` and fill in your API tokens:
```bash
cp .env.example .env
```
Add your Hugging Face, OpenAI, or Ollama variables:
```env
HF_TOKEN=your_huggingface_token_here
OPENAI_API_KEY=your_openai_api_key_here
```

---

## 📓 Notebook Jupyter Kernel Setup

This repository pre-configures a dedicated Jupyter Kernel pointing to the virtual environment `venv` to avoid package import issues.

If Jupyter does not automatically select it:
1. Open any notebook (e.g., `huggingface_embeddings.ipynb`).
2. Click the **Kernel Selector** in the top-right corner.
3. Select **Python Environments...**
4. Choose **Python (langchain-project-venv)**.