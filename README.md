Mahabharata RAG (Retrieval-Augmented Generation) System
A simple question-answering system built using Retrieval-Augmented Generation (RAG) to answer questions about the ancient Indian epic, the Mahabharata.
Overview
This project implements a basic RAG pipeline that allows users to ask questions about the Mahabharata and receive contextually relevant answers. The system chunks the complete Mahabharata text, creates vector embeddings, stores them in a FAISS vector database, and uses a local LLM to generate human-readable responses based on retrieved text passages.
Features

Text Processing: Automatic chunking of the Mahabharata text with configurable chunk size and overlap
Vector Search: Semantic similarity search using sentence transformers
Local LLM: Uses Ollama with TinyLlama model for response generation
Interactive Interface: Command-line interface for asking questions
Fast Retrieval: FAISS vector store for efficient similarity search

Architecture
User Query → Vector Embedding → FAISS Search → Context Retrieval → LLM Generation → Response
Prerequisites

Python 3.8+
Ollama installed locally
TinyLlama model downloaded via Ollama
