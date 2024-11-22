# Song Recommendation System
This project is a Song Recommendation System that suggests songs based on user input, leveraging a combination of clustering algorithms and fuzzy matching for personalized recommendations. It categorizes songs into clusters using audio features and provides recommendations from the same cluster or highlights popular "hot" songs.

Features
Hot Song Detection: Determines if a user-provided song is in the current hot songs list.
Fuzzy Matching: Suggests similar songs if the input does not perfectly match a known song.
Cluster-Based Recommendations: Uses audio features and KMeans clustering to suggest songs from the same cluster.
Audio Feature Analysis: Extracts features like danceability, energy, valence, and tempo to group similar songs.
How It Works
User Input: The user inputs the name of a song.
Hot Song Check:
If the song is in the hot list, another hot song is recommended.
If not, the system uses audio features for further recommendations.
Audio Feature Retrieval:
Extracts song features from Spotify's API.
Features are clustered using KMeans Unsupervised Learning.
Cluster-Based Recommendation:
The system recommends a song from the same cluster as the input song.
Fallbacks:
If the input song is not found, fuzzy matching suggests a similar song.
Provides "hot" songs as a backup recommendation.
Architecture
Data Collection
Web Scraping: Gathers a list of current hot songs.
API Integration: Collects audio features for songs using Spotify's API.
Clustering
Audio features of songs are processed and grouped using KMeans clustering into multiple clusters. These clusters enable similarity-based recommendations.
Recommendation Flow
Hot Song Recommendation:
If the song is "hot," a random song from the hot list is recommended.
Cluster-Based Recommendation:
If the song is not hot, the system recommends a song from the same cluster.
Fuzzy Matching:
If the song is not recognized, a similar song is suggested using string matching algorithms.
Technologies Used
Python: Main programming language.
Spotify API: For fetching song metadata and audio features.
Scikit-learn: For KMeans clustering and feature scaling.
FuzzyWuzzy: For fuzzy matching of song titles.
Web Scraping: To gather the list of popular songs.
