# 📚 Knowledge Assistant (RAG)

An AI-powered document question-answering application that uses **Retrieval-Augmented Generation (RAG)** to answer questions from uploaded PDF documents. The application combines semantic search with Large Language Models (LLMs) to provide accurate, context-aware responses.

---

## 🚀 Features

- 📄 Upload PDF documents
- 🤖 Ask questions in natural language
- 🔍 Semantic search using vector embeddings
- 🧠 Context-aware responses using Groq Llama models
- ⚡ FastAPI backend with REST APIs
- 💾 ChromaDB vector database
- 📚 Automatic document chunking
- 🌐 Simple and responsive web interface

> **Upcoming Features**
> - Source citations
> - Multi-document support
> - Chat history
> - Drag & Drop upload
> - Better retrieval strategies

---

## 🏗️ Architecture

```
                 +--------------------+
                 |    User Uploads    |
                 |      PDF File      |
                 +---------+----------+
                           |
                           v
                 +--------------------+
                 | PDF Loader         |
                 +--------------------+
                           |
                           v
                 +--------------------+
                 | Text Chunking      |
                 +--------------------+
                           |
                           v
                 +--------------------+
                 | HuggingFace        |
                 | Embeddings         |
                 +--------------------+
                           |
                           v
                 +--------------------+
                 | ChromaDB           |
                 | Vector Database    |
                 +--------------------+
                           |
             User Question |
                           v
                 +--------------------+
                 | Similarity Search  |
                 +--------------------+
                           |
                           v
                 +--------------------+
                 | Groq Llama Model   |
                 +--------------------+
                           |
                           v
                 +--------------------+
                 | AI Response        |
                 +--------------------+
```

---

# 🛠 Tech Stack

| Category | Technology |
|----------|------------|
| Language | Python |
| Backend | FastAPI |
| Frontend | HTML, CSS, JavaScript |
| LLM | Groq (Llama 3.1) |
| Framework | LangChain |
| Embeddings | HuggingFace Sentence Transformers |
| Vector Database | ChromaDB |
| Document Loader | PyPDFLoader |

---

# 📂 Project Structure

```
Enterprise-Knowledge-Assistant/

│
├── backend/
│   ├── app.py
│   ├── rag.py
│   ├── utils.py
│   └── requirements.txt
│
├── frontend/
│   ├── index.html
│   ├── style.css
│   └── script.js
│
├── uploads/
│
├── chroma_db/
│
├── .env.example
├── README.md
└── requirements.txt
```

---

# ⚙️ Installation

## 1. Clone Repository

```bash
git clone https://github.com/pareek35-4/knowledge-assistant-rag.git

cd enterprise-knowledge-assistant
```

---

## 2. Create Virtual Environment

### Windows

```bash
python -m venv venv

venv\Scripts\activate
```

### Linux / Mac

```bash
python3 -m venv venv

source venv/bin/activate
```

---

## 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 4. Configure Environment Variables

Create a `.env` file.

```env
GROQ_API_KEY=your_groq_api_key
MODEL_NAME=llama-3.1-8b-instant
```

---

## 5. Run Backend

```bash
uvicorn app:app --reload
```

Backend runs on

```
http://localhost:8000
```

---

## 6. Open Frontend

Simply open

```
index.html
```

or serve using

```bash
python -m http.server
```

---

# 🧠 How It Works

1. Upload a PDF document.
2. The document is split into smaller chunks.
3. Each chunk is converted into vector embeddings.
4. Embeddings are stored inside ChromaDB.
5. User asks a question.
6. Relevant chunks are retrieved using semantic similarity.
7. Retrieved context is passed to the LLM.
8. The LLM generates a grounded response.

---


# 📈 Future Improvements

- Multi-document retrieval
- Source citations with page numbers
- Authentication
- Chat history
- Docker support
- Metadata filtering
- Hybrid Search (BM25 + Vector Search)
- Streaming responses
- Multiple LLM provider support
- Document management dashboard

---


# 📄 License

This project is licensed under the MIT License.

---


## ⭐ If you found this project helpful, consider giving it a star!