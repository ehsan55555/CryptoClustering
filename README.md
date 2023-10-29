# Cryptocurrency Clustering Analysis

## Overview
This project focuses on clustering analysis of cryptocurrency market data. The primary objective is to group cryptocurrencies based on their price change percentages over various time intervals. The clustering is performed using K-Means on both the original data and data reduced through Principal Component Analysis (PCA), allowing for a comparison of the results.

## Repository Contents
The project repository contains the following files and folders:

- `Crypto_Clustering.ipynb`: This Jupyter Notebook is the heart of the analysis. It contains the code, detailed steps, and visualizations for the clustering of cryptocurrencies.

- `resources` folder:
  - `crypto_market_data.csv`: This CSV file, located in the "resources" folder, contains the cryptocurrency market data used for analysis. It includes attributes such as price change percentages over different time intervals.

## Data
The dataset used for this analysis is sourced from the "crypto_market_data.csv" file. Each cryptocurrency's entry includes the following attributes:

- price_change_percentage_24h
- price_change_percentage_7d
- price_change_percentage_14d
- price_change_percentage_30d
- price_change_percentage_60d
- price_change_percentage_200d
- price_change_percentage_1y

## Analysis Steps

### Data Preprocessing
- Import essential libraries and load the dataset into a Pandas DataFrame.
- Normalize the data using StandardScaler.
- Conduct K-Means clustering using the original data.
- Apply PCA and perform K-Means clustering on the PCA-transformed data.

### Determining the Optimal Number of Clusters
- To identify the most suitable number of clusters (k), create an elbow curve for both the original and PCA data.
- Select the k value corresponding to the sharpest "elbow" on the curve.

### K-Means Clustering
- Initialize the K-Means model with the optimal k value.
- Fit the model to the data and predict cluster assignments.
- Visualize the results with a scatter plot.

## Results
- The optimal k value for the original data is found to be 4.
- For the PCA data, the optimal k value is determined to be 2.
- A visual examination of the results indicates that reducing the dimensionality through PCA has improved clustering outcomes.
