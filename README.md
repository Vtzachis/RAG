# 🧠 Retrieval-Augmented Generation (RAG) Chatbot

A simple, local RAG (Retrieval-Augmented Generation) chatbot built in Python. It uses embeddings for semantic search and a small instruction-following language model to generate accurate, context-aware responses — all without external APIs or cloud dependencies.

## 🚀 Features

- 🔍 **Semantic Search**: Uses embedding-based similarity to retrieve relevant text from a local dataset.
- 🧠 **Instruction-Tuned Model**: Integrates a LLaMA-based instruct model for accurate responses.
- 🗂️ **Lightweight Vector DB**: Embeddings stored in-memory with cosine similarity matching.
- 💬 **Interactive Q&A**: User inputs are answered with retrieved, grounded context.

## 📁 Dataset

This implementation uses a local file (`cat-facts.txt`) as the knowledge base, loaded line-by-line into memory and embedded.

## 🛠️ Tech Stack

- **Python**
- **Ollama** (for local LLM and embeddings)
- **Hugging Face Models**
  - Embeddings: `bge-base-en-v1.5`
  - LLM: `Llama-3.2-1B-Instruct`

## ⚙️ How It Works

1. Load the local dataset and convert each chunk into an embedding.
2. Store each chunk and its embedding in a simple vector database (Python list).
3. Accept user queries, convert them to embeddings.
4. Retrieve top `N` most similar chunks using cosine similarity.
5. Pass context + question to the LLM for a grounded answer.
6. Stream the response in real-time.

## 📦 Installation

1. Install [Ollama](https://ollama.com/)
2. Clone this repo:
   ```bash
   git clone https://github.com/Vtzachis/RAG
   cd RAG
