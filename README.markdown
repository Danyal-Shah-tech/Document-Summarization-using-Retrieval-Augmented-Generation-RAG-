# Document Summarization with Retrieval-Augmented Generation (RAG)

This project implements a document summarization system using Retrieval-Augmented Generation (RAG) to process PDF documents, retrieve relevant text chunks, and generate concise summaries. The system is built in a Jupyter Notebook (`Summarization_Using_RAG.ipynb`) and leverages `pdfplumber` for text extraction, `sentence-transformers` for embeddings, `faiss` for vector storage, and `facebook/bart-large-cnn` for summarization. It is designed to run in Google Colab or a local Jupyter environment.

## Project Overview

- **Objective**: Summarize PDF documents by retrieving relevant chunks and generating coherent summaries (60–500 words).
- **Components**:
  - **Ingestion**: Extracts text from PDFs using `pdfplumber`.
  - **Chunking**: Splits text into 500-word chunks with 50-word overlap.
  - **Embedding & Retrieval**: Uses `all-MiniLM-L6-v2` for embeddings and FAISS for efficient retrieval.
  - **Summarization**: Generates summaries using BART (`facebook/bart-large-cnn`).
- **Environment**: Google Colab or local Jupyter Notebook with Python 3.8–3.11.

## Setup Instructions

1. **Clone the Repository** (if applicable):
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. **Create a Virtual Environment**:
   ```bash
   python -m venv env
   source env/bin/activate  # On Windows: env\Scripts\activate
   ```

3. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Launch Jupyter Notebook**:
   ```bash
   jupyter notebook
   ```
   Alternatively, upload `Summarization_Using_RAG.ipynb` to Google Colab.

5. **Prepare Documents**:
   - Place PDF files in the working directory or upload them via Colab’s file upload widget.
   - Suggested datasets:
     - [ArXiv Abstracts](https://www.kaggle.com/datasets/CornellUniversity/arxiv)
     - [CNN/DailyMail](https://huggingface.co/datasets/cnn_dailymail)
     - Custom PDFs

## Usage

1. **Open the Notebook**:
   - Open `Summarization_Using_RAG.ipynb` in Jupyter or Google Colab.
2. **Run Cells Sequentially**:
   - Install dependencies (Cell 1).
   - Import libraries (Cell 2).
   - Upload a PDF file (Cell 3).
   - Extract text, chunk, embed, retrieve, and summarize (Cells 4–8).
3. **View Outputs**:
   - Retrieved chunks and summaries are printed in the notebook.
   - Sample outputs for three documents are available in `sample_output.md`.

## Deliverables

- `Summarization_Using_RAG.ipynb`: Main implementation notebook.
- `requirements.txt`: List of Python dependencies.
- `README.md`: This file with setup and usage instructions.
- `sample_output.md`: Sample summaries and metrics for three documents.
- `report.pdf`: 2-page project report (compiled from `report.tex`).

## Notes

- **Testing**: Run the notebook with at least three documents (e.g., an ArXiv paper, a CNN/DailyMail article, a custom PDF) to meet project requirements.
- **Limitations**: BART truncates inputs to 1024 tokens; long documents rely on effective chunking and retrieval.
- **Creative Addition**: FAISS-based retrieval optimizes performance for large documents.
- **Submission**: Create a ZIP file containing all deliverables:
  ```bash
  zip submission.zip Summarization_Using_RAG.ipynb requirements.txt README.md sample_output.md report.pdf
  ```