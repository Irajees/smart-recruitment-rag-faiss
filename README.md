# Smart Recruitment System - RAG + FAISS

AI-powered resume screening system that ranks candidates based on semantic similarity to Job Description, not just keyword matching.

## 🚀 Project Overview
Recruiters spend hours filtering resumes manually. This system automates it using RAG architecture. It converts resumes and Job Description into vectors and finds the best match, solving the keyword-bias problem.

## 🛠️ Tech Stack
- **Sentence-Transformers (all-MiniLM-L6-v2):** For text to 384-dim embeddings
- **FAISS:** For fast vector similarity search
- **Python, Pandas, Matplotlib**

## ⚙️ Architecture / How it Works
1.  **Indexing:** All 10 Resumes -> Cleaned -> Embeddings -> Stored in FAISS Index
2.  **JD Query:** Job Description -> Embedding (Query Vector)
3.  **Semantic Search:** FAISS calculates Cosine Similarity
4.  **Ranked Output:** Top candidates sorted by Match %

## 📊 Results & Graphs

### Top Candidate Matching
The system correctly identified the most relevant candidate with 64.15% semantic match.

![Result Table](result.png)

### Similarity Distribution Graph
Graph shows clear difference between best match and other candidates. Proves semantic search works better than keywords.

![Graph](graph.png)

| Candidate | Match Score | Rank | Verdict |
| :--- | :--- | :--- | :--- |
| RES-007 | 64.15% | 1 | Best Match |
| RES-004 | 33.27% | 2 | Moderate |
| RES-010 | 24.66% | 3 | Low |

> Inference: Candidate 7 is most suitable for Python Developer role.

## ▶️ How to Run
1. Open `Smart_Recruitment_System.ipynb` in Google Colab
2. `pip install sentence-transformers faiss-cpu matplotlib`
3. Run all cells

## 👨‍💻 Author
Irajees Rajarajeswari I - M.Sc Mathematics
