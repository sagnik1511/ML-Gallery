# Classification : [Supervised Learning] 

## Notebook :
  
  [Notebook link](https://www.kaggle.com/padmanabhabanerjee/wine-quality-tasting)

## Dataset : 
  
  [Portugal Wine Data](https://www.kaggle.com/mpwolke/cusersmarildownloadswinecsv?select=wine.csv)  dataset by Marília Prata

## EDA :

  Boxxplots and scatterplots used to visualise the data !! Boxplots show us the spread of the data and also shows us the outliers present in each feature of the dataset. 
The scatterplot gives us the idea of the distribution of particular feature with respect to another. The correlation heatmap helps us select the best features to be used in the training. It gives us the dependencies of each feature on other.

## Models :

  We have normalised the data because there were many outliers according to the EDA , we have used PCA for best feature selection and also categorised the dependent variable to three classes as **"low"** , **"medium"** and **"high"**.
Then we have used five different classification algorithms and compared each of their results to select the best model and also the best hyperparameter through hyperparameter tuning.
The different algorithms are :
* **Support Vector Machine**
* **Decision Tree**
* **Random Forest**
* **Naive Bayes**
* **Logistic Regression**

## Results :

|Sl.No. |        Model        |  Best_Score 	| Best_Params  	                          |
|-----	|---------------------|---------------|-----------------------------------------|
|   0	  |         svm         |  0.948148  	  | {'C': 1, 'kernel': 'rbf'}  	            |  
|   1	  |    decision_tree    |  0.948148 	  | {'criterion': 'gini', 'max_depth': 5}  	|  
|   2	  |    random_forest    |  0.951235    	| {'max_depth': 8, 'n_estimators': 10}  	|  
|   3   |     naive_bayes     |  0.944444     | {}                                      |
|   4   | logistic_regression |  0.948148     | {'C': 1}                                |

### The table given above shows that Random Forest gives us the best result , so we have used the model to check the cross-validation accuracy.
```
  cross_val_score = 94.93915524557382  
```

### The test accuracy for the model :
```
  test_acc = 93.58024691358024
```
