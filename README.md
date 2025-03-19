# Business Understanding
Music streaming platforms offer vast libraries, making it challenging for users to discover new songs aligned with their tastes. This project aims to create a personalized recommendation system that blends familiar favorites with new discoveries, helping users curate playlists tailored to their listening habits. The system clusters songs based on their audio characteristics, allowing for better organization and improved music recommendations.

# Data Understanding
The dataset used in this project comes from two sources:
1. Kaggle - Spotify 12M Songs Dataset: A comprehensive collection of songs with audio features like danceability, energy, tempo, and valence.
2. Spotify API - User Top Tracks: A dataset of the user’s top 2000 songs, extracted via the Spotify API. An additional column was added to the Kaggle dataset to indicate whether a song appears in the user’s top tracks.

## Feature Selection
The features included were chosen based on their relevance to audio perception and mood classification. Key attributes include:
* Danceability, Energy, and Valence: To assess the overall feel of a song.
* Tempo and Loudness: To capture intensity and dynamics.
* Speechiness and Instrumentalness: To distinguish between lyrical and instrumental music.

## Data Preparation
1. Merged the Kaggle dataset with the user's top tracks from Spotify.
2. Dropped unnecessary columns such as track number, disc number, and release year.
3. Scaled numerical features to standardize data for clustering.
4. Handled missing values and outliers to improve model performance.

# Exploratory Data Analysis
* Analyzed distributions of key audio features across the dataset.
* Visualized clusters to understand how songs are grouped based on characteristics.
* Examined correlations between features to determine their influence on clustering.

# Modeling and Evaluation
* Applied K-Means, Agglomerative Clustering, and Gaussian Mixture Models (GMM) to segment songs.
* Used Silhouette Score and Cosine Similarity to assess clustering quality.
* Reduced dimensionality with PCA to improve cluster separation and visualization.

# Conclusion
The project successfully grouped songs into distinct clusters, allowing users to receive personalized playlist recommendations. By leveraging audio features and clustering techniques, the system provides a structured way to explore new music while preserving individual listening preferences.

## Limitations
1. The model does not incorporate collaborative filtering, limiting recommendations to content-based approaches.
2. Cluster labels are not predefined, requiring interpretation based on feature analysis.
3. Songs from underrepresented genres may not cluster effectively.

## Recommendations
1. Introduce a rating system to refine song recommendations based on user feedback.
2. Incorporate collaborative filtering to enhance recommendations with social listening patterns.
3. Fine-tune clustering parameters to improve accuracy in capturing user preferences.
4. Experiment with hybrid models combining content-based and collaborative filtering approaches.