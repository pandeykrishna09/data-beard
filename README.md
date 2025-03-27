# PREDICTIVE DATA ANALYSIS
## Project Description: Predictive Data Analysis (PDA) on Movie Dataset
## Project Title: Movie Recommender System
## Objective: The primary goal of this project is to perform predictive data analysis on the movie dataset and recommend a movie based on any of the movie which we have liked and seen. It takes into account all the factors such as director, actors, producers, genre, etc of the movie and will recommend 5 movies which are similar to the movie which we have already seen.
## Dataset: [https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata](url) <br> The Dataset can be downloaded from Kaggle and link for same has been given above. The dataset mainly has two files, "tmdb_5000_credits" and "tmdb_5000_movies". Each Excel has following columns:
### tmdb_5000_credits:
- movie_id: Unique ID to identify movies. Also a primary key.
- title: Name of the film
- cast: All the staring casts
- crew: All crew involved in the making of the film
### tmdb_5000_movies:
- budget: Budget of the movie
- genres: Genres to which movie belongs
- homepage: Website of the movie
- id: Unique id and primary key
- keywords: Defines the category to which the movie belongs
- original_language: Language in which the movie is made
- original_title: Initial name of the movie
- overview: Synopsis of the movie
- popularity: How popular was the movie
- production_companies: List of production houses involved in the making of the film.
- production_countries: Countries to which the production companies belongs to
- release_date: Release date of the film
- revenue: Money made by the movie
- runtime: Runtime of the movie
- spoken_languages: Different languages spoken in the movie
- status: Stage of the movie i.e. in production or released or etc.
- tagline: Tagline if given for the movie
- title: Working Title for the movie
- vote_average: Rating based on number of votes
- vote_count: Total number of votes
## **Methodology**

### **1. Data Collection**
- The dataset is sourced from **TMDb (The Movie Database)** and consists of two CSV files:
  - `tmdb_5000_movies.csv`: Contains metadata about movies.
  - `tmdb_5000_credits.csv`: Includes information about the cast, crew, and production teams.
- The datasets are merged using the **title** column.

### **2. Data Preprocessing**
- **Handling missing values**: Any missing or null values in critical columns are handled using imputation or removal.
- **Feature selection**: Extracting relevant columns such as `genres`, `keywords`, `overview`, `cast`, and `crew` for recommendation.

### **3. Text Processing**
- **Tokenization & Vectorization**: The movie descriptions and metadata are converted into numerical vectors using **TF-IDF** or **Count Vectorizer**.
- **Dimensionality Reduction**: If necessary, techniques like **Principal Component Analysis (PCA)** or **Truncated SVD** are applied to reduce feature space.

### **4. Similarity Measurement**
- A **cosine similarity matrix** is created based on textual and categorical features to measure the closeness between movies.
- **Alternative approaches**:
  - **Content-based filtering** using movie descriptions, genres, and cast.
  - **Collaborative filtering** if user preferences are available.

### **5. Recommendation Engine**
- Given a movie title, the system finds **N most similar movies** based on the similarity scores.
- The results are ranked in descending order of relevance.

### **6. Evaluation**
- The system’s performance is assessed using:
  - **Precision & Recall** metrics.
  - **User feedback analysis** (if available).

### **7. Deployment**
- The model can be deployed using:
  - A **Flask API** for web-based recommendations.
  - **Streamlit** or other interactive dashboards for a user-friendly interface.
### Requirements:
- Python 3.6+
- Pandas
- NumPy
- Scikit-learn
