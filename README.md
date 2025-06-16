# Spotify Music Clustering & Recommendation System

This project clusters a large dataset of Spotify tracks using audio features to group similar songs and build a basic recommendation system.

## Dataset

- ~114,000 Spotify tracks with features like danceability, energy, loudness, speechiness, acousticness, tempo, and more.
- Source: [Your dataset source if public] or describe the dataset.

## Features Used

- Numerical audio features: danceability, energy, loudness, speechiness, acousticness, instrumentalness, liveness, valence, tempo, duration_ms, etc.

## Methodology

1. **Data Cleaning & Preprocessing:**
   - Removed duplicates and missing values.
   - Standardized numerical features using `StandardScaler`.
   - Dimensionality reduction via PCA to 10 components.

2. **Clustering:**
   - Used KMeans clustering with 8 clusters (optimal via Elbow method).
   - Compared results with Gaussian Mixture Models (GMM).
   - Evaluated with silhouette score and Adjusted Rand Index.

3. **Recommendation System:**
   - Recommends songs by finding tracks within the same cluster.
   - Includes fallback for songs not found in dataset.

## How to Use

- Run `recommend_songs(song_name, num_recommendations=5)` to get similar song recommendations.
- Evaluate clustering performance with built-in functions.

## Results

- KMeans clustering yielded well-separated groups of songs.
- GMM clustering provided probabilistic clusters with slightly lower silhouette scores.
- Precision@5 for recommendations was 100%, recall was low, indicating precise but narrow recommendations.

## Future Work

- Integrate NLP features for artist/genre.
- Explore deep learning for feature extraction.
- Implement collaborative filtering for personalized recommendations.

## Requirements

- Python 3.x
- pandas, numpy, matplotlib, seaborn
- scikit-learn

## How to Run

1. Clone the repo.
2. Place dataset.csv in the root directory.
3. Run the notebook or script to perform clustering and get recommendations.

---

Feel free to contribute or raise issues!

---

