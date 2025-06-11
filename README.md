# Document Summarization using Retrieval-Augmented Generation (RAG)

## 📌 Objective
This project summarizes long documents using Retrieval-Augmented Generation. It uses vector embeddings, semantic retrieval, and large language models to produce accurate summaries.

---

## 🧱 Components
- **Document Ingestion**: Extract text from PDFs.
- **Chunking**: Semantic chunks with overlap.
- **Embedding + Retrieval**: FAISS + SentenceTransformers.
- **Summary Generation**: Pretrained model (`facebook/bart-large-cnn`).
- **Presentation**: Displays retrieved chunks and summary.

---

## 🚀 Getting Started

### 1. Setup Environment
```bash
pip install -r requirements.txt
