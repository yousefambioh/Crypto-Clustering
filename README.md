# Crypto-Clustering
Using Python and unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes
![image](https://github.com/user-attachments/assets/e5a2c1da-908b-486d-bc7b-e9798f376368)


📈 Cryptocurrency Clustering Analysis
🧠 Overview
This project applies unsupervised machine learning techniques to identify patterns in cryptocurrency data. By analyzing how cryptocurrencies respond to 24-hour and 7-day price changes, we aim to uncover meaningful groupings using K-Means clustering—both on the original feature set and on features reduced with Principal Component Analysis (PCA).

📁 Data Source
Data is located in the Resources folder:

crypto_market_data.csv

🔍 Key Findings
🧮 Elbow Curve Analysis
Original Data (elbow1): Higher inertia values, suggesting less compact clusters.

PCA Data (elbow2): Lower inertia values, indicating tighter, more efficient clustering.

🧊 Cluster Visualization
Original Data Clustering: Overlapping clusters with poor separation.

PCA-Based Clustering: Well-defined, distinct clusters—4 groups clearly identified.

✅ Conclusion
Using PCA to reduce the number of features before clustering improved the results significantly. It reduced noise, highlighted key patterns, and led to more meaningful clusters. In short: fewer features, better clusters.

📘 Project Steps
1. Data Preparation
Normalize the data using StandardScaler.

Create a scaled DataFrame and set coin_id as the index.

2. Determine Optimal k (Original Data)
Use the Elbow Method on scaled data to find the optimal number of clusters.

Plot inertia vs. k to identify the "elbow point."

3. Cluster with K-Means (Original Data)
Train a KMeans model using the best k.

Predict and label clusters.

Visualize the results using hvPlot with principal components as axes.

4. Dimensionality Reduction with PCA
Apply PCA to reduce features to 3 principal components.

Calculate explained variance to assess retained information.

Create a PCA-transformed DataFrame indexed by coin_id.

5. Determine Optimal k (PCA Data)
Repeat the Elbow Method using the PCA-transformed data.

Compare the optimal k with that from the original dataset.

6. Cluster with K-Means (PCA Data)
Cluster the PCA-transformed data using KMeans.

Predict cluster labels and visualize results using hvPlot, this time with 24h and 7d price change on the axes.

📝 Summary
This project clusters cryptocurrencies based on their short-term price fluctuations using K-Means, both on original and PCA-reduced data. PCA improved clustering quality by eliminating noise and enhancing the separation between clusters. Visual and inertia-based analysis confirm PCA's effectiveness in producing better-defined clusters.
