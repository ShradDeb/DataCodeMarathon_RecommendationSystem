# Movie Recommender System

This repository contains a **Movie Recommendation System** built using Python and Streamlit. The system uses machine learning to recommend movies based on similarity between movie features.

---

## 📂 Files in this Repository

| File / Folder | Description |
|---------------|-------------|
| `RecommenderSystem.ipynb` | Jupyter Notebook with code to analyze movie data and build the recommendation system. |
| `tmdb_5000_credits.csv` | Dataset containing movie credits (actors, crew, directors). |
| `tmdb_5000_movies.csv` | Dataset containing movie metadata such as title, genres, and release dates. |
| `README.md` | This file explaining the repository contents and usage. |

---

## ⚠️ Files Not Uploaded

| File | Reason |
|------|--------|
| `artifacts/similarity.pkl` | Exceeds GitHub's 100MB file size limit. Contains precomputed similarity matrix for the recommendation system. Can be generated locally using the notebook. |
| `artifacts/movie_list.pkl` | Exceeds GitHub's file size limit. Contains the list of movie dataframes used in the app. Can be generated locally using the notebook. |

> These large files are necessary for running the Streamlit app directly but can be recreated by running `RecommenderSystem.ipynb` on your local machine.

---

## ⚙️ How the Recommender System Works

1. **Load Movie Data**:  
   The system loads movie metadata and credits from the CSV files.

2. **Compute Similarity Matrix**:  
   A similarity matrix is computed based on movie features (like genres, keywords, cast, crew, etc.) using techniques such as **cosine similarity**.

3. **Select a Movie**:  
   The user selects a movie from a dropdown menu.

4. **Find Recommendations**:  
   The system finds the top 5 movies most similar to the selected movie based on the similarity matrix.

5. **Fetch Posters**:  
   The system fetches movie posters dynamically using the [TMDb API](https://www.themoviedb.org/documentation/api).

6. **Display Recommendations**:  
   Using **Streamlit**, the system displays the recommended movies along with their posters in a neat layout.

---

## 💻 Usage

1. Clone the repository:
```bash
git clone https://github.com/ShradDeb/DataCodeMarathon_RecommendationSystem.git
cd DataCodeMarathon_RecommendationSystem

Install required packages:
pip install -r requirements.txt

Run Jupyter Notebook to recreate the missing files:
jupyter notebook RecommenderSystem.ipynb

Run the Streamlit app locally:
streamlit run app.py

Notes

The precomputed similarity matrix and movie list are too large for GitHub, but they can be generated locally from the CSV datasets.

This project demonstrates a basic recommendation system workflow, including:

Data preprocessing

Feature engineering

Similarity calculation

Recommendation display
