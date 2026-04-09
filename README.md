# 🚀 Advanced RAG Chatbot (Personal Knowledge Base)

![Python](https://img.shields.io/badge/Python-3.10-blue)
![FastAPI](https://img.shields.io/badge/FastAPI-Backend-green)
![Streamlit](https://img.shields.io/badge/Streamlit-Frontend-red)
![LLM](https://img.shields.io/badge/LLM-OpenAI-orange)
![Vector DB](https://img.shields.io/badge/VectorDB-Qdrant-purple)

---

## 🧠 Overview

This project is a **production-ready Retrieval-Augmented Generation (RAG) chatbot** that answers questions based on a **personal knowledge base (PDFs, documents, notes)**.

Instead of relying only on a language model, this system:

* Retrieves relevant information from your documents
* Enhances responses with **context-aware AI**
* Reduces hallucinations and improves accuracy

---

## 🎯 Key Features

✅ Retrieval-Augmented Generation (RAG)
✅ FastAPI backend (scalable APIs)
✅ Streamlit interactive UI
✅ Vector search using Qdrant
✅ LlamaIndex for document indexing
✅ Secure environment variable handling
✅ Modular and production-ready architecture

---

## 🏗️ Architecture Diagram

```
                ┌──────────────┐
                │   User Query │
                └──────┬───────┘
                       │
                       ▼
              ┌─────────────────┐
              │   FastAPI API   │
              └──────┬──────────┘
                     │
                     ▼
        ┌──────────────────────────┐
        │   RAG Pipeline (LlamaIndex) │
        └──────┬───────────────┬──┘
               │               │
               ▼               ▼
     ┌──────────────┐   ┌──────────────┐
     │  Vector DB   │   │  LLM (OpenAI)│
     │  (Qdrant)    │   │              │
     └──────┬───────┘   └──────┬───────┘
            │                  │
            └──────────┬───────┘
                       ▼
                ┌──────────────┐
                │ Final Answer │
                └──────────────┘
```

---

## 📁 Project Structure

```
rag-advanced/
│
├── app/
│   ├── main.py
│   ├── routes/
│   │   └── chat.py
│   ├── core/
│   │   ├── config.py
│   │   └── rag_pipeline.py
│   └── services/
│       └── vector_db.py
│
├── data/
├── frontend/
│   └── streamlit_app.py
│
├── requirements.txt
├── .env (not committed)
├── .gitignore
└── README.md
```

---

## ⚙️ Installation & Setup

### 1️⃣ Clone Repository

```bash
git clone https://github.com/Tejaswini-1802/RAG-chatbot.git
cd RAG-chatbot
```

---

### 2️⃣ Create Virtual Environment

```bash
python -m venv venv
venv\Scripts\activate
```

---

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

### 4️⃣ Setup Environment Variables

Create `.env` file:

```
OPENAI_API_KEY=your_api_key_here
QDRANT_URL=http://localhost:6333
```

---

### 5️⃣ Run Qdrant (Vector DB)

```bash
docker run -p 6333:6333 qdrant/qdrant
```

---

### 6️⃣ Start Backend

```bash
uvicorn app.main:app --reload
```

👉 API Docs: http://127.0.0.1:8000/docs

---

### 7️⃣ Run Frontend

```bash
streamlit run frontend/streamlit_app.py
```

---

## 💡 How It Works

1. User enters a query
2. Backend sends query to RAG pipeline
3. Relevant documents are retrieved from vector DB
4. LLM generates context-aware answer
5. Response is returned to UI

---

## 🔥 Advanced Features (Planned / Extendable)

* 🔐 Authentication (JWT)
* 💬 Chat memory (conversation history)
* ⚡ Streaming responses
* 📂 Multi-file upload support
* 🌐 Deployment (AWS / Render / Docker)
* 🤖 Local LLM integration (LLaMA / Mistral)

---

## 📊 Use Cases

* Personal AI Assistant
* Resume Chatbot (HR queries)
* Study & Notes Assistant
* Company Knowledge Base Bot
* Legal/Research Document Assistant

---

## 🛡️ Security Best Practices

* API keys stored in `.env`
* `.env` excluded via `.gitignore`
* No secrets committed to GitHub

---

## 📸 Demo (Add Screenshots Here)

```
(Add Streamlit UI screenshot)
(Add API docs screenshot)
```

---

## 💼 Resume Description

**Advanced RAG Chatbot using LLMs and Vector Databases**

* Built a scalable AI chatbot using FastAPI, LlamaIndex, and Qdrant
* Implemented semantic search with vector embeddings
* Integrated LLM for context-aware responses
* Designed modular architecture for production deployment

---

## 🤝 Contributing

Pull requests are welcome. For major changes, open an issue first.

---

## ⭐ Show Your Support

If you like this project:

👉 Star the repo
👉 Share with others
👉 Use it in your portfolio

---

## 🚀 Author

**Tejaswini Adasule**
Aspiring Data Scientist | AI Engineer

