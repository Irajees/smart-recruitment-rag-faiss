<img width="960" height="540" alt="image" src="https://github.com/user-attachments/assets/e81b451c-1c37-434f-a7a9-f56f6620f795" /># smart-recruitment-rag-faiss
AI-powered resume screening system using Sentence-Transformers &amp; FAISS. Ranks candidates by semantic similarity to Job Description, not just keywords. Built with RAG architecture.
# 🤖 Smart Recruitment System using RAG & FAISS

> An AI-powered resume screening and candidate matching system that goes beyond keyword search.



### 📌 Problem Statement
Traditional recruitment is manual and time-consuming. Keyword-based ATS often misses semantically relevant candidates.

### 💡 Solution
We built a Semantic Search based system using **Retrieval Augmented Generation (RAG)** architecture. Resumes are converted into 384-dimensional vectors and stored in FAISS for ultra-fast similarity search with Job Descriptions.

### 🚀 Tech Stack
- **Embedding Model:** `sentence-transformers/all-MiniLM-L6-v2`
- **Vector Database:** FAISS `IndexFlatL2`
- **Similarity Metric:** Cosine Similarity
- **PDF Parsing:** PyMuPDF (fitz)
- **Visualization:** Matplotlib & Pandas

### 🏗️ Architecture
`PDF Resumes -> Text Extraction (fitz) -> Embedding (MiniLM) -> FAISS Indexing -> JD Query -> Semantic Search -> Ranked Results`

### 📊 Results
For the Job Description: `AI Engineer (Python, FastAPI, NLP, LLMs, RAG, FAISS, Generative AI)`

| Resume Name | Match Score (%) | Status |
| :--- | :--- | :--- |
| Akash_AI_Engineer.pdf | **64.15%** | Highly Suitable |
| Rahul_Data_Scientist.pdf | 33.89% | Moderate |
| Priya_Java_Developer.pdf | 8.42% | Low Match |

**Graph Output:**
The system correctly identified the AI Engineer as the top candidate, proving semantic understanding > keyword matching.

### ⚙️ How to Run
```bash
pip install sentence-transformers faiss-cpu pymupdf scikit-learn
