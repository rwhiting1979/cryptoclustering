# Cryptocurrency Market Analysis

## Project Overview

This project involves a comprehensive analysis of the cryptocurrency market using machine learning techniques. The objective is to cluster cryptocurrencies based on market data to identify patterns and group similar cryptocurrencies together. The analysis employs K-Means clustering and Principal Component Analysis (PCA) to reduce dimensionality and improve clustering performance.

## Data Source

The data for this project consists of various cryptocurrency market metrics, such as price change percentages over different time frames. The dataset is sourced from a CSV file containing historical market data.

### Data Preprocessing

- Loaded the market data into a Pandas DataFrame.
- Generated summary statistics to understand the data distribution.
- Normalized the data using `StandardScaler` from scikit-learn to ensure equal weighting during the clustering process.

### K-Means Clustering

- Determined the optimal number of clusters by plotting an Elbow curve and identifying the "elbow" point.
- Initialized the K-Means model using the optimal cluster value.
- Fitted the model to the normalized market data and predicted the cluster labels.
- Visualized the clustering results using a scatter plot, mapping 'price_change_percentage_24h' against 'price_change_percentage_7d'.

### Principal Component Analysis (PCA)

- Applied PCA to reduce the feature set to three principal components.
- Calculated the explained variance to quantify the information retained after dimensionality reduction.
- Performed K-Means clustering on the PCA-transformed data.
- Visualized the PCA-based clusters and compared them with the original feature-based clusters.

## Results

The analysis revealed that PCA can enhance clustering by focusing on the main components that capture the most variance within the data. The PCA-based clusters showed clearer separation, suggesting that the reduced number of features retained the essential information for clustering while discarding noise and less relevant details.

## Visualizations

Two scatter plots were provided to contrast the clustering results:
- The first plot showed the clusters based on the original features.
- The second plot showed the clusters after applying PCA.

## Conclusion

This project underscores the importance of preprocessing techniques like scaling and dimensionality reduction in machine learning workflows. The use of PCA, in conjunction with K-Means clustering, can lead to improved clustering performance and provide insightful data groupings that might not be as apparent in higher-dimensional spaces.
