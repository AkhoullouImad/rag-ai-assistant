# 🧠 Local RAG AI Assistant

## 🚀 Overview
A fully local AI assistant using Retrieval-Augmented Generation (RAG),
built with n8n, Ollama (LLaMA 3.1), and Docker.

## 🏗️ Architecture
- LLM: LLaMA 3.1 via Ollama
- Orchestration: n8n workflows
- Backend: REST API via n8n webhooks
- Frontend: HTML/CSS/JS chat interface
- Database: PostgreSQL
- Deployment: Docker Compose

## 🧠 RAG Architecture

This project implements a full Retrieval-Augmented Generation pipeline:

1. Documents are ingested and semantically chunked
2. Chunks are embedded using a local embedding model
3. Embeddings are stored in a vector database (Qdrant)
4. At query time:
   - Relevant chunks are retrieved
   - Passed to the LLM as context
   - Response is generated

This design improves accuracy and enables domain-specific responses.
## ⚙️ Features
- Chat interface for interacting with the AI
- Document ingestion and processing
- Semantic retrieval (RAG)
- Workflow automation via n8n

## 🖥️ Frontend
Located in `/frontend`, provides a simple chat UI connected to the AI backend.

## 🐳 Run locally

```bash
docker compose up -d
After running docker compose up -d, you can access n8n by opening your web browser and navigating to http://localhost:5678⁠ (unless you changed the default port in your docker-compose.yaml).
n8n will be running and available at that address.

## 🔄 Workflows

### 1. Ingestion Pipeline
Processes documents and stores them in the vector database:
- Document loading
- Semantic chunking
- Embedding generation
- Storage in Qdrant

### 2. Chat Pipeline
Handles user queries:
- Receives user input via webhook
- Retrieves relevant context from Qdrant
- Uses LLM (LLaMA 3.1 via Ollama) to generate responses
- Maintains conversation memory

📂 Workflows
Check /workflows for exported n8n pipelines.

🔐 Notes
Runs fully locally (no cloud)
Designed for experimentation with AI pipelines

