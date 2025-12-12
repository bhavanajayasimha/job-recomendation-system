<p align="center">
  <img src="https://img.shields.io/badge/AI%20Hiring%20Engine-Job%20Recommendation%20System-blueviolet?style=for-the-badge" />
</p>

<h1 align="center">🔍 Intelligent Job Recommendation & Candidate Ranking System</h1>

<p align="center">
A lightweight, high-performance ML pipeline that ranks candidates for a job using 
<b>TF-IDF</b>, <b>DistilBERT embeddings</b>, and a <b>Logistic Regression predictor</b>.
</p>

---

## 🚀 **Run the Project in Google Colab**
Click below to launch the notebook instantly:

👉 [**Colab Notebook:**](https://colab.research.google.com/drive/1CDVZCc0WZhl9JVSeyabJChtPtDMmfA3h)

---

## 📌 **Project Overview**

This project implements a **hybrid candidate ranking engine** inspired by real-world hiring platforms.  
It combines:

- **TF-IDF similarity** (classical NLP)
- **BERT-based semantic similarity** (DistilBERT)
- **A logistic regression relevance estimator**
- **A hybrid weighted scoring model**

The output is a **ranked list of candidates** sorted by best match → worst match.

Perfect for:
- Research papers  
- ML-based HR tools  
- Resume/job-matching prototypes  
- Student innovation competitions  

---

## 🧠 **How the Model Works**

### **1️⃣ Job Description Processing**
The JD title + description are merged and processed using:
- TF-IDF Vectorizer  
- DistilBERT encoder  

### **2️⃣ Candidate Feature Extraction**
Each candidate’s combined profile (skills + experience + project summary) is embedded using:
- TF-IDF  
- DistilBERT  

### **3️⃣ Model Components**

| Component | Purpose |
|----------|---------|
| **TF-IDF Similarity** | Measures keyword overlap |
| **Embedding Similarity (BERT)** | Measures semantic closeness |
| **Logistic Regression** | Classifies suitability using synthetic label (experience ≥ 3 years) |
| **Hybrid Score** | Weighted signal combining all 3 |

### **4️⃣ Final Ranking**
Candidates are sorted based on:
final_score = 0.35 * tfidf_sim
+ 0.40 * embedding_sim
+ 0.25 * logistic_reg_prob

### **Conclusion**
This project shows how modern hiring systems combine classical ML, semantic embeddings, and simple heuristics to produce meaningful ranking outputs.
It is easy to extend, experiment with, and integrate into real HR tech stacks.
