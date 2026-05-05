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
🔄 Workflow
User → Frontend → n8n webhook → LLM (Ollama) → Response

📂 Workflows
Check /workflows for exported n8n pipelines.

🔐 Notes
Runs fully locally (no cloud)
Designed for experimentation with AI pipelines

---
# ⚡ Final Git commands

Once everything is clean:

```bash
git init
git add .
git commit -m "RAG AI assistant with n8n + Ollama + frontend UI"

Then:

git remote add origin https://github.com/YOUR_USERNAME/rag-ai-assistant.git
git push -u origin main
