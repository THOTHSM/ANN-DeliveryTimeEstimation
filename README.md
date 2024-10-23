# ANN : Delivery time estimation

### Overview
The goal of this project was to develop a predictive model to estimate delivery times for Porter, utilizing a dataset comprising various features related to stores and delivery operations. The process encompassed data preprocessing, feature engineering, model building, hyperparameter tuning, and evaluation.

### Goal
The primary objective was to create a robust predictive model that accurately estimates delivery times based on the available data. This model aims to optimize Porter’s delivery operations, enhance customer satisfaction, and improve overall efficiency in logistics management.

### Summary:

### Data Preprocessing

#### Feature Engineering:
- **Encoding Categorical Variables**: Mean encoding was employed to transform categorical features, such as `store_id` and `store_primary_category`, into numerical values based on their mean target values.
- **Handling Missing Values**: Appropriate techniques were used to impute missing values in the dataset, ensuring completeness and usability of the data.

#### Feature Scaling:
- **Standardization**: Features were scaled using Standard Scaler to guarantee that all features contributed equally to the model training process.

### Model Building and Hyperparameter Tuning

#### Neural Network Model:
- A neural network model was defined with:
  - An input layer
  - Several hidden layers with dropout for regularization
  - An output layer
- Dropout layers were integrated to mitigate overfitting. The model was compiled with a learning rate of **0.0005** and utilized the **mean_squared_error** loss function.

#### Hyperparameter Search:
- **Hyperparameters Tuned**:
  - Learning rate
  - Number of layers and nodes
  - Dropout rate
  - Regularization strengths (L1 and L2)
- The model was trained with various combinations of these hyperparameters using a grid search approach to identify the best-performing configuration.

### Model Evaluation

#### Validation Performance:
- The best model was selected based on the lowest mean squared error (MSE) on the validation set.

#### Final Model Performance:
- **MSE**: 0.0791
- **RMSE**: 0.2812
- **MAE**: 0.1913
- **R² Score**: 0.2016

These metrics indicate a moderate level of performance, with the model explaining approximately 20% of the variance in delivery times. The MSE and RMSE values are relatively low, suggesting that the predictions are reasonably close to actual values.

### Key Takeaways
- Feature engineering and feature scaling were crucial steps in preparing the data for modeling.
- Dropout and regularization techniques were implemented to prevent overfitting and enhance generalization.
- The hyperparameter tuning process facilitated the identification of the optimal model configuration for the given data.
- The final model demonstrated reasonable predictive performance; however, there may be opportunities for further improvements through additional feature engineering or advanced modeling techniques.

This summary provides a comprehensive overview of the work completed and the results achieved in the Porter business case analysis.

