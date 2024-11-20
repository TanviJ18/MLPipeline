# Data Folder

This folder contains the necessary data files for the pipeline, including the **Iris dataset (CSV)** and the **JSON configuration file**.

## Files

1. **iris.csv**:
   - This file contains the well-known **Iris dataset**, which is commonly used for machine learning tasks such as classification and regression. It includes measurements of different attributes of Iris flowers, which are used as input features for predictive modeling.
   - The dataset consists of 150 rows and 5 columns:
     - **sepal_length**: The length of the sepal (in cm).
     - **sepal_width**: The width of the sepal (in cm).
     - **petal_length**: The length of the petal (in cm).
     - **petal_width**: The width of the petal (in cm).
     - **species**: The species of the Iris flower (setosa, versicolor, or virginica).
   - For this pipeline task, the dataset is used for **regression** tasks, specifically predicting continuous variables such as petal length and width based on other features.
  
2. **data.json**:
   - This is the configuration file for the pipeline, where key parameters like **prediction_type**, **model configurations**, and other preprocessing settings are defined.
   - **Important Note**: The original **data.json** file had some structural issues. I have restructured and formatted the file to comply with the correct JSON norms to ensure proper parsing and execution within the pipeline.
