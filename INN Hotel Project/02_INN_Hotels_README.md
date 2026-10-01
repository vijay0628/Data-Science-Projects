# INN Hotels – Booking Cancellation Prediction

## 📌 Project Overview
This project develops a machine learning solution for predicting hotel booking cancellations using historical booking information from INN Hotels.

INN Hotels operates in Portugal and faces revenue and operational challenges caused by booking cancellations. The project uses historical booking data to identify reservations with a high probability of cancellation before arrival.

## 🎯 Business Problem
Booking cancellations can result in:
- Revenue loss.
- Unused room inventory.
- Lower occupancy.
- Difficult workforce and housekeeping planning.
- Inefficient inventory and reservation management.

The analytical objective is to identify high-risk bookings early enough for the business to take proactive action.

## 🎯 Objectives
### Business Objectives
- Reduce revenue loss caused by cancellations.
- Improve occupancy by identifying high-risk bookings.
- Support cancellation and refund policy decisions.
- Improve revenue management.
- Support staffing and housekeeping planning.
- Enable targeted customer-retention strategies.

### Technical Objectives
- Perform comprehensive EDA.
- Identify important cancellation drivers.
- Engineer meaningful predictive features.
- Build and compare classification models.
- Evaluate models using business-relevant metrics.
- Interpret feature importance.
- Produce actionable business recommendations.

## 🔍 Exploratory Data Analysis
The project examines booking behavior, cancellation patterns, customer characteristics, pricing, lead time, stay characteristics, market segments, meal plans, room types, special requests, and other booking attributes.

Statistical testing was also performed using:
- ANOVA
- Chi-Square tests
- Mutual Information

The analysis identified variables such as **Lead Time, Average Price, and Special Requests** among the important cancellation-related drivers.

## ⚙️ Feature Engineering
Domain-specific features were created to capture:
- Total guests.
- Stay type.
- Weekend-stay indicators.
- Lead-time categories.
- Arrival season.
- Average price per person.

Feature engineering was designed to capture guest commitment, economic value, and non-linear temporal cancellation risk.

## 🧹 Data Preprocessing
The project includes:
- Removal of non-predictive identifiers such as `Booking_ID`.
- One-hot encoding of categorical variables.
- Numerical scaling.
- Train/test separation.
- SMOTE-based class balancing.
- Data-leakage auditing.
- Multicollinearity and redundant-feature management.

The final engineered feature matrix contains **35 features** before modeling, with the training data balanced using SMOTE.

## 🤖 Machine Learning Models
The modeling workflow includes:
- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting
- XGBoost

Model evaluation emphasizes:
- Recall
- Precision
- F1-Score
- Accuracy
- ROC-AUC

Recall is particularly important because failing to identify an actual cancellation can lead to revenue and operational consequences.

## 📊 Modeling Workflow
```text
Raw Booking Data
       ↓
Data Quality Audit
       ↓
EDA & Statistical Testing
       ↓
Feature Engineering
       ↓
Categorical Encoding
       ↓
Train/Test Split
       ↓
SMOTE on Training Data
       ↓
Feature Scaling
       ↓
Model Training
       ↓
Model Evaluation
       ↓
Feature Importance
       ↓
Business Recommendations
```

## 💡 Key Insights
- Lead time is an important cancellation-related factor.
- Pricing characteristics provide useful information for cancellation prediction.
- Special requests contain meaningful behavioral information.
- Engineered variables such as `lead_time_category` and `is_weekend_stay` were introduced to capture non-linear and temporal effects.
- SMOTE was applied to improve sensitivity toward the cancellation class.
- Leakage checks were performed to maintain separation between training information and test information.

## 💼 Expected Business Applications
The predictive solution can support:
- Proactive communication with high-risk reservations.
- Room allocation and inventory planning.
- Revenue-management decisions.
- Dynamic pricing strategies.
- Staffing and housekeeping planning.
- Customer-retention initiatives.

## 🛠️ Technologies
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn / SMOTE
- XGBoost
- Jupyter Notebook / Google Colab

## 🚀 How to Run
1. Open the notebook in Google Colab or Jupyter Notebook.
2. Upload/provide the hotel booking dataset.
3. Execute the notebook sequentially.
4. Review EDA, feature engineering, preprocessing, model evaluation, and business recommendations.

## 📂 Suggested Repository Structure
```text
INN-Hotels-Cancellation-Prediction/
├── README.md
├── MainProject2-INNHotel.ipynb
├── data/
└── outputs/
```

## 👤 Author
**B SRIVIJAY**
