# 🤖 AI Ticket Assistant - SDAIA Academy Applied NLP Capstone

An advanced, industry-standard Natural Language Processing (NLP) pipeline designed to automate customer support ticket classification, semantic retrieval, and routing with support for English, Modern Standard Arabic (MSA), and Gulf dialects.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1MRJ4xffToP926ALeTunlM3zSWhSsRT5Z)

---

## 🏛️ Academy Context
This project was developed as an individual capstone project for the **[SDAIA Academy](https://github.com/SDAIAAcademy/)** Applied NLP Engineering course.

---

## 🧠 Model & Architecture Pipeline
1. **Multilingual Encoder (Frozen):** Uses `intfloat/multilingual-e5-small` to generate 384-dimensional dense semantic embeddings for both English and multi-dialect Arabic tickets (requiring the `query:` and `passage:` prefixes).
2. **Classifier:** Trained using `LogisticRegression` ($C=20$, max_iter=3000) on the extracted embeddings.
3. **Abstain Routing ($\tau$):** Implements a confidence threshold ($\tau$) to automatically route low-confidence predictions to human review rather than mislabeling them.

---

## 📊 Evaluation & Development Stages (M0 to M3)
The pipeline was evaluated across iterative stages to measure the impact of data expansion, threshold tuning, and leakage control. Results are tracked and exported directly from execution logs.

| Version | Description | Macro-F1 (Overall) | Abstain Rate (%) |
| :--- | :--- | :--- | :--- |
| **M0 (Baseline)** | English baseline model, $\tau=0.5$ | 0.3333 | 0.0% |
| **M1 (Threshold Tuned)** | Baseline model with threshold tuning | 0.3333 | 50.0% |
| **M2 (Synthetic Data Added)** | Added synthetic Arabic/Gulf training data | 0.6667 | 25.0% |
| **M3 (Leakage Checked & Cleaned)** | Cleaned near-duplicates ($>0.95$ similarity) | 0.6667 | 75.0% |

*The complete execution results are saved in `model_evaluation_results.csv` inside the repository.*

---

## 🔍 Leakage Check & Validation
- **Semantic Leakage Control:** Computed cosine similarity matrices between training and test sets. Any training sentence with a similarity $>0.95$ to test sentences was monitored and cleaned to ensure true generalization rather than memorization.

---

## 🛠️ Tech Stack & Requirements
- **Python 3.x** / **Google Colab**
- **Sentence-Transformers** (`intfloat/multilingual-e5-small`)
- **Scikit-Learn** (`LogisticRegression`, `cosine_similarity`)
- **Pandas & NumPy**

---

## 🚀 How to Run
1. Open the executable notebook in Google Colab using the badge above.
2. Install dependencies:
   ```bash
   pip install sentence-transformers scikit-learn pandas numpy gradio
