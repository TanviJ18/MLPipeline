# Results Folder

This folder contains the results generated from the pipeline, including a PNG image that visualizes the pipeline steps and a CSV file that stores the performance results of various models.

## Files

### 1. **Pipeline.png**
   - This image represents the **pipeline structure** used for predictive modeling on the Iris dataset. It visually outlines the flow of data through various stages of preprocessing, feature selection, and model training.
   - The pipeline includes the following steps:
     1. **Preprocessing**:
        - **Numerical Features**: Imputation of missing values using the mean strategy and scaling of numerical features using **StandardScaler**.
        - **Categorical Features**: Imputation using the most frequent strategy and One-Hot Encoding of categorical variables (such as species).
     2. **Feature Reduction**:
        - A feature selection step using **SelectFromModel** with a **RandomForestRegressor** to select the top features before training the final model.
     3. **Model Training**:
        - A **DecisionTreeRegressor** with a depth of 4 is used as the final model.
   - The image provides a clear view of the entire pipeline, making it easy to understand the process and flow of data through the stages of the modeling process.

### 2. **results.csv**
   - This CSV file stores the performance results of various models evaluated on the Iris dataset. Each row represents the performance metrics for a different model along with the best hyperparameters.
   - The columns in the file include:
     - **best_params**: The hyperparameters of the model that yielded the best performance.
     - **mse**: The Mean Squared Error of the model, indicating the average squared difference between actual and predicted values.
     - **mae**: The Mean Absolute Error, showing the average absolute difference between actual and predicted values.
     - **r2**: The R² Score, which measures the proportion of variance explained by the model.
     - **explained_variance**: The proportion of total variance explained by the model.

   - The results show the performance of different models on the regression task, with the **DecisionTreeRegressor** performing the best in terms of **R²** and **Explained Variance**.
