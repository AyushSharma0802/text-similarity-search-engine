# 🔍 Text Similarity Search Engine (Quora Question Pairs)

This project is a **text similarity search engine** built using the **Quora Question Pairs dataset**. It helps identify whether two questions are semantically similar using **TF-IDF vectorization** and **cosine similarity**.

> ✅ Suitable for showcasing NLP, Information Retrieval, and Evaluation skills for internships or job applications.

---

## 📦 Dataset

- **Name:** Quora Duplicate Questions
- **Source:** [Quora Kaggle Dataset](https://www.kaggle.com/c/quora-question-pairs/data)
- **Size:** ~400,000 question pairs
- **Format:** TSV (`question1`, `question2`, `is_duplicate`)

---

## ⚙️ Technologies Used

- Python
- Pandas & Numpy
- Scikit-learn (TF-IDF, Cosine Similarity)
- NLTK (stopword removal)
- Matplotlib (visualizations)

---

## 🧠 Project Workflow

### 1. Data Preprocessing
- Lowercasing
- Removing special characters
- Stopword removal using NLTK

### 2. Vectorization
- TF-IDF vectorization on combined questions

### 3. Similarity Calculation
- Cosine similarity between question1 and question2 vectors

### 4. Visualization
- Histogram showing distribution of similarity scores for:
  - Duplicate question pairs
  - Non-duplicate question pairs

---

## 📊 Key Insights

- **High cosine similarity (~1.0)** usually indicates actual duplicates.
- **Very low similarity (~0.0)** usually indicates non-duplicates.
- **Middle range (0.3–0.7)** shows overlap → TF-IDF struggles with semantically similar but lexically different text.

---

## 🔍 Try the Search Engine

A custom function lets you input any question and returns top 5 most similar questions from the dataset.

```python
find_similar_questions("How can I learn Python?")
