# Clustering-Based Approach as an Alternative to Industry Classification

This project aims to develop a dynamic, data-driven alternative to the traditional Global Industry Classification Standard (GICS) by applying clustering techniques to stock data. By analyzing 20 years of historical daily return data from S&P 500 companies, this project captures evolving economic relationships that static systems like GICS may overlook. Through a combination of correlation matrices and feature engineering, the proposed model provides deeper insights into company behavior, market trends, and sector shifts over time.

## Project Objectives

- **Develop a Data-Driven Classification System:** Create a meaningful classification of companies that captures dynamic economic relationships compared to the static GICS system.
- **Provide Insights Over Time:** Analyze how company groupings change during different economic conditions (e.g., financial crises, pandemics).
- **Investment Strategy Applications:** Identify long-term trends, sector-specific behaviors, and potential opportunities for diversified investment strategies.

## Methodology

Three clustering approaches were tested:
1. **Correlation Matrix Approach:** Companies were clustered based on their daily return correlation matrix.
   
   ![K-Means Clustering - Correlation Matrix Approach](<Images/KMeans(Correlation Matrix).png>)

   *Insight:* The clustering based on the correlation matrix generated a relatively small number of clusters (n=3), indicating that companies tend to have high correlations with each other. This approach is limited in capturing more nuanced differences, as it resulted in oversimplified clusters where companies across multiple GICS sectors were grouped together.

2. **Feature Engineering Approach:** Engineered features (e.g., average return, volatility) were extracted for distinct economic phases such as pre-financial crisis, COVID-19, etc.
   
   ![K-Means Clustering - Feature Engineering Approach](<link_to_image>)

   *Insight:* Using 10 engineered features, the clustering yielded smaller cluster sizes (n=2). This approach captured general trends but lacked the detail needed to differentiate between companies with similar volatilities across economic periods.

3. **Combined Approach:** Both correlation matrix and engineered features were used as inputs, followed by Principal Component Analysis (PCA) for dimensionality reduction.
   
   ![K-Means Clustering - Combined Approach](<link_to_image>)

   *Insight:* The combined approach produced 13 clusters, striking a balance between detail and interpretability. This method was able to differentiate companies more effectively by leveraging both the correlation matrix and engineered features, revealing patterns missed by the first two approaches.

## Cluster Analysis

### Inter and Intra-Cluster Correlations

   ![Inter and Intra-Cluster Correlation Matrix](<link_to_image>)

   *Insight:* The heatmap of inter-cluster correlations shows that most clusters are well-separated, with low correlation values between them. Clusters like Cluster 1 and Cluster 9 have low correlations with most others, making them ideal candidates for portfolio diversification. Intra-cluster correlations (on the diagonal) reveal the internal cohesion of clusters. For instance, Cluster 11 has a high intra-cluster correlation, suggesting that companies within this cluster behave similarly, while Cluster 1 shows more independent behavior among its companies.

### Amazon’s Cluster Membership Over Time

   ![Amazon Distance to Clusters](<link_to_image>)

   *Insight:* Amazon's distance to different clusters over time shows how its market position evolved. Initially close to Consumer Cyclical companies, Amazon later became more aligned with technology sectors, reflecting its growing influence in cloud computing. Over time, its distance to other sectors, such as Healthcare and Industrials, fluctuated, providing a dynamic view of its business diversification not captured by static classifications like GICS.

## Results

- **Volatility and Return Analysis:** Each cluster's mean daily return and volatility were analyzed, providing insights into potential investment strategies (e.g., risk-tolerant vs. risk-averse portfolios).
- **Inter-Cluster Correlation:** Low correlation values between clusters indicate well-separated groups, offering opportunities for diversified investments.
  
## Future Work

- **Backtesting:** Applying the clustering method in real-world portfolio management and comparing results to GICS-based strategies.
- **Feature Engineering Enhancements:** Utilizing advanced techniques (e.g., deep learning) to capture non-linear relationships and temporal dependencies.
- **Expanded Data Sources:** Incorporating additional data such as social media sentiment for more precise company classification.

## Limitations
- Focused only on publicly traded companies.
- Potential survivorship bias due to the exclusion of companies without complete data.
- Linear relationships assumed through correlation matrices, potentially missing non-linear dynamics.

## Conclusion
This project demonstrates the potential for using clustering techniques to provide a more nuanced, dynamic view of company classifications. Compared to GICS, clustering can offer better insights into changing market behaviors and relationships, making it a valuable tool for investment analysis and portfolio diversification.

## References
[List of references included in the project report]
