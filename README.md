# PDF Deciphering Assistant - RAG Pipeline

**Microsoft-Simplilearn Agentic AI Program | PDF Deciphering Assistant Project**

## Project Overview

The PDF Deciphering Assistant is a Retrieval-Augmented Generation (RAG) project designed to process scientific PDF documents and retrieve relevant information for question answering.

The project explores document loading, text chunking, embedding generation, vector storage, semantic retrieval, and retrieval-augmented responses.

## Technologies

- Python
- Jupyter Notebook
- Retrieval-Augmented Generation (RAG)
- OpenAI Embeddings
- FAISS Vector Store
- Sentence Transformers (SBERT)
- all-MiniLM-L6-v2

## RAG Pipeline Architecture

```text
Scientific PDF Documents
          |
          v
      PDF Loading
          |
          v
      Text Chunking
          |
          v
     OpenAI Embeddings
          |
          v
    FAISS Vector Store
          |
          v
    Semantic Retrieval
          |
          v
    RAG Response
```

## Local Embedding Comparison

An additional local embedding pipeline was implemented to compare API-based embeddings with locally generated embeddings.

The local pipeline uses Sentence Transformers and the all-MiniLM-L6-v2 model.

## Project Structure

```text
pdf_deciphering_assistant/
|
|-- README.md
|-- .gitignore
|-- notebooks/
|   |-- pdf_rag_capstone.ipynb
|
|-- data/
    |-- Local PDF documents
```

The scientific PDF files are excluded from the public GitHub repository.

## Running the Project

Open `notebooks/pdf_rag_capstone.ipynb` in a Jupyter environment.

Install the dependencies required by the notebook and configure any necessary API credentials before executing its cells.

## Security and Data

- API credentials should not be committed to GitHub.
- Local PDF documents are excluded from version control.
- The notebook is provided as the main project implementation.

## Purpose

This project demonstrates the use of retrieval-augmented generation to support information retrieval and question answering over scientific literature.