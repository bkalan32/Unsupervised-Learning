# Unsupervised-Learning

In this project, we aim to assemble investment portfolios based on cryptocurrencies using unsupervised learning techniques. We use the K-means algorithm to cluster the cryptocurrencies according to their performance in different time periods. We also use Principal Component Analysis (PCA) to reduce the features to three principal components.

### Files
The following files are provided for this project:

crypto_data.csv: contains the price change data of cryptocurrencies in different periods.
### Tasks
The project tasks are divided into the following sections:

### Import the Data
Import the crypto_data.csv file and prepare the data for clustering.

### Find the Best Value for k Using the Original Data
Use the elbow method to find the best value for k. Code the elbow method algorithm to find the best value for k using a range from 1 to 11. Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.

### Cluster Cryptocurrencies with K-means Using the Original Data
Initialize the K-means model with four clusters by using the best value for k. Fit the K-means model using the original data. Predict the clusters to group the cryptocurrencies using the original data. Create a copy of the original data and add a new column with the predicted clusters. Using hvPlot, create a scatter plot by setting x="price_change_percentage_24h" and y="price_change_percentage_7d". Color the graph points with the labels found using K-means. Then, add the crypto name in the hover_cols parameter to identify the cryptocurrency represented by each data point.

### Optimize Clusters with Principal Component Analysis
Perform a principal component analysis (PCA) and reduce the features to three principal components. Create a PCA model instance and set n_components=3. Use the PCA model to reduce to three principal components. Retrieve the explained variance to determine how much information can be attributed to each principal component. Create a new DataFrame with the PCA data. Be sure to set the coin_id index from the original DataFrame as the index for the new DataFrame.

### Find the Best Value for k Using the PCA Data
Use the elbow method to find the best value for k by using the PCA data. Code the elbow method algorithm and use the PCA data to find the best value for k using a range from 1 to 11. Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.

### Cluster Cryptocurrencies with K-means Using the PCA Data
Initialize the K-means model with four clusters by using the best value for k. Fit the K-means model by using the PCA data. Predict the clusters to group the cryptocurrencies by using the PCA data. Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters. Using hvPlot, create a scatter plot by setting x="PC1" and y="PC2". Color the graph points with the labels found using K-means. Then, add the crypto name in the hover_cols parameter to identify the cryptocurrency represented by each data point.

### Visualize and Compare the Results
Create a composite plot using hvPlot and the plus (+) operator to compare the elbow curve that you created to find the best value for k with the original data and the PCA data. Create a composite plot using hvPlot and the plus (+) operator to compare the cryptocurrencies clusters using the original data and the PCA data.
