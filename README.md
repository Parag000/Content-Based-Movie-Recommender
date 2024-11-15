# Movie Recommendation System (Content Based Filtering) 🎬

This project demonstrates the use of content-based filtering to recommend movies based on metadata features like cast, genres, director, and production company. The focus of this project is on understanding and implementing various text vectorizers and similarity metrics to create a basic recommendation system, rather than optimizing model performance.

---

Run this notebook on Google Colab 
--
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1vO0rg_TYcj72W5lwi0GH34f2v7vjvPiJ?usp=sharing)

---

## What I Learned in This Project 🎬💡

In this project, my focus was to learn how text vectorizers and cosine similarity works. Below is my approach to build a recommendation system. Note that this project is not focused on improving performance of the model  

1. **Textual Feature Engineering** 📝  
   - Learned to create a "metadata soup" by combining multiple textual features into a single string for each movie. 
   - Explored the use of CountVectorizer to create a term-frequency matrix for the metadata soup.

2. **Cosine Similarity for Recommendations** 🔍  
   - Understood the concept of cosine similarity and its application in content-based filtering to identify similar items based on textual data.
   - Practiced using cosine_similarity to calculate pairwise similarities across all movies, allowing for efficient retrieval of similar movies.

3. **Building a Recommendation Function** 🎯  
   - Learned to build a function that takes a movie title as input and retrieves the most similar movies by sorting similarity scores.

4. **Using Pandas for Index Mapping** 🗂️  
   - Discovered the importance of indexing by creating a dictionary that maps movie titles to DataFrame indices, enabling efficient lookups.

---

### Vectorizers I Explored for the Project

1. **Count Vectorizer**: 
   - Creates a sparse matrix
   - Each row represents a document and every word is a column
   - Count matrix = frequency of word in the document
   - Computationally expensive due to high dimensionality
   - Does not account for semantics

2. **TF-IDF (Term Frequency-Inverse Document Frequency) Vectorizer**

   - Creates sparse matrix and is computationally expensive

   - Term Frequency (TF):
     - Represents the relative frequency of a word in a document.
     - No. of occurrences of the term / Total no. of terms
  
   - Inverse Document Frequency (IDF):
     - Measures how common or rare a word is across all documents.
     - log (Total no. of doc / No. of doc with that word)

   - The overall importance of each word in a document is the product of TF and IDF.

3. **Word2Vec**

   - Takes account of textual semantics
   - Embedding based approach
   - Requires large datasets to learn meaningful embeddings
   - Two models in Word2Vec - Skip Gram and CBOW
   - Word level analysis

---

### Similarity Based Models

1. **Cosine Similarity**
   - Calculates similarity based on the angle between the vectors in an n-dimensional space
   - Values range from -1 (opposite) to 1 (identical), with 0 indicating orthogonal (no similarity).

2. **Jaccard Similarity**
   - Measures similarity as the size of the intersection divided by the size of the union of two sets.
   - Used for categorical data
   - It's not vector based

3. **Pearson Correlation**
   - Measures the linear correlation between two vectors.
   - Frequently used in collaborative filtering for user and item similarity in rating-based recommendation systems.

4. **Euclidean Distance**
   - Calculates the "straight-line" or absolute distance between two points in space.

---

## Getting Started

### Prerequisites

- Python 3.7+
- Libraries: `pandas`, `numpy`, `scikit-learn`

### Running Locally (Not Recommended)
```bash
git clone https://github.com/Parag000/Content-Based-Movie-Recommender.git
```
### Installation

Install the required Python libraries using:

```bash
pip install pandas numpy scikit-learn
```
