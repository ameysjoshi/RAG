# Mahabharata RAG (Retrieval-Augmented Generation) System

A simple question-answering system built using Retrieval-Augmented Generation (RAG) to answer questions about the ancient Indian epic, the Mahabharata.

## Overview

This project implements a basic RAG pipeline that allows users to ask questions about the Mahabharata and receive contextually relevant answers. The system chunks the complete Mahabharata text, creates vector embeddings, stores them in a FAISS vector database, and uses a local LLM to generate human-readable responses based on retrieved text passages.

## Features

- **Text Processing**: Automatic chunking of the Mahabharata text with configurable chunk size and overlap
- **Vector Search**: Semantic similarity search using sentence transformers
- **Local LLM**: Uses Ollama with TinyLlama model for response generation
- **Interactive Interface**: Command-line interface for asking questions
- **Fast Retrieval**: FAISS vector store for efficient similarity search

## Architecture

```
User Query → Vector Embedding → FAISS Search → Context Retrieval → LLM Generation → Response
```

## Prerequisites

- Python 3.8+
- Ollama installed locally
- TinyLlama model downloaded via Ollama

## Dependencies

- **langchain**: Framework for building RAG applications
- **sentence-transformers**: For generating text embeddings
- **faiss-cpu**: Vector database for similarity search
- **ollama**: Interface for local LLM
- **jupyter**: For notebook interface


## Example Queries

- "What advice does Krishna give to Arjuna?"
- "Who are the five Pandava brothers?"
- "What happens in the battle of Kurukshetra?"
- "Tell me about Bhishma's role in the epic"

## Limitations

This is a basic RAG implementation with the following limitations:

- Simple chunking strategy without semantic awareness
- No query preprocessing or enhancement
- Basic retrieval without reranking
- Limited context window for the LLM
- No citation tracking or source attribution

## Acknowledgments

- The Complete Mahabharata in English, translated by Kisari Mohan Ganguli (1883-1896)
- LangChain community for the excellent RAG framework
- Ollama team for making local LLMs accessible
- Sentence Transformers for embedding models

