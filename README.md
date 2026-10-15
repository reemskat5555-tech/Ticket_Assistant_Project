# 🎫 AI Ticket Assistant - SDAIA Academy Capstone Project

An advanced, industry-standard Natural Language Processing (NLP) pipeline designed to automate customer support ticket classification and semantic retrieval.

---

## 📌 Project Architecture & Pipeline
This project is built using a robust two-step technical pipeline:
1. **Step 1: Advanced Text Classification**
   - Utilizes deep learning `Sentence-Transformers` (`all-MiniLM-L6-v2`) and a `LogisticRegression` classifier to accurately categorize incoming support tickets.
2. **Step 2: Semantic Retrieval & Grounded Generation (RAG)**
   - Computes cosine similarity between new tickets and historical archives to retrieve the most relevant past case and generate a grounded, hallucination-free response.

---

## 🛠️ Tech Stack
- **Python**
- **Google Colab** (Development Environment)
- **Sentence-Transformers** (For text embeddings)
- **Scikit-Learn** (For classification & cosine similarity)
- **Pandas** (For data handling)

---

## 🚀 How to Run
1. Open the project notebook in Google Colab.
2. Ensure required libraries are installed:
   ```bash
   pip install sentence-transformers scikit-learn pandas
   
   https://github.com/SDAIAAcademy
