# Introduction
This project involves building a classification model using TensorFlow and Keras to predict whether a person has diabetes or not. The dataset used for training and testing is sourced from '/kaggle/input/diabetes-prediction-dataset/diabetes_prediction_dataset.csv'.

# Task
The primary objective is to create an accurate model that can effectively distinguish between individuals with and without diabetes. This notebook will guide you through the essential steps, from data loading to model evaluation.

# Preparation
Before diving into the model creation, several preprocessing steps are performed:
1. **Data Loading:** The dataset is loaded using pandas to analyze and manipulate the data.
2. **Data Inspection:** Information and statistical descriptions of the dataset are displayed to gain insights.
3. **Data Balancing:** As the dataset is imbalanced, undersampling is applied to ensure an equal representation of both diabetes and non-diabetes cases.
4. **Label Encoding:** Categorical columns ('gender' and 'smoking_history') are label-encoded to convert them into numerical format.
5. **Data Splitting:** The dataset is split into features (X) and the target variable (y), followed by a further split into training and test sets.

# Steps and Actions
1. **Standardization:** Numerical features are standardized using the StandardScaler to ensure uniform scales, a crucial step for machine learning algorithms sensitive to feature scales.
2. **Model Architecture:** A neural network model is constructed using the Keras Sequential API. It comprises dense layers with ReLU activation, and dropout layers are added to prevent overfitting.
3. **Model Compilation:** The model is compiled with the 'adam' optimizer, 'binary_crossentropy' loss function (suitable for binary classification), and accuracy as a metric for evaluation.
4. **Model Training:** The model is trained on the training set for 20 epochs, and the training process is monitored using the validation set.
5. **Model Evaluation:** The trained model's performance is evaluated on the test set, providing insights into its accuracy and loss.
6. **Model Saving:** The final trained model is saved for future use or deployment.

# Prediction on New Data
To demonstrate the model's predictive capabilities, an example of making predictions on new data is included. This involves creating a DataFrame with input values, encoding categorical columns, standardizing the input data, and utilizing the trained model to make predictions. The predicted probabilities are then converted into binary predictions for easier interpretation.
