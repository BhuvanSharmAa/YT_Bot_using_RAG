# YouTube RAG Assistant

A decoupled Retrieval-Augmented Generation (RAG) system that extracts transcripts from YouTube videos, builds a high-performance local hybrid index, and interfaces directly with the native Hugging Face Inference API for smart Q&A.

Built entirely with standard Python structures and the latest stable LangChain primitives, this architecture bypasses volatile library paths for long-term production stability.

---

## Features

* **Custom Hybrid Retrieval:** Combines exact keyword matching (BM25) with dense semantic vectors (Chroma DB + Hugging Face Embeddings) inside a pure-Python deduplication layer to maximize context relevance.
* **Decoupled & Serverless Inference:** Connects directly to the native Hugging Face Inference API (`huggingface_hub`), keeping the local memory footprint incredibly light.
* **Dual-Model Automatic Failover:** Features a built-in traffic fallback mechanism that routes queries to Mistral-7B by default and automatically shifts to Llama-3.1 if an endpoint fails.
* **Interactive Web UI:** Includes a streamlined Gradio web interface complete with a real-time system status tracker and chat history memory.

---

## Installation and Setup

Ensure you have Python 3.10+ installed on your system. 

### 1. Clone the Repository
```bash
git clone [https://github.com/BhuvanSharmAa/YT_Bot_using_RAG.git](https://github.com/BhuvanSharmAa/YT_Bot_using_RAG.git)
cd YT_Bot_using_RAG
