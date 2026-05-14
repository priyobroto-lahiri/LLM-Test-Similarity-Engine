# LLM Text Similarity Engine

A professional benchmark suite for evaluating LLM response quality using four distinct statistical and semantic similarity algorithms. This project is part of a 5-month transition to AI Evaluation Engineering.

## 🎯 The Problem
Traditional software testing uses "Exact Match" (Boolean) validation. However, LLM outputs are non-deterministic and linguistically diverse. A model might provide a correct answer that uses different words than the ground truth. To evaluate such models, we need mathematical tools that can measure "closeness" on a spectrum from 0 to 1.

## 🛠️ The Approach
This engine benchmarks four industry-standard methods to move from Boolean testing to Statistical evaluation:

1.  **Jaccard Similarity (Lexical):** Measures word-set overlap. Optimized with `str.translate` for high-performance punctuation removal.
2.  **TF-IDF Cosine Similarity (Weighted Lexical):** Measures weighted keyword overlap, accounting for word importance.
3.  **ROUGE-L (Structural):** Measures the Longest Common Subsequence, ideal for summarization tasks.
4.  **Semantic Similarity (SBERT):** Uses vector embeddings (all-MiniLM-L6-v2) to measure meaning overlap.

## 📈 Current Project Status: Phase 1
- [x] **Jaccard Similarity Implementation:** Completed in Jupyter laboratory.
    - [x] Case-insensitive normalization.
    - [x] High-performance punctuation stripping (C-level optimization).
    - [x] Verification against "Near Match" and "Paraphrase" datasets.
- [ ] **ROUGE-L Prototyping:** In Progress.
- [ ] **TF-IDF & Semantic Implementation:** Upcoming.

## 🚀 Repository Structure
- `notebooks/`: 01_similarity_prototyping.ipynb (Active laboratory for algorithm development).
- `data/`: Sample reference and candidate pairs for benchmarking.
- `docs/`: Curriculum and progress tracking.

## 🛠️ Tech Stack
- **Language:** Python 3.13+ (Base Anaconda Environment)
- **Core Libraries:** Pandas, string.translate, rouge-score (planned), sentence-transformers (planned)
- **Workflow:** Socratic Scaffolding 2.0 (Logic -> Structure -> Implementation)
