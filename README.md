# Bankruptcy Prediction using Machine Learning

This project focuses on predicting the likelihood of a company going bankrupt using various machine learning models such as Random Forest, Support Vector Machines (SVM), and Logistic Regression. A significant emphasis is placed on Exploratory Data Analysis (EDA) to gain a deeper understanding of the financial data and its patterns.

## Project Overview

The objective is to predict company bankruptcy based on several financial indicators. The project is divided into two main phases:
1. **Exploratory Data Analysis (EDA)**
2. **Modeling and Evaluation**

### Key Financial Features:
- **Earnings Per Share (EPS)**: A company’s profitability indicator.
- **Liquidity**: Measures the company's ability to pay off its short-term obligations.
- **Profitability**: The company’s profit margin.
- **Leverage Ratio**: A measure of financial risk by comparing debt to equity.
- **Asset Turnover**: Efficiency in using assets to generate revenue.
- **Return on Equity (ROE)**: Profitability relative to shareholder equity.
- **Market Book Ratio**: A company's market value relative to its book value.
- **Growth Metrics**: Sales, assets, and employee growth.

## Exploratory Data Analysis (EDA)

EDA plays a crucial role in this project, providing insights into the data's structure, distributions, and relationships between key financial metrics and the target variable (`BK` - bankruptcy).

### Key Steps in EDA:
1. **Data Cleaning**: Handling missing values in critical financial columns such as `Assets Growth`, `Sales Growth`, and `Employee Growth`.
2. **Summary Statistics**: Using `.describe()` to examine the central tendencies and spread of financial metrics.
3. **Correlation Matrix**: Understanding the correlations between various financial indicators and their relationship with bankruptcy.
4. **Distribution Plots**: 
   - **Histograms**: For visualizing the distribution of continuous variables like `EPS`, `Liquidity`, and `Profitability`.
   - **Box Plots**: To identify outliers and variability in financial data.
   - **Density Plots**: To visualize the probability distribution of key features, separated by the bankruptcy target (`BK`).
5. **Bivariate Analysis**: 
   - **Scatter plots**: Examining the relationship between `Leverage Ratio`, `Asset Turnover`, and other features against `ROE` and `EPS` to uncover meaningful trends.
   - **Bar Plots**: Comparing the average values of key financial ratios across companies that went bankrupt versus those that did not.
6. **Missing Value Imputation**: Analyzing the extent of missing data and applying strategies such as mean imputation or filling with median values based on the distribution.

### Key Findings from EDA:
- **Profitability** and **Liquidity** tend to be significantly lower for bankrupt companies.
- Companies with higher **Leverage Ratios** and lower **Asset Turnovers** showed a higher probability of bankruptcy.
- **Return on Equity (ROE)** shows a wide variance, but bankrupt companies typically have negative ROE values.
- The correlation between **Market Book Ratio** and **BK** suggests that companies with a higher market-to-book value are less likely to face bankruptcy.

## Modeling

After EDA, various machine learning models are implemented to predict the likelihood of bankruptcy based on the financial indicators.

### Models Used:
1. **Logistic Regression**: For baseline classification.
2. **Random Forest Classifier**: A robust ensemble method that improves prediction accuracy by averaging multiple decision trees.
3. **Support Vector Classifier (SVC)**: To capture complex decision boundaries.
4. **Decision Trees** and **Gradient Boosting Classifier**: For additional comparisons and boosting performance.

### Model Evaluation:
Each model is evaluated using:
- **Confusion Matrix**: To visualize the true positives, false positives, etc.
- **Classification Report**: Providing precision, recall, and F1-score.
- **ROC Curve and AUC**: Measuring model performance in distinguishing between bankrupt and non-bankrupt companies.

## Results

The **Random Forest Classifier** provided the best results with an AUC score of 0.92, high precision, and recall. The **Logistic Regression** and **SVC** models also performed well but had slightly lower performance metrics.

## Dependencies

- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn


