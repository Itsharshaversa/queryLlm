<div align="center">

# 🔍 Query Retrieval System

### AI-Powered Document Intelligence via Retrieval-Augmented Generation

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com)
[![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)](https://langchain.com)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://docker.com)
[![FAISS](https://img.shields.io/badge/FAISS-Vector_DB-FF6F00?style=for-the-badge)](https://faiss.ai)

> Upload any PDF. Ask anything. Get accurate, grounded answers — no hallucinations.

</div>

---

## 📌 What Is This?

The **Query Retrieval System** is a production-ready RAG (Retrieval-Augmented Generation) pipeline that lets users upload PDF documents and query them in natural language. Instead of relying solely on an LLM's pre-trained knowledge, responses are **grounded in your document's actual content** — making answers accurate, traceable, and hallucination-resistant.

---

## ✨ Key Features

| Feature | Description |
|---|---|
| 📄 **PDF Ingestion** | Upload and process any PDF document |
| ✂️ **Smart Chunking** | Text split with overlap to preserve context |
| 🧠 **Semantic Embeddings** | Vector representations of document chunks |
| 🔎 **FAISS Similarity Search** | Lightning-fast nearest-neighbor retrieval |
| 🤖 **LLM Answer Generation** | Gemini / OpenAI / Llama — context-grounded |
| 🔗 **RAG Pipeline** | Full retrieve-then-generate orchestration |
| 🐳 **Dockerized** | One-command deployment anywhere |
| ⚡ **FastAPI Backend** | Async, modular, production-ready APIs |

---

## 🏗️ System Architecture

```
┌─────────────────────────────────────────────────────────┐
│                    INGESTION PIPELINE                    │
│                                                         │
│   PDF Upload → Text Extraction → Chunking               │
│       → Embedding Generation → FAISS Vector Store       │
└─────────────────────────────────────────────────────────┘
                           │
                    Vector Store
                           │
┌─────────────────────────────────────────────────────────┐
│                     QUERY PIPELINE                       │
│                                                         │
│   User Query → Query Embedding → Similarity Search      │
│       → Relevant Chunks → LLM → Grounded Answer         │
└─────────────────────────────────────────────────────────┘
```

---

## 🛠️ Tech Stack

### Backend
- **Python 3.10+** — Core language
- **FastAPI** — Async REST API framework

### AI / LLM Layer
- **LangChain** — Prompt management, chains, memory
- **LangGraph** — Stateful agent orchestration
- **Gemini API / OpenAI API / Llama** — LLM inference

### Vector Search
- **FAISS** — Efficient local vector similarity search

### DevOps
- **Docker** — Containerized deployment

---

## 📁 Project Structure

```
LLM-Based-Query-Retrieval-System/
│
├── main.py               # App entry point
├── router.py             # API route definitions
├── config.py             # Environment & model config
├── requirements.txt      # Python dependencies
├── Dockerfile            # Container setup
│
└── utils/
    ├── documentLoader.py # PDF parsing & text extraction
    ├── embedding.py      # Embedding generation logic
    ├── vectorDB.py       # FAISS store operations
    └── generateAnswer.py # LLM response generation
```

---

## ⚙️ How It Works

### Step 1 — Document Processing
User uploads a PDF → text is extracted → split into overlapping chunks to preserve cross-boundary context.

### Step 2 — Embedding Generation
Each chunk is passed through an embedding model → dense vector representation capturing semantic meaning.

### Step 3 — Vector Storage
Embeddings are indexed in **FAISS** — enabling sub-millisecond similarity search at query time.

### Step 4 — Query Processing
User submits a question → converted to an embedding → top-K most relevant chunks retrieved via cosine similarity.

### Step 5 — Answer Generation
Retrieved chunks (context) + user query → passed to the LLM → model generates an accurate, document-grounded answer.

---

## 🚀 Getting Started

### Prerequisites
- Python 3.10+
- Docker (optional, for containerized run)
- Gemini API key or OpenAI API key

### Local Setup

```bash
# 1. Clone the repo
git clone https://github.com/Itsharshaversa/LLM-Based-Query-Retrieval-System.git
cd LLM-Based-Query-Retrieval-System

# 2. Create and activate virtual environment
python -m venv venv
source venv/bin/activate        # Linux/Mac
venv\Scripts\activate           # Windows

# 3. Install dependencies
pip install -r requirements.txt

# 4. Add your API key to config.py or .env
# GEMINI_API_KEY=your_key_here

# 5. Run the app
uvicorn main:app --reload
```

### Docker Setup

```bash
docker build -t query-retrieval-system .
docker run -p 8000:8000 query-retrieval-system
```

API docs available at: `http://localhost:8000/docs`

---

## 🎯 Use Cases

- 📚 **Academic Research** — Query research papers and textbooks
- 🏢 **Enterprise Docs** — Search internal policy and compliance documents
- ⚖️ **Legal & Contracts** — Extract clauses and answers from legal PDFs
- 🛠️ **Technical Manuals** — Navigate complex documentation instantly
- 🧬 **Healthcare** — Query medical reports and clinical guidelines

---

## 🔮 Roadmap

- [ ] Multi-document retrieval and cross-document reasoning
- [ ] Persistent chat history with session management
- [ ] Source citation with page-level references
- [ ] Voice-based query interface
- [ ] React frontend dashboard
- [ ] AWS cloud deployment (EC2 + S3)
- [ ] User authentication and per-user document isolation

---

## 👨‍💻 Author

**Harshit Srivastava**
B.Tech CSE (AI & ML) — KIET Group of Institutions

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/harshit-srivastava-aiml/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)](https://github.com/Itsharshaversa)
[![LeetCode](https://img.shields.io/badge/LeetCode-FFA116?style=flat&logo=leetcode&logoColor=white)](https://leetcode.com/u/itsharshit04/)

---

<div align="center">

**If this project helped you, drop a ⭐ — it means a lot!**

</div>
