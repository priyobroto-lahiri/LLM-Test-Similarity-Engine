# LLM Text Similarity Engine

A professional benchmark suite for evaluating LLM response quality using four distinct statistical and semantic similarity algorithms.

## 🎯 The Problem
Traditional software testing uses "Exact Match" (Boolean) validation. However, LLM outputs are non-deterministic and linguistically diverse. A model might provide a correct answer that uses different words than the ground truth. To evaluate such models, we need mathematical tools that can measure "closeness" on a spectrum from 0 to 1.

## 🛠️ The Approach
This engine benchmarks four industry-standard methods to move from Boolean testing to Statistical evaluation:

1.  **Jaccard Similarity:** Measures word-set overlap (Lexical).
2.  **TF-IDF Cosine Similarity:** Measures weighted keyword overlap, accounting for word importance.
3.  **ROUGE-L:** Measures the Longest Common Subsequence (Structural), ideal for summarization tasks.
4.  **Semantic Similarity (MiniLM):** Uses vector embeddings to measure meaning overlap, even when no words match.

## 📊 Benchmark Results (Preview)
*The results below will be populated after running the final benchmark against Gemini 1.5 Flash and Claude 3 Haiku.*

| Method | Avg Score (Paraphrases) | Avg Score (Contradictions) | Latency (Avg) |
| :--- | :--- | :--- | :--- |
| **Jaccard** | TBD | TBD | TBD |
| **TF-IDF Cosine** | TBD | TBD | TBD |
| **ROUGE-L** | TBD | TBD | TBD |
| **Semantic (SBERT)** | TBD | TBD | TBD |

## 🚀 Tech Stack
- **Language:** Python 3.x
- **Libraries:** scikit-learn, NLTK, Sentence-Transformers, SacreBLEU
- **Deployment:** Streamlit + Hugging Face Spaces
