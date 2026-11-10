# Smart Subject Tutor

Open-source RAG tutor for B.Tech subjects with adaptive teaching styles and zero API keys.

## Features
- RAG-powered subject notes retrieval
- ChromaDB vector indexing with cosine similarity
- Sentence-transformers embeddings
- Qwen 2.5 0.5B instruction model on CPU
- Four teaching styles: ELI10, Exam Topper, Socratic Professor, Practical Engineer

## Quick start
```bash
python3 -m venv .venv
source .venv/bin/activate
pip install torch --index-url https://download.pytorch.org/whl/cpu
pip install -r requirements.txt
streamlit run app.py
```

## Project files
- `data/subject_notes.md` — subject notes used as the knowledge base
- `rag_engine.py` — embedding, chunking, retrieval, and generation logic
- `app.py` — Streamlit UI

## Notes
- The app stores ChromaDB state in `.chroma_db/` and keeps it out of version control.
- First launch downloads the embedding model and the Qwen model from Hugging Face; subsequent runs are faster.
