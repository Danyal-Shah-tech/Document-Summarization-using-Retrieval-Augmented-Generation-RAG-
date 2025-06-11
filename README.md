Document Summarization with Retrieval-Augmented Generation (RAG)
This project implements a document summarization system using RAG, designed to process PDF documents, retrieve relevant chunks, and generate concise summaries. The system uses pdfplumber for text extraction, sentence-transformers for embeddings, faiss for vector storage, and facebook/bart-large-cnn for summarization, running in a Jupyter Notebook on Google Colab.
Project Overview

Objective: Summarize documents by retrieving relevant text chunks and generating coherent summaries (60–500 words).
Components:
Ingestion: Extracts text from PDFs using pdfplumber.
Chunking: Splits text into 500-word chunks with 50-word overlap.
Embedding & Retrieval: Uses all-MiniLM-L6-v2 for embeddings and FAISS for efficient retrieval.
Summarization: Generates summaries using BART (facebook/bart-large-cnn).


Environment: Google Colab or local Jupyter Notebook.

Setup Instructions

Clone the Repository (if applicable):
git clone <repository-url>
cd <repository-directory>


Create a Virtual Environment:
python -m venv env
source env/bin/activate  # On Windows: env\Scripts\activate


Install Dependencies:
pip install -r requirements.txt


Launch Jupyter Notebook:
jupyter notebook

Alternatively, open Summarization_Using_RAG.ipynb in Google Colab.

Prepare Documents:

Place PDF files in the working directory or upload them via Colab’s file upload widget.
Example datasets: ArXiv Abstracts (Kaggle), CNN/DailyMail (HuggingFace), or custom PDFs.



Usage

Open the Notebook:
In Jupyter or Colab, open Summarization_Using_RAG.ipynb.


Run Cells Sequentially:
Install dependencies (Cell 1).
Import libraries (Cell 2).
Upload a PDF file (Cell 3).
Process the document, retrieve chunks, and generate a summary (Cells 4–8).


View Outputs:
Retrieved chunks and the summary are printed in the notebook.
Sample outputs for three documents are provided in sample_output.md.



Deliverables

Summarization_Using_RAG.ipynb: Jupyter Notebook with the implementation.
requirements.txt: Dependency list.
README.md: This file.
sample_output.md: Summaries and metrics for three sample documents.
report.pdf: 2-page report summarizing the project (compiled from report.tex).

Notes

Testing: Test with at least three documents (e.g., one ArXiv paper, one CNN/DailyMail article, one custom PDF).
Limitations: BART’s input is truncated to 1024 tokens; larger documents rely on chunking and retrieval.
Creative Addition: FAISS-based retrieval enhances efficiency for long documents.
Submission: ZIP containing all deliverables, including sample outputs and the compiled report.

