# 📘 Word Similarity Clustering from Literature — NLP Project

![Typing Header](https://readme-typing-svg.demolab.com?font=Fira+Code&size=24&pause=1000&color=F59E0B&center=true&vCenter=true&width=850&lines=📚+Semantic+Clustering+From+Classic+Novels;🧠+Nouns+as+Nodes+in+a+Meaning+Graph)

<p align="center">
  <img src="https://img.shields.io/badge/NLP-Graph%20Clustering-blue?style=for-the-badge&logo=python"/>
  <img src="https://img.shields.io/badge/Text%20Analysis-Gutenberg-green?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/MDS-KMeans-orange?style=for-the-badge"/>
</p>

---

## 🧠 Overview

This project clusters the top 100 most frequent **nouns** from six literary works using two semantic similarity methods:

- 📐 **Graph-Based Similarity**: co-occurrence graph + Dijkstra distance
- 🧬 **Embedding-Based Similarity**: Word2Vec + t-SNE projection

The goal is to discover latent meaning structures in classical literature.

---

## 📘 Corpus

Classic English novels from [Project Gutenberg](https://www.gutenberg.org/):

- *Frankenstein*
- *Twenty Thousand Leagues Under the Sea*
- *Pride and Prejudice*
- *The Adventures of Sherlock Holmes*
- *Moby Dick*
- *Jack Pumpkinhead of Oz*

> 📏 ~30,000 sentences | 📚 ~2.5M words

---

## 🔍 Methodology

### 🔤 Preprocessing
- Cleaned text, tokenized with NLTK
- Extracted top 100 nouns via POS tagging

### 🕸️ Graph-Based Clustering
- Created co-occurrence graph of nouns (100×100)
- Edge weights = 1 / co-occurrence count (to form distance)
- Used **Dijkstra’s algorithm** to compute shortest paths
- Applied **MDS** for dimensionality reduction
- Clustered with **KMeans (k=5)**

### 🧭 Embedding-Based Clustering
- Trained **Word2Vec** on the corpus
- Applied **t-SNE** for visualization
- Clustered using **KMeans**

---

## 📊 Results

| Method           | Silhouette Score |
|------------------|------------------|
| Graph Distance   | ⭐ **0.479**      |
| Word2Vec (t-SNE) | 0.316            |

✅ **Final Insight**:  
Graph-based clustering using co-occurrence + Dijkstra outperforms embedding-based methods for this task.

🧠 **What It Means**:  
Literal co-presence in literary context reveals deeper thematic groupings like:
- 👤 Characters (man, captain, woman)
- 🏠 Locations (room, street, sea)
- 🔧 Objects (boat, gun, window)
- ❤️ Emotions (love, fear, truth)

---

## ⚙️ Tech Stack

| Component          | Tools & Libraries            |
|--------------------|------------------------------|
| Language           | Python 3.10                  |
| Preprocessing      | NLTK                         |
| Graph Analysis     | NetworkX                     |
| Clustering         | KMeans (sklearn)             |
| Dim. Reduction     | MDS, t-SNE                   |
| Visualization      | Matplotlib, Seaborn          |

---

## 🚀 Quick Start

```bash
# Clone the repo
git clone https://github.com/yourusername/word-graph-nlp.git
cd word-graph-nlp

# Launch notebook
jupyter notebook Final_Code.ipynb
```
