# SPY Trend Prediction Project

## Objective

The goal of this project is to predict the next-day trend of SPY (S&P 500 ETF) using technical indicators. The objective is to provide investors with actionable insights on whether the SPY price is likely to increase or decrease based on historical data and technical indicators.

## Data Mining Solution

A data mining solution was employed to address the problem by:
- Identifying patterns and relationships between technical indicators and the next-day trend of SPY.
- Enabling more informed investment decisions by analyzing historical data and technical indicators.
  
## Data Preparation

1. **Data Filtration**:
   - Cleaned and filtered the raw data to remove noise and irrelevant information, ensuring high-quality input for modeling.

2. **Feature Extraction**:
   - Extracted relevant features from the raw data, including technical indicators such as OBV, RSI, WMA, and ATR, which are crucial for trend prediction.
     
   ![Alt Text](https://github.com/PrakhyathS/Trend-Prediction/blob/main/Results/Result1.png)

3. **Generating Training and Testing Dataset**:
   - Split the data into training and testing datasets to evaluate model performance. Ensured that the datasets are representative of the underlying data patterns.

4. **Feature Scaling**:
   - Applied feature scaling techniques to normalize the data, improving model convergence and performance.
     
![Alt Text](https://github.com/PrakhyathS/Trend-Prediction/blob/main/Results/Result2.png)

## Modeling

### Overview

The project involved model training and hyperparameter tuning using GridSearchCV for various classification algorithms. The models tested include:
- Decision Tree
- Random Forest
- AdaBoost
- Gradient Boosting
- Support Vector Machine (SVM)

### Implementation

1. **Model Training and Hyperparameter Tuning**:
   - Imported necessary libraries and data.
   - Defined models and hyperparameters.
   - Performed grid search for each model.
   - Printed results including train accuracy, test accuracy, mean cross-validation accuracy, and best parameters.
   - Calculated and printed execution time.

2. **Performance Evaluation**:
   - Compared model performance using Matthews Correlation Coefficient (MCC), test error, and average probability.
   - Results were displayed in a table format showing model performance metrics.

3. **Feature Importance**:
   - Identified key features impacting model predictions:
     - On-Balance Volume (OBV): 0.306
     - Relative Strength Index (RSI_14): 0.254
     - Weighted Moving Average (WMA_14): 0.242
     - Average True Range (ATR_14): 0.197

![Alt Text](https://github.com/PrakhyathS/Trend-Prediction/blob/main/Results/Result3.png)

## Results

- **Best Model**: The Gradient Boosting Classifier outperformed other models with an MCC score of 0.0074 and a test error of 0.5087.
- **SVM Performance**: Although SVM showed better test accuracy, MCC and test error were used for comprehensive model evaluation.
- **Model Drawdown**: Noted some risk associated with the Gradient Boosting model due to drawdowns during evaluation.


![Alt Text](https://github.com/PrakhyathS/Trend-Prediction/blob/main/Results/Result4.png)

## Conclusion

The Gradient Boosting Classifier was identified as the most effective model for predicting SPY's next-day returns. Despite its superior performance, it is essential to account for the associated risk and drawdowns before making investment decisions based on the model’s predictions.

