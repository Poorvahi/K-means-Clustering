# K-means-Clustering 
https://colab.research.google.com/drive/1w8YHMvjIuTnViL41v0LTiPoNGTjfMvDj?usp=sharing#scrollTo=2bpX3z1T90Kd

Online Store Customer Segmentation (K-Means Clustering) :We identified 4 distinct customer groups that businesses can target with different marketing strategies (loyalty rewards, win-back campaigns, etc.), helping improve retention and revenue.
Steps Performed:
1. Feature Selection
We selected meaningful features from the cleaned dataset:
   1.Recency → Days since last purchase
   2.Frequency → Number of unique purchase invoices
   3.Monetary → Total spending by customer
   4.Total Quantity → Total items purchased
   5.Avg Basket Size → Average number of items per invoice
   6.Avg Item Price → Average spend per item
These capture both purchase behavior (frequency, quantity) and value behavior (monetary, price sensitivity).

2. Data Preparation
  1.Converted dates & created reference date for Recency.
  2.Handled missing/infinite values.
  3.Applied StandardScaler to normalize features.
  4.Visualized data distribution before and after scaling.

3. Choosing Number of Clusters (k)

We tested k = 2 to 10 using:
-> Elbow Method → Checked WCSS (inertia).
-> Silhouette Score → Evaluated cluster separation.
   Chose k = 4 as the best balance.

4. Modelling with K-Means
  1.Applied K-Means clustering with 4 clusters.
  2.Assigned each customer to a segment.
  3.Validated with PCA (2D visualization).

5. Cluster Profiles
Based on averages of Recency, Frequency, Monetary, etc., we identified:
  Cluster 0 → Loyal Customers (low Recency, high Frequency & Monetary)
  Cluster 1 → At Risk (high Recency, low Frequency & Monetary)
  Cluster 2 → Best Customers (very high Frequency & Monetary)
  Cluster 3 → Lost Customers (inactive for a long time)

6. Visualizations
  - Histograms & Boxplots of features.
  - Correlation Heatmap of scaled features.
  - PCA Scatter Plot showing clusters in 2D.

Conclusion:
  We successfully segmented customers into 4 groups:
  Best Customers – High spenders, most valuable.
  Loyal Customers – Consistent buyers.
  At Risk – Declining engagement.
  Lost Customers – Inactive, need win-back campaigns.
These insights can help businesses tailor personalized marketing strategies and improve customer retention.
