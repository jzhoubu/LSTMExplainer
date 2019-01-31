
# Update
- **2019/01/30**
    + **Meet**: Fix Direction to **work on SHAP**
    + **Next Meet**: 2019/02/03 evening to discuss the possibility of SHAP 

- **2019/01/31**
    + **Direction**: Produce a LSTM model from Kaggle dataset for Experiment
    + **Experiment**:
        * Requirement: {keras: 2.2.2, tensorflow: 1.10.0, shap: 0.28.3}
        * Data set: Stock time series data
        * **Shape**
            * **X_train shape**: (2709, 60, 4) --> (batch, time_stamps, features) 
            * **LSTM input shape**: (60, 4)-->(time_stamps, features) 
            * **SHAP values output shape**: (1, 5, 60, 4)
            * **shap_values[0][1] shape**: (60, 4) --> (time_stamps, features)