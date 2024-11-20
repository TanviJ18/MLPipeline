## Overview

The **best_model.pkl** file contains a **RDecisionTreeRegressor** model, which achieved the best performance in predicting continuous values (such as sepal and petal dimensions) from the Iris dataset. This model is based on the optimized hyperparameters and has shown superior accuracy in regression tasks compared to other models tested.

## Model Details
- **Model Type**: DecisionTreeRegressor
- **Dataset Used**: Iris dataset
- **Prediction Type**: Regression (Predicting continuous values)
- **Best Hyperparameters**:
  - `max_depth`: 4

## Model Evaluation
The **DecisionTreeRegressor** model outperformed other models tested during evaluation. Here are the metrics for the best-performing model:

- **Mean Squared Error (MSE)**: 0.050421486
- **Mean Absolute Error (MAE)**: 0.152912698
- **R² Score**: 0.894977118
- **Explained Variance**: 0.895427925

These metrics demonstrate that the **DecisionTreeRegressor** offers a robust model for predicting continuous values from the Iris dataset.

## Conclusion
The **best_model.pkl** file contains the best-performing **DecisionTreeRegressor** model, which achieved optimal results on the Iris dataset with the highest R² score and explained variance, making it an effective model for regression tasks on this dataset.
