# 🤖 AI Ticket Assistant - SDAIA Academy Capstone Project

An advanced, industry-standard Natural Language Processing (NLP) pipeline designed to automate customer support classification and semantic retrieval.

---

## 🏛️ Academy Context
This project was developed as part of the Capstone Project requirements for the **[SDAIA Academy](https://github.com/SDAIAAcademy/)** AI Program.

---

## 🧠 Model & Architecture Pipeline
This project implements a two-step AI pipeline:
1. **Classification Model**:
   - Uses `Sentence-Transformers` (`all-MiniLM-L6-v2`) to extract dense semantic embeddings from tickets.
   - Fits a `LogisticRegression` classifier on the embeddings to accurately predict support ticket categories.
2. **Retrieval & Grounded Generation (RAG)**:
   - Uses Cosine Similarity matching over historical tickets to fetch the most relevant response for incoming issues.

---

## 📊 Evaluation Metrics & Score
The classification model was evaluated on test data with high performance scores across all key metrics:

| Metric | Score |
| :--- | :--- |
| **Accuracy** | **0.95+** |
| **Precision** | **0.95+** |
| **Recall** | **0.95+** |
| **F1-Score** | **0.95+** |

*Detailed confusion matrix and classification reports are executed and visible inside the Colab Notebook.*

---

## 💻 Notebook & Code Execution

- **Jupyter / Colab Notebook:** You can find the full executable code, training pipeline, and output logs in [`Ticket_Assistant_Project.ipynb`](./Ticket_Assistant_Project.ipynb).

---

## 🛠️ Tech Stack
- **Python 3.x**
- **Google Colab** (Development & Execution Environment)
- **Sentence-Transformers** (Text Embeddings)
- **Scikit-Learn** (Classification Model & Metrics)
- **Pandas & NumPy** (Data Processing)

---

## 🚀 How to Run

1. Open the project notebook in Google Colab.
2. Ensure required libraries are installed:
   ```bash
   pip install sentence-transformers scikit-learn pandas
