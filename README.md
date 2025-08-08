# 📚 Word Similarity Clustering from Literature  
**Discovering hidden meaning structures in classic novels using NLP, Graph Theory & Word Embeddings**  

<p align="center">
  <img src="https://img.shields.io/badge/Domain-NLP-blue?style=for-the-badge&logo=python"/>
  <img src="https://img.shields.io/badge/Approach-Graph%20%26%20Embedding-orange?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Tech-Python%20%7C%20NLTK%20%7C%20sklearn%20%7C%20NetworkX-green?style=for-the-badge"/>
</p>

---

## 🚀 Executive Summary  
In this project, I applied **two semantic similarity methods** to cluster the top 100 most frequent nouns from **six classic novels**.  
The goal: **Reveal hidden thematic structures** such as characters, locations, objects, and emotions — without manual labeling.  

**Key Result:**  
📊 **Graph-based co-occurrence + Dijkstra’s algorithm outperformed Word2Vec embeddings** for thematic clustering in this dataset.  

---

## 🎯 Why This Matters to a Recruiter
- **Real-world relevance:** Shows ability to work with **messy, large-scale text data** and extract structured insights.  
- **Multi-technique approach:** Combines **graph theory** + **unsupervised ML** + **NLP preprocessing**.  
- **End-to-end pipeline:** From raw text acquisition to final visual clusters.  
- **Measurable outcome:** Compared algorithms using **Silhouette Score** for objective evaluation.  

---

## 📂 Dataset
**Source:** [Project Gutenberg](https://www.gutenberg.org/)  
**Works Used (~2.5M words, ~30k sentences):**
- *Frankenstein*
- *Twenty Thousand Leagues Under the Sea*
- *Pride and Prejudice*
- *The Adventures of Sherlock Holmes*
- *Moby Dick*
- *Jack Pumpkinhead of Oz*

---

## 🛠 Methodology Overview

| Step | Description | Tools |
|------|-------------|-------|
| **1. Preprocessing** | Text cleaning, tokenization, POS tagging to extract top 100 nouns | NLTK |
| **2. Graph-Based Similarity** | Build co-occurrence graph → Edge weight = 1 / frequency → Dijkstra shortest paths → MDS reduction → KMeans clustering | NetworkX, sklearn |
| **3. Embedding-Based Similarity** | Train Word2Vec → t-SNE reduction → KMeans clustering | Gensim, sklearn |
| **4. Evaluation** | Compare clustering with Silhouette Score | sklearn |
| **5. Visualization** | 2D plots of clusters for interpretability | Matplotlib, Seaborn |

---

## 📊 Results at a Glance

| Method                 | Silhouette Score | Insight |
|------------------------|------------------|---------|
| **Graph Distance (MDS)** | ⭐ **0.479**     | Strong thematic grouping |
| **Word2Vec (t-SNE)**    | 0.316            | Weaker separation |

**Themes Identified**:  
- 👤 Characters: *man, captain, woman*  
- 🏠 Locations: *room, street, sea*  
- 🔧 Objects: *boat, gun, window*  
- ❤️ Emotions: *love, fear, truth*

---

## 🧠 Key Takeaways
- **Graph-based methods excel in small, domain-specific corpora** where co-occurrence patterns are rich.
- Embeddings can underperform without very large, diverse training data.
- Combining linguistic intuition with algorithmic modeling yields stronger insights.

---

## ⚙️ Tech Stack
**Languages:** Python 3.10  
**Libraries:** NLTK, NetworkX, scikit-learn, gensim, matplotlib, seaborn  
**Concepts Applied:**  
- NLP preprocessing & POS tagging  
- Graph construction & shortest path algorithms  
- Dimensionality reduction (MDS, t-SNE)  
- Clustering & evaluation metrics  

---

## 🖥 Quick Start
```bash
# Clone repository
git clone https://github.com/yourusername/word-graph-nlp.git
cd word-graph-nlp
```

# Launch analysis
jupyter notebook Final_Code.ipynb

## 📌 Impact Statement
This project demonstrates my ability to **design, implement, and evaluate** a complete NLP pipeline — leveraging both **graph algorithms** and **machine learning** to solve an open-ended semantic problem. It highlights skills in **data wrangling, algorithm selection, and results interpretation** — all critical in production-grade AI systems.

