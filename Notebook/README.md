## Folder Content

- **notebook.ipynb**: This is the main Jupyter notebook that has the process of predictive modeling, including data loading, preprocessing, feature selection, model training, and evaluation.

## Workflow Overview

The notebook covers the following steps:

1. **Data Loading**: The Iris dataset is loaded into the notebook from a CSV file.

2. **Data Preprocessing**: 
   - Numerical features are imputed with a specified strategy, and they are scaled for better model performance.
   - Categorical features (if any) are imputed with the most frequent strategy and encoded using One-Hot Encoding.
   
3. **Feature Selection**: 
   - Feature reduction is performed using **SelectFromModel**, leveraging **RandomForestRegressor** to identify and select the most important features for the model.

4. **Model Training**: 
   - The **DecisionTreeRegressor** is used to train a regression model. This model can easily be swapped with other regression models (such as **RandomForestRegressor**, **LinearRegression**, etc.) based on the needs.

5. **Model Evaluation**: 
   - The model's performance is evaluated using appropriate metrics based on whether it's a regression or classification task.

## Model Evaluation

### Regression

For **regression** tasks, the following metrics are used:

- **Mean Squared Error (MSE)**: Measures the average squared difference between actual and predicted values. A lower MSE indicates better model performance.
  
- **Mean Absolute Error (MAE)**: Calculates the average absolute difference between predicted and actual values. This metric helps to understand the magnitude of errors in the predictions.

- **R² Score**: Indicates how well the model explains the variance in the data. A value closer to 1 signifies a better model fit.

- **Explained Variance**: Measures the proportion of the total variance in the data that is captured by the model. Higher values indicate better performance in terms of variance explanation.

### Classification

For **classification** tasks, if the `prediction_type` is set up for classification (i.e., using **LogisticRegression** or similar), the following metrics would be used:

- **Accuracy**: Measures the proportion of correctly predicted instances over the total instances. It provides a straightforward way to gauge model performance.

- **F1 Score**: The weighted average of Precision and Recall. This metric is useful for imbalanced datasets, as it balances the trade-off between false positives and false negatives.

- **ROC AUC**: The Area Under the Receiver Operating Characteristic Curve measures how well the model distinguishes between different classes. A higher value indicates better model performance.

- **Confusion Matrix**: A matrix that summarizes prediction results, showing the number of true positives, false positives, true negatives, and false negatives. This helps in understanding where the model is making errors.

## Requirements

For running the Jupyter notebooks, the following Python libraries are required:

- **pandas**
- **numpy**
- **scikit-learn**
- **matplotlib**
- **seaborn**

