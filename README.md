# Dockerized-RAG-API-Gradio-UI-Project-Setup
This repository contains a fully containerized Retrieval-Augmented Generation (RAG) API service and a Gradio-based UI, both packaged using Docker. The project includes all required scripts, notebooks, Dockerfiles, environment files, and configuration needed to run the complete system end-to-end.

/
├── RAG/
│   ├── app.py                     # RAG API FastAPI backend
│   ├── rag_agent.ipynb            # Model + FAISS + LangChain logic
│   ├── requirements.txt           # RAG backend Python dependencies
│   └── Dockerfile                 # Builds dockerproject-rag-api image
│
├── GRADIO/
│   ├── gradio_client.py           # Frontend client for interacting with RAG API
│   ├── ui_notebook.ipynb          # Notebook for UI prototype
│   ├── requirements_gradio.txt    # Gradio UI dependencies
│   └── Dockerfile                 # Builds dockerproject-gradio-ui image
│
├── docker-compose.yml             # Orchestrates API + UI services
└── README.md                      # Documentation


🚀 Project Overview

This project implements:

1. 🧠 RAG API Service

FastAPI-based microservice

Uses FAISS in-memory vector search for fast retrieval

LangChain / LangGraph pipeline for multi-step reasoning

Packaged into a Docker image: dockerproject-rag-api

2. 🎨 Gradio UI

Lightweight UI to interact with the RAG agent

Sends requests to the FastAPI backend

Packaged into a Docker image: dockerproject-gradio-ui

3. 🐳 Docker Compose Orchestration

Launches both containers together

Frontend connects to backend automatically

Single command deployment

🔧 Running Locally (Docker)
1️⃣ Build the images
docker-compose build

2️⃣ Run the complete system
docker-compose up

3️⃣ Access the system
Service	URL
Gradio UI	http://localhost:7860

RAG API Docs (Swagger)	http://localhost:8000/docs
📦 Exported Docker Images (Optional)

The directory also includes pre-built images:

rag_api.tar

gradio_ui.tar

Load them if you don’t want to build:

docker load -i rag_api.tar
docker load -i gradio_ui.tar
docker-compose up

🌐 Deployment Options

You can deploy the stack to:

Docker Hub

GitHub Container Registry

AWS / GCP / Azure

A local or cloud VM 

