# Smart Recruitment System - RAG + FAISS

AI-powered resume screening system that ranks candidates based on semantic similarity to Job Description.

## 🚀 Project Overview
Recruiters spend hours filtering resumes manually. This system automates it using RAG architecture. It converts resumes and JD into vectors and finds the best match.

## 🛠️ Tech Stack
- Sentence-Transformers (all-MiniLM-L6-v2)
- FAISS for fast similarity search
- Python, Pandas, Matplotlib

## ⚙️ How it Works
1. Indexing: Resumes -> Embeddings -> FAISS Index
2. JD Query -> Embedding
3. Semantic Search using Cosine Similarity
4. Ranked Output

## 📊 Results & Graphs

**Top Candidate Matching:**
System identified RES-007 as best match with 64.15% score.

| Candidate | Match Score | Rank | Verdict |
| :--- | :--- | :--- | :--- |
| RES-007 | 64.15% | 1 | Best Match |
| RES-004 | 33.27% | 2 | Moderate |
| RES-010 | 24.66% | 3 | Low |

**Graph Analysis:** Similarity Distribution graph shows clear gap between Rank 1 (64%) and Rank 2 (33%), proving semantic search works better than keyword matching.

## ▶️ How to Run
1. Open `Smart_Recruitment_System.ipynb` in Colab
2. `pip install sentence-transformers faiss-cpu`
3. Run all cells

## 👨‍💻 Author
Irajees Rajarajeswari I - M.Sc Mathematics
