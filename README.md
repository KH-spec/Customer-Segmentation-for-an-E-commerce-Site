# Customer Segmentation for an E-commerce Site

## Project Overview  
This project aims to segment customers of an e-commerce platform using unsupervised classification methods. The objective is to provide actionable insights and customer segmentation to optimize communication campaigns and maintain segment relevance over time.

---

## Context and Dataset Description  
Olist, a Brazilian company, provides an anonymized dataset with historical order data, purchased products, satisfaction reviews, and customer locations since January 2017. The goal is to understand different user types through their behaviors and anonymized personal data.

---

## Mission  
1. Provide actionable customer segmentation for Olist's e-commerce teams.  
2. Propose a maintenance plan based on the stability analysis of customer segments over time.

---

## Dataset Tables  
The dataset includes the following tables:  
- **Customer**  
- **Geolocation**  
- **Order_items**  
- **Order_payments**  
- **Sellers**  
- **Products**  
- **Translation**  
- **Orders**  
- **Order_reviews**  

---

## Data Cleaning and Preparation  
- Removal of NaN values.  
- Selection and renaming of relevant features.  

---

## Exploratory Data Analysis (EDA)  
1. **Univariate Analysis**: Distribution of quantitative data relative to the mean.  
2. **Bivariate Analysis**: No correlation between features, which is favorable for clustering.  

---

## Modeling Process  
- Clustering Process:  
  - Applied `np.log1p()` for scaling.  
  - Normalization using `StandardScaler`.  
  - Models explored: **K-Means**, **DBSCAN**, **Hierarchical Agglomerative Clustering (CAH)**.  
- Cluster count determination:  
  - Used the **Elbow Method** and **Silhouette Score**.

---

## Selected Model and Stability  
- **Chosen Model**: K-Means with 5 clusters.  
- **Update Frequency**: Recommended every 6 months based on ARI score.  

---

## Conclusion  
- Tested algorithms: **K-Means**, **Agglomerative Hierarchical Clustering**, and **DBSCAN**.  
- Applied logarithmic transformation to selected variables.  
- Opted for K-Means over RFM segmentation to avoid arbitrary choices.  
- Update frequency set to every 6 months based on ARI score.

---

## Future Improvements  
- Enhance feature selection with domain-specific insights.  
- Explore advanced clustering algorithms such as **Gaussian Mixture Models**.  
- Automate the maintenance and re-segmentation process.
