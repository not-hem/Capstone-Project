# Telecom Churn Project

## Project Overview
This project aims to predict customer churn in the telecom industry using machine learning models. The dataset contains customer usage patterns, recharge history, and engagement behavior. The objective is to identify high-value customers at risk of churning and provide actionable insights for customer retention.

## Dataset
The dataset consists of telecom usage data for multiple customers. Key features include:
- Recharge amounts over different months
- Voice and data usage
- Customer engagement metrics
- Churn indicator for target prediction

## Steps Followed

### 1. Data Preprocessing
- Converted columns to appropriate numerical formats.
- Identified high-value customers based on recharge amounts.
- Defined churn based on customer inactivity.
- Handled missing values by removing highly missing columns and imputing medians.
- Encoded categorical features using Label Encoding.
- Removed highly correlated features to improve model efficiency.

### 2. Handling Class Imbalance
- Applied **Synthetic Minority Over-sampling Technique (SMOTE)** to balance churn vs. non-churn data.

### 3. Feature Engineering
- Created an `avg_rech_amt_6_7` feature to determine high-value customers.
- Dropped unnecessary columns to remove redundancy.

### 4. Model Training
- **Logistic Regression** and **Random Forest Classifier** were trained to predict churn.
- **Hyperparameter tuning** was performed using `RandomizedSearchCV` for optimizing the Random Forest model.
- Data was standardized using `StandardScaler` before model training.

### 5. Model Evaluation
- Evaluated models using:
  - **Classification report** (Precision, Recall, F1-score)
  - **ROC-AUC score** for assessing predictive performance
  - **Confusion matrix** to visualize performance
  - **Feature importance analysis** to determine key churn indicators

### 6. Visualization
- **ROC-AUC Curve** was plotted for both models.
- **Feature Importance Bar Plot** highlighted the top 20 most significant factors influencing churn.

## Results
- The **Random Forest model** outperformed Logistic Regression based on AUC score.
- Key churn indicators include **recharge amounts, voice call usage, and data consumption trends**.

## Business Recommendations
1. **Targeted Retention Offers**: Provide discounts or incentives for customers showing declining recharge amounts.
2. **Personalized Plans**: Offer customized plans for high-value customers with changing usage patterns.
3. **Early Intervention**: Engage customers who have reduced activity in recent months to prevent churn.
4. **Loyalty Programs**: Encourage long-term customer engagement through exclusive rewards and benefits.

## Dependencies
- Python (3.x)
- Pandas, NumPy, Matplotlib, Seaborn (for data processing and visualization)
- Scikit-learn (for ML models and preprocessing)
- Imbalanced-learn (for SMOTE oversampling)

## How to Run
1. Install required dependencies using:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn
   ```
2. Run the Python script:
   ```bash
   python churn_prediction.py
   ```
3. Check outputs including model reports, plots, and recommendations.

## Future Improvements
- Implement deep learning models for improved accuracy.
- Explore additional customer behavior features.
- Deploy as a web-based dashboard for business users.

---
This project helps telecom companies **predict churn, retain high-value customers, and improve revenue streams** by taking data-driven decisions!

