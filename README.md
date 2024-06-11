# Customer Segmentation Project
This project focuses on customer segmentation using the `marketing_campaign.csv` dataset. The objective is to identify distinct customer groups through clustering techniques, aiding in personalized marketing strategies. This project employs KMeans and Agglomerative Clustering algorithms, with feature engineering, scaling, and PCA for dimensionality reduction.

## Table of Contents
- [Dataset Overview](#dataset-overview)
- [Feature Description](#feature-description)
- [Methods and Techniques](#methods-and-techniques)
  - [Feature Engineering](#feature-engineering)
  - [Scaling](#scaling)
  - [Clustering Algorithms](#clustering-algorithms)
  - [PCA](#pca)
- [Results](#results)

## Dataset Overview
The dataset `marketing_campaign.csv` contains customer information and their responses to various marketing campaigns. This information is crucial for understanding customer behavior and segmenting them into meaningful groups. The dataset has been taken from the kaggle.

## Feature Description
Below is an overview of the features in the dataset:
- `ID`: Unique identifier for each customer.
- `Year_Birth`: The birth year of the customer.
- `Education`: The highest education level attained by the customer.
- `Marital_Status`: The marital status of the customer.
- `Income`: Annual income of the customer.
- `Kidhome`: Number of children in the customer's household.
- `Teenhome`: Number of teenagers in the customer's household.
- `Dt_Customer`: Date of enrollment with the company.
- `Recency`: Number of days since the last purchase.
- `MntWines`, `MntFruits`, `MntMeatProducts`, `MntFishProducts`, `MntSweetProducts`, `MntGoldProds`: Amount spent on various product categories in the last 2 years.
- `NumDealsPurchases`: Number of purchases made with a discount.
- `NumWebPurchases`, `NumCatalogPurchases`, `NumStorePurchases`, `NumWebVisitsMonth`: Number of purchases through different channels and visits to the company's website.
- `AcceptedCmp1`, `AcceptedCmp2`, `AcceptedCmp3`, `AcceptedCmp4`, `AcceptedCmp5`: Indicators of acceptance of the respective campaigns.
- `Complain`: Indicator if the customer has complained in the last 2 years.
- `Z_CostContact`, `Z_Revenue`: Fixed cost and revenue for contact; used for internal purposes.
- `Response`: Indicator if the customer responded to the last campaign.

## Methods and Techniques
### Feature Engineering
Feature engineering involves transforming raw data into meaningful features that better represent the underlying problem. This includes:
- Handling missing values.
- Creating new features (e.g., total children in the household).
- Encoding categorical variables.

### Scaling
Scaling is crucial to ensure that each feature contributes equally to the distance calculations in clustering algorithms. This project uses standard scaling (z-score normalization).

### Clustering Algorithms
#### KMeans Clustering
KMeans clustering partitions the data into k clusters by minimizing the variance within each cluster. It's efficient but sensitive to initial seed selection.

#### Agglomerative Clustering
Agglomerative clustering is a hierarchical method that builds nested clusters by repeatedly merging or splitting them. It doesn't require the number of clusters to be specified beforehand but can be computationally intensive.

### PCA
Principal Component Analysis (PCA) reduces the dimensionality of the data while retaining most of the variance. This improves clustering performance and interpretability by simplifying the feature space.

## Results
The project identifies several distinct customer segments, providing insights into customer behavior. These segments can be used to tailor marketing strategies, improve customer satisfaction, and increase sales.
