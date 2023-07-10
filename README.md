# CryptoClustering

# Cryptocurrency Clustering Analysis

This repository contains code for performing cryptocurrency clustering analysis using K-means and Principal Component Analysis (PCA). The analysis aims to group cryptocurrencies based on their price change percentage over different time intervals.

## Getting Started

To get started with the code, follow these steps:

1. Install the required libraries and dependencies:
   - pandas
   - hvplot.pandas
   - scikit-learn

2. Load the cryptocurrency market data into a Pandas DataFrame. The data should be in CSV format and contain the following columns:
   - coin_id: Identifier for each cryptocurrency
   - price_change_percentage_24h: Price change percentage in the last 24 hours
   - price_change_percentage_7d: Price change percentage in the last 7 days
   - price_change_percentage_14d: Price change percentage in the last 14 days
   - price_change_percentage_30d: Price change percentage in the last 30 days
   - price_change_percentage_60d: Price change percentage in the last 60 days
   - price_change_percentage_200d: Price change percentage in the last 200 days
   - price_change_percentage_1y: Price change percentage in the last 1 year

3. Normalize the data using the StandardScaler module from scikit-learn. This step ensures that all the features are on a similar scale.

4. Perform exploratory data analysis (EDA) to understand the data. This includes generating summary statistics and visualizing the data using line plots.

## Original Data Analysis

### Clustering with K-means

- Initialize the K-means model using the desired number of clusters.
- Fit the K-means model using the scaled data.
- Predict the clusters for the cryptocurrencies.
- Add a new column to the DataFrame with the predicted clusters.
- Visualize the clusters using a scatter plot, where the x-axis represents the price change percentage in the last 24 hours, the y-axis represents the price change percentage in the last 7 days, and the color represents the clusters. The hover feature displays the cryptocurrency name.

### Optimize Clusters with PCA

- Create a PCA model instance and set the number of components to 3.
- Use the PCA model to transform the scaled data into three principal components.
- Create a DataFrame with the PCA data.
- Perform exploratory analysis on the transformed data.
- Determine the explained variance ratio of each principal component.
- Find the optimal number of clusters using the elbow method and plot the elbow curve.
- Cluster the transformed data using K-means with the optimal number of clusters.
- Visualize the clusters using a scatter plot, where the x-axis represents the first principal component, the y-axis represents the second principal component, and the color represents the clusters. The hover feature displays the cryptocurrency name.

## Visualize and Compare the Results

- Create composite plots to contrast the elbow curves and clusters obtained from the original data and PCA data. The composite plots provide a visual comparison of the clustering results.

## Conclusion

The cryptocurrency clustering analysis provides insights into grouping cryptocurrencies based on their price change percentage over different time intervals. By using K-means and PCA, we can identify clusters and understand the relationships between cryptocurrencies based on their price performance. The analysis helps in visualizing and comparing the clustering results obtained from the original data and reduced-dimensional PCA data.

