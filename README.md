# Movie-Recommender

# 🎬 Movie Recommendation System – Content-Based (MovieLens 20M)

This project builds a simple yet effective **content-based recommendation system** using the MovieLens 20M dataset. It recommends movies similar to a given title based on their genre composition using **TF-IDF** and **cosine similarity**.

---

## 📦 Dataset

- **Source**: [MovieLens 20M](https://grouplens.org/datasets/movielens/20m/)
- Files used:
  - `movies.csv` – Movie titles and genres
  - `ratings.csv` – (Loaded but unused in content-based filtering)

---

## 📌 Methodology

### ✅ Step 1: Data Cleaning
- Removed noisy characters from genres
- Reformatted genre strings for vectorization

### ✅ Step 2: TF-IDF Vectorization
- Converted movie genres into TF-IDF vectors using `TfidfVectorizer`
- Each movie represented as a numeric vector of genre weights

### ✅ Step 3: Cosine Similarity
- Calculated **cosine similarity** between every movie pair
- Stored in a similarity matrix for fast lookups

### ✅ Step 4: Recommendation Engine
- User inputs a movie title (e.g., `"Matrix, The (1999)"`)
- Model returns top N movies with the highest cosine similarity scores
- Flexible search helper to locate movie titles by fragment

---

## 📈 Sample Output

```python
recommend_movies("Matrix, The (1999)")
