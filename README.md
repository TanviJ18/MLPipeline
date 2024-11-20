# MLPipeline 

### **Introduction**
The pipeline is built for predictive modeling using the **Iris dataset** and is designed to be flexible for both **regression** and **classification** tasks. In this case, I am working with regression-based prediction. The pipeline is dynamic, making it easy to adapt to different models and datasets.


### **Approach**
- **Dataset Used**: Iris dataset (CSV format).
- **Prediction Type**: Regression (as specified in the `prediction_type` field within the **JSON configuration file**, which has been correctly formatted as per standard JSON norms).
- **Pipeline Steps**:
  - **Preprocessing**: 
    - Numerical features are imputed and scaled.
    - Categorical features are imputed using the most frequent strategy and encoded via **One-Hot Encoding**.
  - **Feature Reduction**: 
    - Utilized **SelectFromModel** with a **RandomForestRegressor** to identify and select top features before the model is trained.
  - **Modeling**:
    - The pipeline uses **DecisionTreeRegressor** by default, but it's easy to swap it out for any other regression model, such as **RandomForestRegressor** or **LinearRegression**.
  
### **Metrics**

#### For Regression:
Since the **prediction_type** in the JSON configuration file is set to regression, the following metrics will be used to evaluate model performance:
- **Mean Squared Error (MSE)**: 
  - Measures the average squared difference between the actual and predicted values. A lower MSE indicates better model performance.
  
- **Mean Absolute Error (MAE)**:
  - Calculates the average absolute difference between predicted and actual values. It helps in understanding the magnitude of errors.
  
- **R² Score**: 
  - Shows how well the model explains the variance in the data. A value closer to **1** signifies a better fit.

- **Explained Variance**:
  - Measures how much of the total variance in the data is captured by the model. Higher values indicate better performance in terms of explaining variance.

#### For Classification:
If the **prediction_type** is set to classification, the following metrics will be used:
- **Accuracy**: 
  - Measures the proportion of correctly predicted instances out of all instances. It's a simple and effective performance gauge.
  
- **F1 Score**: 
  - The weighted average of **Precision** and **Recall**, useful for evaluating imbalanced datasets and balancing false positives and false negatives.
  
- **ROC AUC**: 
  - The Area Under the Receiver Operating Characteristic Curve, which indicates the model's ability to distinguish between classes. A higher value signifies better performance.

- **Confusion Matrix**:
  - Summarizes prediction results by showing true positives, false positives, true negatives, and false negatives, providing deeper insight into classification performance.

### **Dynamic Pipeline**
This pipeline is highly flexible and offers several key benefits:
- **Model Swapping**: 
  - One can easily replace the current **DecisionTreeRegressor** with any other regression or classification model (e.g., **RandomForestRegressor**, **LinearRegression**, or **LogisticRegression**).
  
- **Customizable Preprocessing**: 
  - Preprocessing steps like **imputation**, **scaling**, and **encoding** are easily customizable to suit different data types.

- **Extendable Metrics**:
  - The pipeline allows for adding or modifying evaluation metrics to suit the task, whether it’s regression or classification.

- **JSON Configuration**:
  - The pipeline makes use of a **JSON configuration file** (`data.json`), which has been carefully formatted to comply with correct JSON standards, ensuring seamless integration with the pipeline components and flexibility in adjusting dataset configurations, model parameters, and metric selection.

### **Results**
Once you run the pipeline on the Iris dataset, the regression model will return results based on the metrics mentioned above. These results give you valuable insights into how well the model is predicting continuous values like sepal and petal dimensions.

### **Conclusion**
This repository offers a flexible and dynamic predictive modeling pipeline, adaptable for both **regression** and **classification** tasks. By modifying the **data.json** configuration file, which is correctly formatted as per JSON standards, one can easily apply this pipeline to various datasets or models.
