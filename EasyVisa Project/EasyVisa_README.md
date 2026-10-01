# EasyVisa – Visa Application Classification

## 📌 Project Overview
EasyVisa is a machine learning classification project focused on predicting the outcome of visa applications. The target variable is `case_status`, with two outcomes: **Certified** and **Denied**.

The project analyzes applicant, employer, employment, wage, education, experience, and geographical characteristics to understand factors associated with visa case outcomes and build predictive classification models.

## 🎯 Business Objective
The project aims to:
- Support a more efficient and data-driven visa certification process.
- Identify applicant and employer characteristics associated with case status.
- Develop a model capable of predicting visa application outcomes.
- Provide evidence-based insights that can support decision-making for increasing application volumes.

## 🔍 Analytical Approach
The project follows this workflow:

**Business Understanding → Data Understanding → EDA → Data Preprocessing → Original Data Modeling → Oversampling → Undersampling → Hyperparameter Tuning → Model Comparison → Final Model Selection → Business Insights**

## 📊 Exploratory Data Analysis
EDA examined:
- Applicant and employer characteristics.
- Education and previous-job-experience patterns.
- Prevailing wage differences between Certified and Denied cases.
- Relationships among numerical variables.
- Class distribution and categorical patterns.

The analysis found noticeable differences in certification rates across education level and previous job experience, while prevailing wage also showed meaningful differences between Certified and Denied cases.

## 🧹 Data Preprocessing
The project includes:
- Data-quality checks.
- Duplicate and missing-value checks.
- Categorical-variable preprocessing.
- Feature preparation for classification.
- Class-imbalance experiments using oversampling and undersampling.
- Train/test separation to evaluate generalization on unseen applications.

## 🤖 Machine Learning Models
The following classification approaches were evaluated:
- Decision Tree
- Bagging
- Random Forest
- AdaBoost
- Gradient Boosting

Models were evaluated using:
- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC

## 📈 Model Results – Original Dataset

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Decision Tree | 0.6464 | 0.7388 | 0.7280 | 0.7334 | 0.6051 |
| Bagging | 0.7137 | 0.7623 | 0.8302 | 0.7948 | 0.7445 |
| Random Forest | 0.7194 | 0.7681 | 0.8308 | 0.7982 | 0.7502 |
| AdaBoost | 0.7329 | 0.7576 | 0.8825 | 0.8153 | 0.7672 |
| Gradient Boosting | 0.7473 | 0.7774 | 0.8710 | 0.8216 | 0.7776 |

The project reports Gradient Boosting with an accuracy of 0.7473, F1-score of 0.8216 and ROC-AUC of 0.7776 on the original dataset. AdaBoost recorded recall of 0.8825.

## 🔄 Class-Imbalance Experiments
Both oversampling and undersampling were evaluated.

For the undersampled dataset, Gradient Boosting achieved:
- Accuracy: 0.7111
- Precision: 0.8253
- Recall: 0.7200
- F1-Score: 0.7691
- ROC-AUC: 0.7752

This experiment demonstrated the trade-off between precision and recall when changing the class distribution.

## 💡 Key Insights
- Visa case status is associated with a combination of applicant, employer, wage, education, experience, and geographical characteristics.
- Education level and previous job experience show noticeable differences in observed certification rates.
- Prevailing wage provides additional information for distinguishing case outcomes.
- Ensemble methods generally provide stronger predictive performance than a single Decision Tree in the evaluated experiments.
- Class-balancing strategy materially changes the precision/recall trade-off.

## 🛠️ Technologies
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook / Google Colab

## 🚀 How to Run
1. Open the project notebook in Google Colab or Jupyter Notebook.
2. Upload/provide the required dataset.
3. Run the notebook cells sequentially.
4. Review the EDA, preprocessing, model evaluation, and business-insight sections.

## 📂 Suggested Repository Structure
```text
EasyVisa/
├── README.md
├── EasyVisa.ipynb
├── data/
└── outputs/
```

## 👤 Author
**B SRIVIJAY**
