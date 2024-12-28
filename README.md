# Segmentation des clients d'un site e-commerce / E-commerce Customer Segmentation

## Contexte / Context

Le projet consiste à segmenter les clients d'un site e-commerce en utilisant des méthodes de classification non supervisées. L'objectif est de fournir une description et une segmentation des clients pour optimiser les campagnes de communication et la maintenance des segments au fil du temps.  
The project consists of segmenting customers of an e-commerce site using unsupervised classification methods. The goal is to provide a description and segmentation of customers to optimize communication campaigns and maintain the segments over time.

### Contexte et présentation des Data-Set / Context and Dataset Presentation

Olist, une entreprise brésilienne, fournit une base de données anonymisée sur l'historique des commandes, les produits achetés, les commentaires de satisfaction et la localisation des clients depuis janvier 2017.  
L'objectif est de comprendre les différents types d'utilisateurs grâce à leur comportement et à leurs données personnelles anonymisées.  
Olist, a Brazilian company, provides an anonymized database of order history, purchased products, satisfaction reviews, and customer location since January 2017. The goal is to understand different types of users based on their behavior and anonymized personal data.

## Mission / Mission

Fournir une description et une segmentation des clients actionnable pour les équipes d'e-commerce Olist.  
Proposer un contrat de maintenance basé sur une analyse de la stabilité des segments au cours du temps.  
Provide an actionable description and segmentation of customers for Olist's e-commerce teams.  
Propose a maintenance contract based on the analysis of segment stability over time.

## Présentation des tables de données / Dataset Tables Presentation

- **Customer**
- **Geolocation**
- **Order_items**
- **Order_payments**
- **Sellers**
- **Products**
- **Translation**
- **Orders**
- **Order_reviews**

## Traitement et nettoyage du Data-Set / Data Cleaning and Preprocessing

- Suppression des valeurs NaN  
- Sélection et renommage des features  
- Removal of NaN values  
- Feature selection and renaming

## Analyse exploratoire / Exploratory Analysis

- **Analyse univariée** : distribution des données quantitatives par rapport à la moyenne  
- **Analyse bivariée** : absence de corrélation entre les features, favorable pour le clustering  
- **Univariate analysis**: distribution of quantitative data against the mean  
- **Bivariate analysis**: absence of correlation between features, favorable for clustering

## Modélisation / Modeling

- **Processus de clustering** : utilisation de `np.log1p()`, normalisation avec `StandardScaler`, choix des modèles KMeans, DBScan, CAH  
- **Détermination du nombre de clusters** : méthode Elbow et score de silhouette  
- **Clustering process**: using `np.log1p()`, normalization with `StandardScaler`, choosing models like KMeans, DBScan, and Hierarchical Clustering (CAH)  
- **Determining the number of clusters**: Elbow method and silhouette score

## Modèles retenus et Stabilité / Selected Models and Stability

- **Modèle KMeans avec 5 clusters**  
- **Fréquence de mise à jour recommandée** : tous les 6 mois selon le score ARI  
- **KMeans model with 5 clusters**  
- **Recommended update frequency**: every 6 months based on ARI score

## Conclusion

- **Test de différents algorithmes** : K-Means, clustering hiérarchique agglomératif et DBSCAN  
- **Passage au Log pour certaines variables**  
- **Écartement de la segmentation RFM** en faveur de K-Means pour éviter les choix arbitraires  
- **Fréquence de mise à jour** : tous les 6 mois selon le score ARI  
- **Testing different algorithms**: K-Means, Agglomerative Hierarchical Clustering, and DBSCAN  
- **Log transformation for certain variables**  
- **Exclusion of RFM segmentation** in favor of K-Means to avoid arbitrary choices  
- **Update frequency**: every 6 months based on ARI score

## Technologies utilisées / Technologies Used

- **Python**
- **Scikit-learn**
- **Pandas**
- **Matplotlib**
- **Seaborn**
- **NumPy**
- **Jupyter Notebooks**


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
