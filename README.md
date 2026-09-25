# 🇲🇾 Malaysia Tourism Analytics — DOSM Datathon 2026

An interactive tourism analytics project developed for **DOSM Datathon 2026**, combining **Power BI** visualisation with **Python and K-Means Clustering** to uncover tourism patterns across Malaysian states.

## 📌 Project Overview

This project analyses Malaysian tourism data to understand tourism trends, visitor flows, market dependency, diversification, and similarities between states.

The project combines **Exploratory Data Analysis (EDA)** with **Machine Learning** to transform tourism statistics into meaningful and actionable insights.

## 🎯 Objectives

- Analyse tourism trends across Malaysian states
- Explore origin-to-destination tourism flows
- Measure local tourism dependency and market diversification
- Identify tourism market structures
- Group states with similar tourism characteristics using K-Means Clustering
- Develop an interactive Power BI dashboard for data-driven decision making

## 🛠️ Tools & Technologies

- Power BI
- Python
- Google Colab
- Pandas
- Scikit-learn
- Matplotlib
- K-Means Clustering

## 📊 Exploratory Data Analysis

The Power BI dashboard explores tourism performance through:

- State Trend Analysis
- Tourism Flow Analysis
- Local Dependency
- Market Diversification
- Market Structure Analysis

### Tourism Overview Dashboard

![Tourism Overview Dashboard](images/Tourism%20Overview%20Dashboard.png)

### Tourism Flow & Market Structure Dashboard

![Tourism Flow and Market Structure Dashboard](images/Tourism%20Flow%20%26%20Market%20Structure%20Dashboard.png)

## 🤖 Machine Learning — K-Means Clustering

### Why K-Means?

While Power BI helps visualise tourism patterns, K-Means clustering was used to identify groups of Malaysian states with similar tourism characteristics automatically.

K-Means is an **unsupervised machine learning algorithm**, making it suitable for this project because the dataset does not contain predefined cluster labels.

### Machine Learning Workflow

1. Data preparation
2. Feature selection
3. Feature scaling
4. Evaluation of different K values
5. Elbow Method and Silhouette Score analysis
6. K-Means clustering
7. PCA visualisation
8. Integration of cluster results into Power BI

### 📉 Selecting the Number of Clusters — Elbow Method

To determine an appropriate number of clusters, K-Means was tested using **K = 2 to K = 6**.

![Elbow Method](images/elbow-method.png)

The inertia values decreased as the number of clusters increased:

| K | Inertia | Silhouette Score |
|---|---:|---:|
| 2 | 51.69 | 0.451 |
| 3 | 34.21 | 0.367 |
| 4 | 24.96 | 0.366 |
| 5 | 19.76 | 0.223 |
| 6 | 13.73 | 0.204 |

The largest reduction in inertia occurred between **K = 2 and K = 3**, after which the improvements became more gradual.

Although **K = 2 produced the highest Silhouette Score**, **K = 3** was selected as a practical balance between the Elbow Method and obtaining a more informative segmentation of tourism market structures.

### 🧩 K-Means Clustering Result

The final model was therefore developed using **three clusters**.

![K-Means Clustering Result](images/kmeans-clustering-result.png)

For visualisation, **Principal Component Analysis (PCA)** was used to reduce the clustering features into two dimensions.

The PCA plot allows the cluster structure to be visualised while the K-Means model itself groups states according to the selected tourism characteristics.

The resulting cluster labels were subsequently integrated into the Power BI dashboard to support interactive analysis and comparison between states.

### 📓 Notebook

The complete Python implementation, including data preprocessing, feature scaling, Elbow Method, Silhouette Score evaluation, K-Means clustering and PCA visualisation, is available here:

➡️ [View K-Means Clustering Notebook](notebooks/tourism-kmeans-clustering.ipynb)

## 📈 Power BI Dashboard

The final dashboard integrates exploratory analysis and machine-learning results to provide an interactive view of Malaysia's tourism landscape.

*Final dashboard screenshot will be added here.*

## 👥 Team

Developed for **DOSM Datathon 2026** by:

- Balqish
- Deeja
- Nadh
- Puti

## 👩‍💻 My Contribution

My contributions to the project include:

- Exploratory Data Analysis
- Power BI dashboard development
- Tourism indicator visualisation
- K-Means clustering implementation and analysis
- Integration of machine-learning results into Power BI

## 📁 Repository Structure

```text
├── data/
├── images/
├── notebooks/
├── powerbi/
├── report/
└── README.md
