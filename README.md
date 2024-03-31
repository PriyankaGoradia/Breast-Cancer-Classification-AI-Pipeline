# Breast Cancer Classification Pipeline

This project aims to classify breast cancer tumors as benign or malignant using machine learning techniques. The pipeline includes data preprocessing, model building, and performance evaluation steps.

## Dataset Preprocessing

The dataset is processed by checking for missing data. Mean imputation is used if needed. The dataset is then analyzed by computing the median, 1st and 3rd quartile, minimum, and maximum values for each attribute. This information is visualized using side-by-side box and whisker plots for each attribute using Matplotlib and Seaborn libraries.

## Class Label Transformation

The class labels are transformed to 0 for benign and 1 for malignant tumors.

## Data Splitting

The data is split into training and testing sets using the train_test_split function from the sklearn.model_selection module.

## AI Pipeline Construction

1. **Data Scaling:** The data is scaled using Min-Max scaling from the sklearn.preprocessing module. This scaler is added to the pipeline.
   
2. **Model Building:** The k-Nearest Neighbors (k-NN) classifier is added to the pipeline.

3. **Parameter Tuning:** GridSearchCV is used for automatic exploration of the k-NN algorithm's performance for different values of k in the range (1,10).

4. **Performance Evaluation:** The F1 score is used for performance evaluation of the classifier.

5. **Best Parameter Selection:** The pipeline identifies the best choice of the parameter k that maximizes the F1 score.

## References

- Download the Wisconsin Breast Cancer dataset: https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic
- The breast cancer dataset is a classic & easy binary classification dataset. 30 
features, 569 instances 1: malignant, 0:benign
