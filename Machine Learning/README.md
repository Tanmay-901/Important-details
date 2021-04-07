# How to write a ML code(overview)
1. Import Pandas Library to read the dataset.  
`import pandas as pd` 

2. Read dataset using read_csv module and save in some variable.  
`var_name = pd.read_csv('dataset_name.csv')`  

3. Check data set.  
`iris.head()`  

5. Declare and assign independent(x) and dependent(y) variables.  

6. Divide the train and test data from the dataset.  
`from sklearn.model_selection import train_test_split`  
`x_train, x_test, y_train, y_test = train_test_split(x, y, test_size = 0.35)`  
-> here test data will be 35% and train data will be 65% of the overall dataset.  

7. Import the regressor/classifier model.  
`from sklearn.linear_model import LogisticRegression`  OR,
`from sklearn.linear_model import LinearRegression`  

8. make instance of the regressor/classifier model.  
`log_model = Logistic_Regression()`  

9. Fit the train data.  
`log_model.fit(x_train, y_train)`  

10. Make prediction using the model.  
`y_pred = dtc.predict(x_test)`  

11. Import confusion matrix.  
`from sklearn.metrics import confusion_matrix`  

12. Run confusion matrix to check and calculate the accuracy of the prediction model.  
`confusion_matrix(y_test, y_pred)`  

13. In the confusion matrix, check the sum of the left diagonal for correct predictions and right diagonal for wrong predictions.  

14. accuracy of the model = sum(left diagonal)/sum of total matrix  
