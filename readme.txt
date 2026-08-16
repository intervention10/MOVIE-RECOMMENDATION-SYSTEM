# 🎬 Movie Recommender System

A content-based movie recommendation web application built with **Python**, **scikit-learn**, and **Streamlit**. The app suggests the top 9 most similar movies based on natural language processing (NLP) of metadata from the TMDB 5000 Movies dataset.

---

## 📌 Project Overview
This project processes text metadata—including genre, plot overview, keywords, top cast, and director—to generate vector embeddings for every movie using a Bag-of-Words model. It calculates pairwise similarity using **Cosine Similarity** to recommend relevant movies instantly.

To optimize application performance, precomputed feature vectors and similarity matrices are exported via `pickle`, allowing the Streamlit web app to load and serve recommendations dynamically with zero runtime calculation overhead.

---

## 🛠️ Key Features
* **Metadata Extraction & Tokenization**: Parses JSON-like string metadata to extract cleaned tokens for genres, keywords, directors, and top 3 cast members.
* **Vectorization**: Transforms combined text tags into 5,000-dimensional numerical vectors using `CountVectorizer` (with English stop-words removed).
* **Similarity Modeling**: Computes pairwise Cosine Similarity across all movies in the TMDB dataset.
* **Streamlit UI**: Clean and interactive web user interface featuring instant dropdown search and structured recommendation outputs.
* **Performance Caching**: Pre-serializes datasets (`movies_dict.pkl`, `similarity.pkl`) to bypass recalculation on app launch.

---

## 🚀 Tech Stack
* **Language:** Python 3.x
* **Data Manipulation:** Pandas, NumPy
* **NLP & ML:** scikit-learn (`CountVectorizer`, `cosine_similarity`)
* **Serialization:** Pickle
* **Web Framework:** Streamlit

---

