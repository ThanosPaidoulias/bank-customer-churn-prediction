# Bank Customer Churn Prediction

A machine learning project to predict customer churn in the banking sector using advanced classification techniques.

## 📊 Project Overview

Customer churn is a critical business metric for financial institutions. This project develops predictive models to identify customers at risk of churning, enabling proactive retention strategies.

**Key Achievement**: Identified 67% of actual churners using an optimized LGBM model with custom threshold tuning.

## 🎯 Business Problem

- **Goal**: Predict which bank customers are likely to churn
- **Impact**: Enable targeted retention campaigns and reduce customer attrition
- **Approach**: Compare multiple ML algorithms with emphasis on recall to minimize missed churners

## 📁 Repository Structure
```
├── notebook/
│   └── Churn_analysis.ipynb          # Complete analysis and modeling
├── data/
│   └── Churn_data.csv                # Customer dataset
├── report/
│   └── Churn_Analysis.pdf            # Detailed technical report
├── requirements.txt                   # Python dependencies
└── README.md                          # Project documentation
```

## 🔍 Dataset Features

- **CustomerID**: Unique identifier
- **Demographics**: Geography, Gender, Age Band
- **Account Info**: Tenure, Balance, Number of Products
- **Behavior**: Digital transaction ratio, Credit card status, Loan status
- **Target**: Inactive (Churn indicator)

## 🛠️ Technologies Used

- **Python 3.x**
- **Libraries**: 
  - Pandas, NumPy (data manipulation)
  - Scikit-learn (modeling, evaluation)
  - LightGBM (gradient boosting)
  - Matplotlib, Seaborn (visualization)
  - LazyClassifier (model benchmarking)

## 📈 Methodology

### 1. Exploratory Data Analysis
- No missing values detected
- ~20% churn rate (moderately imbalanced)
- Key findings: Higher balance correlates with increased churn, shorter tenure indicates higher risk

### 2. Data Preprocessing
- Outlier analysis using IQR method
- Feature scaling (StandardScaler)
- One-hot encoding for categorical variables
- Train-test split (80/20)

### 3. Model Development

**Models Evaluated:**
- LGBMClassifier (best performance)
- Random Forest Classifier
- Logistic Regression
- Support Vector Machine
- Others via LazyClassifier

### 4. Model Optimization
- Hyperparameter tuning via GridSearchCV
- Custom threshold optimization (0.28) to maximize recall
- Focus on recall over precision to capture more at-risk customers

## 📊 Results

### Best Model: LGBMClassifier with Custom Threshold


### Key Insights

**Most Important Churn Predictors:**
1. Balance (Euros) - Higher balance → higher churn
2. Estimated Income
3. Digital Transaction Ratio
4. Tenure (Years) - Shorter tenure → higher risk
5. Number of Products - Single product users at higher risk

**Customer Segments at Risk:**
- Female customers
- Age groups 25-35 and 35-45
- Customers registered outside Athens
- Single product holders

## 💡 Business Recommendations

1. **Target High-Risk Segments**: Focus retention efforts on customers with high balance and short tenure
2. **Product Cross-Selling**: Encourage single-product customers to adopt additional services
3. **Early Engagement**: Implement onboarding programs for customers in their first year
4. **Geographic Strategy**: Investigate reasons for higher churn in non-Athens regions
5. **Custom Threshold**: Use 0.28 probability threshold to identify 2 out of 3 potential churners for proactive outreach

## 🚀 Future Enhancements

- Incorporate temporal features (seasonality, trends)
- Gather customer interaction data (support tickets, complaints)
- Implement RFM (Recency, Frequency, Monetary) segmentation
- Deploy model as API for real-time predictions
- A/B test retention strategies on predicted churners

## 📖 How to Use

### Installation
```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/bank-customer-churn-prediction.git

# Navigate to project directory
cd bank-customer-churn-prediction

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter Notebook
jupyter notebook notebook/Churn_analysis.ipynb
```

### Running the Analysis

1. Open `Churn_analysis.ipynb` in Jupyter
2. Run all cells sequentially
3. Review model outputs and visualizations
4. Check `report/Churn_Analysis.pdf` for detailed findings

## 📄 Detailed Report

For a comprehensive analysis including methodology, visualizations, and business insights, see [`report/Churn_Analysis.pdf`](report/Churn_Analysis.pdf).

## 👤 Author

**Thanos Paidoulias**
- GitHub: [@YOUR_USERNAME](https://github.com/ThanosPaidoulias)
- LinkedIn: [Your LinkedIn](https://www.linkedin.com/in/thanos-paidoulias/)

## 📝 License

This project is open source and available for educational purposes.

---

⭐ If you found this project helpful, please consider giving it a star!
