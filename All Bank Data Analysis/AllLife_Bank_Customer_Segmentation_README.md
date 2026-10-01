# AllLife Bank – Customer Segmentation using Unsupervised Learning

## Project Overview

This project performs **customer segmentation for AllLife Bank** using unsupervised machine learning techniques. The objective is to discover meaningful groups of customers based on their banking behavior and support targeted customer engagement and marketing strategies.

The analysis applies **K-Means Clustering** and **Hierarchical Clustering** after data cleaning, outlier treatment, and feature scaling.

## Business Objective

AllLife Bank wants to understand its customer base and identify groups of customers with similar banking behavior. The resulting segments can be used to:

- Design targeted marketing campaigns
- Personalize financial products and offers
- Improve customer engagement
- Identify customers with different banking-channel preferences
- Support customer-service and relationship-management strategies

## Dataset

The clustering analysis uses the following customer-behavior variables:

| Feature | Description |
|---|---|
| Average Credit Limit | Average credit limit available to the customer |
| Total Credit Cards | Number of credit cards held |
| Total Bank Visits | Number of visits to the bank |
| Total Online Visits | Number of online banking visits |
| Total Calls Made | Number of customer-service calls |

Identifier fields such as `Sl_No` and `Customer Key` are excluded from the clustering features.

## Project Workflow

1. Business Understanding
2. Data Understanding
3. Exploratory Data Analysis
4. Data Quality Checks
5. Outlier Detection and Treatment
6. Feature Scaling
7. K-Means Clustering
8. Optimal Cluster Selection
9. Hierarchical Clustering
10. Cluster Profiling
11. Business Interpretation
12. Customer Segmentation Recommendations

## Exploratory Data Analysis

The project investigates:

- Dataset structure and data types
- Missing values
- Duplicate records and customer identifiers
- Distribution of numerical variables
- Relationships among customer attributes
- Outliers using the IQR approach
- Correlation among clustering variables

## Data Preprocessing

The preprocessing stage includes:

- Checking for missing values
- Checking for duplicate observations
- Investigating duplicate customer keys
- Identifying outliers using the **Interquartile Range (IQR)** method
- Capping extreme outlier values where appropriate
- Excluding identifier columns from clustering
- Standardizing numerical variables using `StandardScaler`

Scaling is important because the clustering algorithms are distance-based and the variables have different numerical ranges.

## K-Means Clustering

K-Means clustering is used to divide customers into groups with similar behavioral characteristics.

### Cluster Selection

The **Elbow Method** and **Silhouette Score** are used to determine an appropriate number of clusters.

The analysis identifies **3 customer clusters**, with an approximate silhouette score of **0.52**.

The resulting cluster sizes are approximately:

| Cluster | Number of Customers |
|---|---:|
| Cluster 1 | 386 |
| Cluster 2 | 50 |
| Cluster 3 | 224 |

## Hierarchical Clustering

Hierarchical clustering is performed as a complementary segmentation approach.

The analysis evaluates:

- Single Linkage
- Complete Linkage
- Average Linkage
- Ward Linkage

Dendrograms are used to visualize the hierarchical structure of the customer groups, while **cophenetic correlation** is used to evaluate how well the hierarchical structure represents the pairwise distances.

## Cluster Profiling

After clustering, each customer segment is profiled using the original business variables.

The profiles can be compared using:

- Average Credit Limit
- Total Credit Cards
- Total Bank Visits
- Total Online Visits
- Total Calls Made

This helps translate the mathematical clusters into meaningful customer-behavior segments.

## Business Applications

### Targeted Marketing
Create segment-specific campaigns based on credit usage and preferred banking channels.

### Personalized Financial Products
Recommend suitable credit-card and banking products based on customer characteristics.

### Channel Optimization
Use differences in bank visits, online visits, and calls to tailor digital and branch-based engagement.

### Customer Relationship Management
Develop differentiated service strategies for customers with different levels of engagement and credit usage.

### Customer Engagement
Identify customer groups that may benefit from additional engagement, education, or personalized offers.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook / Google Colab

## Machine Learning Techniques

- Exploratory Data Analysis
- IQR-based outlier detection
- Feature scaling
- K-Means clustering
- Elbow Method
- Silhouette Score
- Hierarchical/Agglomerative Clustering
- Dendrogram analysis
- Cophenetic correlation
- Cluster profiling

## Project Structure

```text
AllLife-Bank-Customer-Segmentation/
│
├── README.md
├── Main Project- Pattern Discovery with Unsupervised Learning.html
├── data/
│   └── Credit Card Customer Data.xlsx
│
└── notebooks/
    └── customer_segmentation.ipynb
```

> Update the filenames and folder structure if your GitHub repository uses different names.

## How to Run

1. Clone or download the repository.
2. Open the notebook in **Jupyter Notebook** or **Google Colab**.
3. Place the dataset in the expected data directory.
4. Install the required Python libraries if necessary.
5. Run the notebook cells sequentially.
6. Review the EDA, clustering evaluation, dendrograms, and cluster profiles.

### Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn openpyxl
```

## Results Summary

- Three customer segments were identified using K-Means.
- The selected K-Means solution has an approximate silhouette score of **0.52**.
- The cluster sizes are approximately **386, 50, and 224 customers**.
- Hierarchical clustering was used as a complementary clustering approach.
- Cluster profiling translates the mathematical clusters into customer-behavior insights that can support targeted business actions.

## Conclusion

This project demonstrates how unsupervised learning can be used to identify customer groups without a predefined target variable. By combining **K-Means and Hierarchical Clustering** with exploratory analysis, preprocessing, cluster validation, and business profiling, the analysis provides a structured approach for understanding customer behavior and supporting data-driven customer segmentation.

## Author

**B SRIVIJAY**
