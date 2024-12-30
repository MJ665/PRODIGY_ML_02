
---

# Prodigy Internship Task 2: Customer Segmentation with K-Means Clustering

## Task Overview
Create a K-means clustering algorithm to group customers of a retail store based on their purchase history.

---

## Steps and Code Details

### 1. **Importing Necessary Libraries**
The script uses the following libraries:
- `pandas` and `numpy`: For data handling and manipulation.
- `matplotlib.pyplot` and `seaborn`: For creating visualizations.
- `sklearn`: For clustering, scaling, PCA, and evaluation metrics.

### 2. **Loading the Dataset**
The dataset (`Mall_Customers.csv`) is loaded using `pandas`. Ensure the correct path is set in the code.

### 3. **Preprocessing**
- **Encoding Categorical Data**: The `Gender` column is encoded into numeric values (`Male=1`, `Female=0`).
- **Feature Selection**: Relevant features (`Age`, `Annual Income (k$)`, and `Spending Score (1-100)`) are used for clustering.
- **Scaling Features**: StandardScaler is used to normalize the features.

### 4. **Principal Component Analysis (PCA)**
PCA reduces the dimensionality to 2 components, aiding visualization while retaining essential data characteristics.

### 5. **Determining Optimal Clusters**
- The **Elbow Method** is employed to identify the optimal number of clusters.
- Inertia values are plotted for a range of cluster counts (`K=1 to K=10`).

### 6. **Clustering with K-Means**
- The optimal number of clusters (`K=5`) is used for clustering.
- Cluster labels are assigned to each data point.

### 7. **Evaluation**
- **Silhouette Score**: Measures the quality of clustering.
- **Cluster Characteristics**: Averages of features within each cluster provide insights.
- **Classification Metrics**:
  - Assuming pseudo-labels (or true labels if available) to evaluate clustering as a classification task.
  - Generates a confusion matrix and a classification report.

### 8. **Visualizations**
- **Elbow Curve**: Displays inertia for different cluster counts.
- **PCA-Based Scatterplot**: Visualizes clusters in reduced dimensions.
- **Confusion Matrix**: Highlights clustering performance (pseudo-label evaluation).
- **Cluster Centroids**: Shows data points and centroids in PCA space.

---

## Requirements

### Dependencies
Install the necessary Python libraries:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### Dataset
Ensure the `Mall_Customers.csv` dataset is placed in the correct directory or update the file path in the script.

---

## Running the Code
1. Place the script and dataset (`Mall_Customers.csv`) in the same directory or specify the correct file path.
2. Execute the script:
   ```bash
   python clustering_script.py
   ```
3. View the visualizations and metrics in the output.

---

## Results
- **Optimal Clusters**: Identified using the Elbow Method.
- **Silhouette Score**: Quantitative measure of clustering quality.
- **Cluster Characteristics**: Insights into customer groups.
- **Visualizations**:
  - PCA scatter plots of clusters.
  - Confusion matrix heatmap.

---

## Notes
- Replace pseudo-labels with true labels in `true_labels` if available for better evaluation.
- Adjust the `optimal_k` variable if the Elbow Curve suggests a different value.
- PCA is optional and primarily for visualization.

--- 
