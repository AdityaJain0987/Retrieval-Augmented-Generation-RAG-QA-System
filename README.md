# RAG-based Question Answering System

This project implements a **Retrieval-Augmented Generation (RAG)** pipeline to answer user queries based on the content of `.txt` documents using vector search and a language model.

## Overview

The system performs the following steps:

1. Loads and preprocesses plain text files from a specified directory.
2. Splits documents into manageable chunks.
3. Generates semantic embeddings using Hugging Face's `MiniLM` model.
4. Stores embeddings in a Chroma vector database for persistent storage.
5. Accepts a user query, retrieves the top-k most relevant document chunks.
6. Uses OpenAI's GPT-4o-mini model (via OpenRouter or similar API) to answer the query using only the retrieved context.

## Key Features

* Document chunking and metadata tagging
* Embedding with Hugging Face `all-MiniLM-L6-v2`
* Persistent vector store using Chroma
* Top-k similarity-based retrieval
* LLM-based question answering using GPT-4o-mini
* Modular, reproducible pipeline in Python

## Tech Stack

* Python
* LangChain
* ChromaDB
* Hugging Face Transformers
* OpenAI / OpenRouter (for GPT-4o-mini)
* dotenv for API key management
