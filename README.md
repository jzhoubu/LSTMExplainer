
# Update
- **2019/01/30**
    + **Meeting**: Pivot direction to **SHAP**

- **2019/01/31**
    + **Direction**: Produce a LSTM model from Kaggle dataset for Experiment
    + **Experiment**:
        * Requirement: {keras: 2.2.2, tensorflow: 1.10.0, shap: 0.28.3}
        * Data set: Stock time series data
        * **Shape**
            * **X_train**: (2709, 60, 4) --> (batch, time_stamps, features) 
            * **y_train**: (2709, ) 
            * **LSTM first layer input**: (60, 4)-->(time_stamps, features) 
            > model.add(LSTM(units=50, return_sequences=True, input_shape=(X_train.shape[1],4)))
            * **SHAP values output**: (1, 5, 60, 4)
            * **shap_values[0][1] shape**: (60, 4) --> (time_stamps, features)

- **2019/02/02**
    + Meeting at everning

