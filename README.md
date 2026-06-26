# LangChain Practice 🧠🤖

A personal learning playground designed for practicing and mastering the core concepts of Retrieval-Augmented Generation (RAG) pipelines using Python and LangChain.

## 📂 Repository Structure

The repository is organized sequentially, taking you step-by-step from raw data ingestion to vector storage and retrieval:

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
│   └── speech.txt               # Sample historical text speeches
```

## 🚀 RAG Workflow Overview

This playground covers the core components of a Retrieval-Augmented Generation pipeline:

1. **Ingestion**: Loading structured and unstructured data formats (PDF, XML, Text).
2. **Chunking**: Splitting documents recursively, by HTML headers, or by JSON keys to maintain semantic meaning within context limits.
3. **Embeddings**: Generating vector representations of text using local (Ollama) and open-source (Hugging Face) model embeddings.
4. **Vector Stores**: Storing embeddings in local vector databases (Chroma, FAISS) and querying them to retrieve relevant context.