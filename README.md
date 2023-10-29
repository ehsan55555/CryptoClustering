# Cryptocurrency Clustering Analysis

## Overview
This project involves the clustering analysis of cryptocurrency market data. We aim to group cryptocurrencies based on their price change percentages over different time intervals. To achieve this, we utilize K-Means clustering with the original data and the Principal Component Analysis (PCA) data, then compare the results.


## Data
- We use cryptocurrency market data from the provided "crypto_market_data.csv" file.

- The data includes the following attributes for each cryptocurrency:
  - price_change_percentage_24h
  - price_change_percentage_7d
  - price_change_percentage_14d
  - price_change_percentage_30d
  - price_change_percentage_60d
  - price_change_percentage_200d
  - price_change_percentage_1y


## Analysis Steps

### Data Preprocessing
- Start by importing necessary libraries and loading the data into a Pandas DataFrame.
- Use StandardScaler to normalize the data.
- Perform K-Means clustering with the original data.
- Apply PCA and perform K-Means clustering with the PCA data.

### Finding the Optimal Number of Clusters
- To determine the best number of clusters (k), we create an elbow curve for both the original and PCA data.
- Select the k value with the sharpest "elbow" on the curve.

### K-Means Clustering
- Initialized the K-Means model using the optimal k value.
- Fit the model to the data and predict clusters.
- Created a scatter plot to visualize the results.


## Results
- The optimal k value for the original data is 4.
- The optimal k value for the PCA data is 2.
- Visual analysis shows that reducing the number of features using PCA improved clustering results.

