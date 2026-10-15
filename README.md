# 🤖 AI Ticket Assistant - SDAIA Academy Capstone Project

An advanced, industry-standard Natural Language Processing (NLP) pipeline designed to automate customer support ticket classification and semantic retrieval.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)

---

## 🏛️ Academy Context
This project was developed as part of the Capstone Project requirements for the **[SDAIA Academy](https://github.com/SDAIAAcademy/)** AI Program.

---

## 🧠 Model & Architecture Pipeline
This project implements a robust two-step AI pipeline:
1. **Step 1: Advanced Text Classification**
   - Uses deep learning `Sentence-Transformers` (`all-MiniLM-L6-v2`) to extract dense semantic embeddings from customer support tickets.
   - Fits a `LogisticRegression` classifier on the embeddings to accurately categorize incoming issues into predefined departments.
2. **Step 2: Semantic Retrieval & Grounded Generation (RAG)**
   - Computes `Cosine Similarity` between new incoming tickets and historical archived cases to fetch the most relevant past solution, ensuring a grounded, hallucination-free response.

---

## 📊 Evaluation Metrics & Score
The classification model was rigorously tested on validation and test splits, achieving high performance across all standard metrics:

| Evaluation Metric | Score |
| :--- | :--- |
| **Accuracy** | **0.95+** |
| **Precision** | **0.95+** |
| **Recall** | **0.95+** |
| **F1-Score** | **0.95+** |

*Detailed classification reports, confusion matrices, and execution outputs are fully traceable inside the Jupyter/Colab Notebook.*

---

## 💻 Code & Colab Notebook
- **Executable Notebook:** You can access the complete end-to-end code, data pipeline, and training logs via [`Ticket_Assistant_Project.ipynb`](./Ticket_Assistant_Project.ipynb).

---

## 🛠️ Tech Stack & Requirements
- **Python 3.x**
- **Google Colab** (Development & Execution Environment)
- **Sentence-Transformers** (For semantic text embeddings)
- **Scikit-Learn** (For Logistic Regression classifier & cosine similarity metrics)
- **Pandas & NumPy** (For structured data processing)

---

## 🚀 How to Run

1. Open the project notebook in Google Colab using the badge above or via the repository files.
2. Install the required dependencies by running:
   ```bash
   pip install sentence-transformers scikit-learn pandas
