# Project---Wafer-fault-detection

Problem Statement:-
To build a classification methodology to predict the quality of wafer sensors based on the given training data.
Basically to build wafer working or not.
Wafer - A wafer is very thin slice of semiconductor material which is used in various electronic circuits &
        electronic devices, it is also used in photovoltaic cell.

      > +1 means that the wafer is in working condition & it does not need to replace
      > -1 means that the wafer is fault & it need to be replaced

# Data validation
In this step, we perform different sets of validation like filename validation, number of columns, name of the
columns,data type of each column and other kind of validations. In this step we have to convert it into CSV file.
This exported CSV file is input for our data training step.

# Data insertion in database
In this step we perform the following things
   1) Database Creation and connection
   2) Table creation in the database
   3) Insertion of files in the table.

# Model training
   1) Data export from DB - The data is stored in database is exported as CSV file to be used for model training.
   2) Data Preprocessing - Checking for null values, imputation for null values using KNNImputer, 
                           removing the features with zero standard deviation etc.
   3) Clustering - The idea behind clustering is to implement different algorithms.To train data in different 
                   clusters. The Kmeans model is trained over preprocessed data and the model is saved for further 
                   use in prediction.
   4) Model Selection - After clusters are created, we find the best model for each cluster. 
                        Two algorithms are used RandomForest and XGBoost.

# Model Prediction
Here also all the above steps like Data Validation, Data Insertion in Database, Data Preprocessing and 
Clustering is performed. Based on the cluster group, the model is loaded and prediction is made. The same main.py
file is used for model prediction
