

---

## Instructions

### 1. Data Preparation

- **Normalize the Data:**
  - Use the `StandardScaler()` module from scikit-learn to normalize the data from the provided CSV file.
  - Create a new DataFrame with the scaled data, and set the `"coin_id"` index from the original DataFrame as the index for this new DataFrame.

### 2. Determine the Optimal k Value Using the Elbow Method

- **Find the Best Value for k:**
  - Create a list of k values ranging from 1 to 11.
  - Initialize an empty list to store the inertia values for each k.
  - Use a for loop to compute and store the inertia for each value of k.
  - Create a dictionary with the k values and corresponding inertia values to plot the elbow curve.
  - Plot a line chart to visualize the inertia values and identify the optimal value for k.
  - Answer the following question: *What is the best value for k?*

### 3. Cluster Cryptocurrencies Using K-means with the Original Scaled Data

- **Cluster the Data:**
  - Initialize the K-means model using the best k value identified.
  - Fit the K-means model on the original scaled DataFrame.
  - Predict the clusters for the cryptocurrencies using the original scaled data.
  - Create a copy of the original DataFrame and add a new column to store the predicted cluster labels.
  - **Visualize the Clusters:**
    - Create a scatter plot using hvPlot.
    - Set the x-axis to `"PC1"` and the y-axis to `"PC2"`.
    - Color the points based on the predicted clusters.
    - Use the `"coin_id"` column in the `hover_cols` parameter to identify each cryptocurrency.

### 4. Optimize Clusters with Principal Component Analysis (PCA)

- **Perform PCA:**
  - Apply PCA on the original scaled DataFrame to reduce the features to three principal components.
  - Retrieve and analyze the explained variance to understand how much information each principal component contributes.
  - Answer the following question: *What is the total explained variance of the three principal components?*
  - Create a new DataFrame using the PCA data, setting the `"coin_id"` index from the original DataFrame as the index.

### 5. Determine the Optimal k Value Using the PCA Data

- **Elbow Method for PCA Data:**
  - Create a list of k values ranging from 1 to 11.
  - Initialize an empty list to store the inertia values for each k.
  - Use a for loop to compute and store the inertia for each k value.
  - Create a dictionary with the k values and corresponding inertia values to plot the elbow curve.
  - Plot a line chart to visualize the inertia values and identify the optimal value for k.
  - Answer the following question: *What is the best value for k when using the PCA data? How does it compare to the best k value found using the original data?*

### 6. Cluster Cryptocurrencies Using K-means with the PCA Data

- **Cluster the PCA Data:**
  - Initialize the K-means model using the best k value identified from the PCA data.
  - Fit the K-means model on the PCA data.
  - Predict the clusters for the cryptocurrencies using the PCA data.
  - Create a copy of the PCA DataFrame and add a new column to store the predicted cluster labels.
 

