# LangChain Practice 🧠🤖

A hands-on notebook workspace for learning LangChain fundamentals and experimenting with common Retrieval-Augmented Generation (RAG) building blocks.

## Overview

The notebooks are organized in a practical learning path, from loading data to splitting text, creating embeddings, and storing vectors for retrieval.

## Workspace Structure

```text
Langchain/
├── .env.example
├── 01_Data_Ingestion/
│   └── data_ingestion.ipynb
├── 02_Text_Splitting/
│   ├── 01_recursive_character_splitter.ipynb
│   ├── 02_json_splitter.ipynb
│   └── 03_html_header_splitter.ipynb
├── 03_Embeddings/
│   ├── 01_huggingface_embeddings.ipynb
│   └── 02_ollama_embeddings.ipynb
├── 04_Vector_Databases/
│   ├── 01_chroma_db.ipynb
│   └── 02_faiss_db.ipynb
└── data/
	 └── speech.txt

Langchain_v1/
```

## What’s Inside

- **Data ingestion**: Load and prepare raw documents for downstream processing.
- **Text splitting**: Experiment with recursive, JSON, and HTML header splitters.
- **Embeddings**: Compare Hugging Face and Ollama-based embeddings.
- **Vector databases**: Build local vector stores with Chroma and FAISS.

## Setup

1. Create and activate a virtual environment.
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Copy `Langchain/.env.example` to `.env` and add your Hugging Face token if you plan to use Hugging Face models:
   ```dotenv
   HF_TOKEN=your_huggingface_token_here
   ```

## Usage

- Open any notebook in VS Code and run the cells top to bottom.
- Start with `Langchain/01_Data_Ingestion/data_ingestion.ipynb` if you want the intended learning sequence.
- Use `Langchain/data/speech.txt` as the included sample text source.

## Notes

- Some notebooks may rely on external services or local model setups, depending on the embedding/vector store examples you run.
- `Langchain_v1/` is currently empty and can be used for future experiments or alternate notebook versions.
