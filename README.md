# Medical RAG Assistant (LLM-Powered)

An end-to-end Retrieval-Augmented Generation (RAG) medical chatbot built using OpenAI, Pinecone vector database, HuggingFace embeddings, and Flask.

The system retrieves relevant medical context from a document knowledge base and generates concise, context-aware responses through a web-based chat interface.

DISCLAIMER: This chatbot provides informational responses only and does not constitute medical advice.

---

## Project Overview

This project demonstrates the implementation of a production-style RAG architecture:

1. Medical documents are processed and embedded using HuggingFace embeddings.
2. Embeddings are stored in a Pinecone vector database.
3. User queries are embedded and matched via vector similarity search.
4. Retrieved context is passed to an OpenAI LLM using prompt engineering.
5. The generated response is returned through a Flask-based web interface.

The system ensures concise responses with controlled output length and fallback handling when context is insufficient.

---

## Architecture

User Query  
↓  
Query Embedding (HuggingFace)  
↓  
Vector Search (Pinecone)  
↓  
Context Retrieval  
↓  
LLM Generation (OpenAI)  
↓  
Flask Web Response 

---

## Tech Stack

- Python
- Flask
- OpenAI API
- Pinecone (Vector Database)
- HuggingFace Sentence Transformers
- LangChain
- Docker (containerization)
- HTML / CSS (Bootstrap frontend)

---

## Demo

Below is the chatbot interface:

![Chatbot Demo](assets/chat-demo.png)

---

## Local Setup

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/medical-rag-assistant.git
cd medical-rag-assistant
```

---

## Local Setup Guide

Follow the steps below to run the Medical RAG Assistant locally.

---


## Create Virtual Environment

```bash
python -m venv venv
venv\Scripts\activate
```

---


## Install Dependencies

```bash
pip install -r requirements.txt  
```

---

## Create a `.env` File

Create a file named `.env` in the root directory and add:

```bash
OPENAI_API_KEY=your_openai_key  
PINECONE_API_KEY=your_pinecone_key  
PINECONE_ENV=your_environment  
```

---

## Create and Populate the Pinecone Index

This step loads the medical PDF, generates embeddings, and stores them in Pinecone.

```bash
python store_index.py  
```

---

## Run the Application

```bash
python app.py  
```

Open your browser and visit:

```bash
http://127.0.0.1:8080  
```

---

## Responsible AI Measures

- Informational disclaimer included in the user interface  
- Controlled response length (maximum 3 sentences)  
- Explicit fallback when the model does not know the answer  
- Retrieval-based answering (RAG) to reduce hallucinations  

---

## Future Improvements

- Migration to production WSGI server (Gunicorn)  
- AWS ECS or EC2 deployment  
- Next.js frontend upgrade  
- User authentication layer  
- Logging & monitoring  
- Multi-document ingestion  
- Medical knowledge validation layer  

---

## Key Skills Demonstrated

- Retrieval-Augmented Generation (RAG)  
- Vector similarity search  
- Embedding pipelines  
- Prompt engineering  
- API integration  
- Full-stack AI deployment  
- Docker containerization  
- Responsible AI implementation  

---

## ⚠️ Disclaimer

This application is for educational and demonstration purposes only.  
It does not provide medical advice. Always consult a qualified healthcare professional.