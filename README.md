# 🚀 Simple Groq RAG Pipeline  
### *Retrieval-Augmented Generation with Dynamic Chunking + Multilingual Question Support*

This project implements a **minimal, clean, and production-ready RAG (Retrieval-Augmented Generation)** pipeline using:

- **Groq’s OpenAI-compatible Responses API**  
- **`openai/gpt-oss-120b` model**  
- **SentenceTransformers embeddings**  
- **FAISS similarity search**

You can upload *any* document and then ask questions like:

- **“Summarize this document.”**  
- **“Is document ka summary kya hai?”** (Hindi)  
- **“¿Cuál es el punto principal del documento?”** (Spanish)

The pipeline automatically retrieves the most relevant chunks from the document and sends them to an LLM for grounded question answering.

---

## 🌟 Key Features

### 🔹 **1. Dynamic Chunking**
Instead of fixed-size splits, the system uses **configurable chunk size + overlap**, allowing:

- Better semantic grouping  
- Reduced hallucinations  
- More accurate retrieval  
- Flexibility across different document types  

Modify these easily via environment variables:

```env
CHUNK_SIZE=700
CHUNK_OVERLAP=150
