**Customer Segmentation Using RFM and K-Means Clustering**
**Project Overview**
This project performs customer segmentation for sales data using RFM analysis and K-Means clustering. RFM analysis categorizes customers based on their Recency, Frequency, and Monetary behavior, and K-Means clustering is then used to segment the customers into groups based on these RFM scores.

Approach 1:
RFM Scores Assignment: First, assign RFM scores based on quantiles.
K-Means Clustering: Use the RFM scores as features for customer segmentation via K-Means.

**Steps Involved**
1. Data Preprocessing
  Load Sales Data: The sales data is loaded from a CSV file.
  Data Cleaning: Unnecessary columns are dropped, and column data types are corrected (e.g., converting ORDERDATE to a datetime type).
  Feature Engineering: The PRODUCTCODE is used to create a new feature PRODUCTINITIAL containing the first 3 characters of the product code.

2. RFM Analysis
  Recency (R): Days since the customer’s last order.
  Frequency (F): Number of orders placed by the customer.
  Monetary (M): Total sales value of each customer.

**Scoring:** RFM scores are calculated by dividing each RFM metric into quartiles and assigning scores (1 to 4) for Recency (lower scores represent more recent), and (1 to 4) for Frequency and Monetary (higher scores represent more frequent or more valuable).

3. K-Means Clustering
  Features Used for Clustering: Recency, Frequency, and Monetary scores.
  Optimal Number of Clusters: The model uses the Elbow Method to find the optimal number of clusters.
  Clustering: Customers are segmented into 4 distinct clusters using K-Means clustering.

4. Visualization
3D Scatter Plot: A 3D scatter plot is created to visualize the customer segments using their RFM scores (Recency, Frequency, and Monetary).
Cluster Distribution: The distribution of customers across each segment (cluster) is visualized and analyzed.

**Dependencies**
This project requires the following Python libraries:
pandas: For data manipulation and analysis.
numpy: For numerical computations.
matplotlib: For data visualization.
seaborn: For statistical data visualization.
plotly: For interactive visualizations.
sklearn: For K-Means clustering.
datetime: For working with dates and times.

**Dataset Link**   https://www.kaggle.com/kyanyoga/sample-sales-data.
