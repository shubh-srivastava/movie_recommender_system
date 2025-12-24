# Movie Recommender System

## Overview
This project implements a **content-based movie recommender system** that suggests movies similar to a user’s selected title.

The system analyzes movie metadata (genres, description, keywords, etc.) to compute similarities and presents the top recommendations.

## Features
- Processes a movie dataset (e.g., TMDB data).
- Computes pairwise similarities using TF-IDF and cosine similarity.
- Generates top-N similar movie recommendations.
- Deploys the recommendation API via Heroku for easy remote usage.

## Getting Started

### Prerequisites
- Python 3.x
- Libraries: `pandas`, `scikit-learn`, `flask`
- (Optional) `gunicorn` for production deployment

### Installation
```bash
git clone https://github.com/shubh-srivastava/movie_recommender_system.git
cd movie_recommender_system
pip install -r requirements.txt
```

### Running Locally
```bash
python app.py
```
- Open your browser at `http://127.0.0.1:5000/`.
- Enter a movie name to retrieve the top 5 similar recommendations.

## Project Structure
```
movie_recommender_system/
├── movies_metadata.csv       # Movie dataset
├── app.py                    # Flask application
├── model.py                  # TF‑IDF + cosine similarity logic
├── requirements.txt          # Dependencies
└── README.md                 # Project overview
```

## How It Works
1. **Data Loading:** Load movie metadata (title, overview, genres, etc.).
2. **Feature Extraction:** Concatenate relevant text into a single “feature” field per movie.
3. **Vectorization:** Convert text into TF-IDF vectors.
4. **Similarity Computation:** Compute cosine similarity across movies.
5. **Recommendation Logic:** Given a movie title, find its index, retrieve top similar movies, and display their titles.

## Example Use
- Input: *"Inception"*
- Output: Top 5 recommended movies with similar content and themes.

## Contributing
Contributions are welcome! Please consider:
- Adding collaborative or hybrid filtering.
- Improving front-end UI (e.g., with Streamlit or React).
- Enhancing dataset (posters, ratings, runtime).
- Optimizing recommendation logic or caching popular queries.
