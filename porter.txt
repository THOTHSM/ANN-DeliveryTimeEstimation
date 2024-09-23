Summary of Porter Business Case Analysis

Overview
The goal was to develop a predictive model to estimate delivery times for Porter, using a dataset with various features related to stores and delivery operations. The process involved data preprocessing, feature engineering, model building, hyper parameter tuning, and evaluation.

Data Preprocessing

    Feature Engineering:
        Encoding Categorical Variables: Mean encoding was used to transform categorical features such as store_id and store_primary_category into numerical values based on the mean target values.
        Handling Missing Values: Missing values in the dataset were imputed using appropriate techniques to ensure completeness.

    Feature Scaling:
        Standardization: Features were scaled using Standard Scaler to ensure that all features contributed equally to the model training.

Model Building and Hyper parameter Tuning

    Neural Network Model:
        A neural network model was defined with an input layer, several hidden layers with dropout for regularization, and an output layer.
        Dropout layers were added to prevent overfitting, and the model was compiled with a learning rate of 0.0005 and the mean_squared_error loss function.

    Hyper parameter Search:
        Hyper parameters Tuned:
            Learning rate
            Number of layers and nodes
            Dropout rate
            Regularization strengths (L1 and L2)
        The model was trained with different combinations of these hyper parameters using a grid search approach to identify the best performing configuration.

Model Evaluation

    Validation Performance:
        The best model was selected based on the lowest mean squared error (MSE) on the validation set.

    Final Model Performance:
        MSE: 0.0791
        RMSE: 0.2812
        MAE: 0.1913
        RÂ² Score: 0.2016

    These metrics indicate a moderate level of performance, with the model explaining approximately 20% of the variance in delivery times. The MSE and RMSE values are relatively low, suggesting that the predictions are reasonably close to actual values.

Key Takeaways

    Feature Engineering and Feature Scaling were crucial steps in preparing the data for modeling.
    Dropout and Regularization techniques were implemented to prevent overfitting and improve generalization.
    The hyper parameter tuning process helped identify the optimal model configuration for the given data.
    The final model demonstrated reasonable predictive performance, but there may be opportunities for further improvements through additional feature engineering or advanced modeling techniques.

This summary provides a comprehensive view of the work completed and the results achieved in the Porter business case analysis.
