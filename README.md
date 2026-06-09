# Data Mining Project — IMDb Dataset

This repository contains the project developed for the **Data Mining: Fundamental** course, part of the **Master Programme in Data Science and Business Informatics** at the **University of Pisa**.

The project analyzes an IMDb dataset containing movies, TV shows, and other visual entertainment titles. The work includes data understanding, preprocessing, clustering, classification, regression, and pattern mining.

## Project Overview

The dataset contains **16,431 records** and **23 features** describing IMDb titles. The attributes include title type, rating, release year, runtime, awards, votes, reviews, genres, country of origin, and other metadata.

The project is divided into five main parts.

### 1. Data Understanding and Preparation

The first step focuses on exploring and cleaning the dataset.

Main operations include:

- Analysis of variable meanings and data types
- Handling of missing values
- Correction of inconsistent data types
- Conversion of rating ranges into numerical values
- Removal of constant or redundant variables
- Detection and removal of extreme noise values
- Standardization of numerical features
- Correlation analysis using Spearman correlation

### 2. Clustering

The clustering task aims to group similar IMDb titles.

The following methods were tested:

- K-Means
- DBSCAN
- Hierarchical Clustering

Two feature sets were compared:

- A full set with 12 numerical features
- A selected set with 6 more informative features

The best clustering results were obtained using **K-Means on the selected 6 features**. DBSCAN and hierarchical clustering produced less balanced and less interpretable clusters.

### 3. Classification

The classification task predicts the `titleType` of each IMDb title.

The models tested were:

- K-Nearest Neighbors
- Gaussian Naive Bayes
- Categorical Naive Bayes
- Decision Tree

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrix
- ROC curves
- Precision-recall curves

The **Decision Tree classifier** achieved the best overall performance. However, some minority classes were harder to predict because the dataset was imbalanced.

### 4. Regression

The regression task studies whether IMDb metadata can predict numerical targets such as rating-related values.

The models tested include:

- Linear Regression
- Ridge Regression
- Lasso Regression
- Decision Tree Regressor
- KNN Regressor

The results showed that the available metadata had weak predictive power for IMDb ratings. This suggests that ratings may depend on additional factors not included in the dataset.

### 5. Pattern Mining

The pattern mining task extracts frequent patterns and association rules from the dataset.

The methods used were:

- Apriori
- FP-Growth

The analysis tested different support, confidence, and lift thresholds. FP-Growth was more efficient than Apriori, especially when using lower support values.

## Repository Structure

```text
.
├── Data Understanding.ipynb
├── Clustering - 12 features.ipynb
├── Clustering - 6 features.ipynb
├── Classification.ipynb
├── Regression.ipynb
├── Regression 2.ipynb
├── Pattern Mining.ipynb
├── Project_Do_Huynh_Altangerel.pdf
└── README.md
```
