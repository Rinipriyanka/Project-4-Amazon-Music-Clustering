# Project-4-Amazon-Music-Clustering

# Project Overview
- Developed a Music Clustering project using **Unsupervised Machine Learning**
- The objective is to group songs based on the similar Audio Characteristics
- **K Means Clustering** is used to grouping similarities

# Objectives
- Analyzing the datasets
- Checking whether the columns contains null values
- Data Cleaning
- Finding and Dropping Duplicates
- Feature Selection for clustering
- Standardizing Selected Features
- Finding clusters for K means using Elbow Method, Silhouette Score
- Apply K Means Cluster
- Evaluating and Visualizing the cluster characteristics
- Generating Final dataset containing **Cluster Labels**

## Dataset
- Dataset contains **95,687 songs** after removing duplicate records.
- The dataset contains various song and audio-related attributes.
- Important audio features used for clustering include:
  - Danceability
  - Energy
  - Loudness
  - Speechiness
  - Acousticness
  - Instrumentalness
  - Liveness
  - Valence
  - Tempo
  - Duration

## Data Preprocessing
- Loaded the dataset using **Pandas**
- Checked the dataset shape, data types, and missing values
- Identified and removed duplicate records
- Cleaned the "genres" column
- Extracted "release_year" from "release_date"
- Selected relevant numerical audio features for clustering

## Feature Scaling
- Used **Standard Scaler** to standardize the features
- That means, standardizing larger numerical values into comparable scale such as Duration ms

## PCA
- Used **Principal Component Analysis** to reduce the features dimension for visualization
- It is mainly used to visualize features in Two Dimensions

## Clustering
- Used **K-Means Clustering** as the main clustering algorithm
- Tested different values of K using the **Elbow Method**
- Compared clustering performance using:
  - Silhouette Score
  - Davies-Bouldin Index
  - Inertia
- Selected **K = 4** for the final clustering

##  Cluster Evaluation
- **Silhouette Score:** Approximately *0.2288* for K = 4
- **Davies-Bouldin Index:** Approximately *1.5287* for K = 4

## Cluster Analysis
**Cluster 0**
- Higher acousticness
- Relatively lower energy
- Lower-to-moderate valence
- Represents songs with more acoustic and lower-energy characteristics

**Cluster 1**
- Higher energy
- Higher danceability
- Higher valence
- Higher tempo
- Lower acousticness
- Represents energetic and dance-oriented characteristics

**Cluster 2**
- Very high speechiness
- High liveness
- Lower tempo
- Shorter average duration
- Represents speech-heavy or spoken-content characteristics

**Cluster 3**
- Very high instrumentalness
- Higher acousticness
- Relatively lower energy
- Represents highly instrumental characteristics

## Visualizations
- Elbow Method plot
- PCA cluster scatter plot
- Cluster feature comparison bar chart
- Cluster heatmap
- Feature distribution plots

## Applications
The resulting clusters can be used as a foundation for:
- Similar-song recommendation
- Playlist generation
- Music categorization
- Grouping songs based on audio characteristics
