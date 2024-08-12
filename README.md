

**Starbucks Customer Segmentation**

**1. Business Understanding**  
Starbucks, a leading global coffee company, aims to enhance customer engagement through its Rewards Program. This project focused on segmenting customers based on their interactions and demographics to optimize targeted marketing efforts, thereby increasing revenue and reducing promotional costs.

**2. Data Understanding**  
The analysis was conducted using three primary datasets:
- **Portfolio:** Metadata about the promotional offers (e.g., discounts, BOGO).
- **Profile:** Demographic information of customers (e.g., age, income, membership duration).
- **Transcript:** Records of customer transactions and interactions with offers (e.g., offers received, viewed, completed).

These datasets provided a comprehensive view of customer behaviors and preferences.

**3. Data Preparation**  
Data preprocessing involved cleaning each dataset to handle missing values and inconsistencies, followed by merging and aggregating the data. The final dataset focused on customer-offer interactions, forming the **Customer-Offer Engagement (COE)** dataset, which grouped customers based on their profiles and responses to promotional offers.

**4. Modeling & Evaluation**  
- **Feature Transformation:** Data was standardized using **PowerTransformer** to ensure a Gaussian-like distribution, crucial for effective clustering.
- **Dimensionality Reduction:** **Principal Component Analysis (PCA)** was applied to reduce data dimensionality while retaining essential variance.
- **Clustering:** **K-Means Clustering** was chosen for customer segmentation. The optimal number of clusters was identified using the **silhouette score** and **elbow method**.
  - **Silhouette Analysis** was conducted to assess cluster quality, focusing on minimizing misclassified points and ensuring uniform cluster distribution.

The final model identified distinct customer segments, although a relatively low silhouette score (0.11) indicated some cluster overlap.

**5. Discussion & Conclusion**  
The project successfully segmented Starbucks customers into actionable clusters, providing insights into different customer profiles:
- **Cluster 0:** High-value customers with quick responses to discount offers.
- **Cluster 1:** Low-income, low-spend customers with minimal offer engagement.
- **Cluster 2:** Highly engaged customers, responding well to all offer types, especially informational offers.
- **Cluster 3:** Highest spenders during non-promo periods, favoring BOGO offers.
- **Cluster 4:** Promo-period-driven spenders with a significant increase in spend during promotions.
- **Cluster 5:** Inactive customers with minimal engagement, requiring further investigation.

**Model Recommendations:**  
While the silhouette score was lower than desired, the clusters formed provided valuable insights. Future improvements could involve experimenting with alternative clustering techniques like **t-SNE** and **Gaussian Mixture Models** to enhance cluster separability and silhouette score.


