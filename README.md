# CryptoClustering Project

Welcome to my CryptoClustering project! In this project, I applied the K-means algorithm and Principal Component Analysis (PCA) to classify cryptocurrencies based on their price fluctuations over various timeframes. This README provides an overview of the steps I took to complete the project and the insights I gained.

## Project Overview

The goal of this project was to classify cryptocurrencies according to their price changes over different intervals: 24 hours, 7 days, 30 days, 60 days, 200 days, and 1 year. By leveraging K-means clustering and PCA, I aimed to uncover patterns and group similar cryptocurrencies together.

## Steps Taken

### Initial Setup

- **Repository Creation**: I created a new GitHub repository named `CryptoClustering` to host this project. This ensured a clean and organized workspace for my work.

- **File Renaming**: I renamed the starter code file from `Crypto_Clustering_starter_code.ipynb` to `Crypto_Clustering.ipynb` to reflect the final version of my work.

### Data Preparation

- **Data Loading**: I loaded the `crypto_market_data.csv` file into a DataFrame and set the index to the `coin_id` column. This allowed me to work with the data efficiently.

- **Data Normalization**: Using the `StandardScaler()` module from scikit-learn, I normalized the data to ensure that all features contributed equally to the analysis.

### Finding the Best Value for k

- **Elbow Method**: I implemented the elbow method to determine the optimal number of clusters (k) for the K-means algorithm. By plotting the inertia values for k ranging from 1 to 11, I visually identified the best k value.

### Clustering with K-Means

- **Model Initialization and Fitting**: I initialized the K-means model with the best k value and fitted it using the scaled data. This allowed me to predict clusters and group cryptocurrencies accordingly.

- **Visualization**: I created a scatter plot to visualize the clusters, setting the x-axis as `price_change_percentage_24h` and the y-axis as `price_change_percentage_7d`.

### Optimizing Clusters with PCA

- **PCA Implementation**: I performed PCA on the scaled data to reduce the features to three principal components. This step helped in simplifying the dataset while retaining essential information.

- **Explained Variance**: I calculated the explained variance to understand how much information each principal component captured.

### Clustering with PCA Data

- **Elbow Method on PCA Data**: I repeated the elbow method using the PCA data to find the best k value for clustering.

- **Model Initialization and Fitting**: Using the best k value, I initialized and fitted the K-means model with the PCA data, predicting clusters for the cryptocurrencies.

- **Visualization**: I created a scatter plot with `PC1` on the x-axis and `PC2` on the y-axis to visualize the clusters formed using PCA data.

### Feature Weights Analysis

- **Feature Weights DataFrame**: I created a DataFrame to show the weights of each feature for each principal component. This analysis helped identify which features had the strongest influence on each component.

## Insights and Conclusions

- **Optimal k Value**: Through the elbow method, I determined the best k value for clustering both the original and PCA data.

- **Impact of PCA**: Using PCA reduced the complexity of the dataset, making it easier to visualize and interpret the clusters.

- **Feature Influence**: The feature weights analysis revealed which features had the most significant impact on the principal components, providing insights into the underlying patterns in the data.

## Deployment and Submission

- **GitHub Repository**: I have submitted the project files to my GitHub repository, ensuring that all changes are well-documented with appropriate commit messages.

## Code Comments

- **Documentation**: The code is well-commented with concise and relevant notes, making it easy for other developers to understand my approach and findings.

Thank you for reviewing my CryptoClustering project! If you have any questions or feedback, feel free to reach out.

