# House Price Prediction

Prediction of house prices in Ames, Iowa using over 79 features and about 1460 data points.

## Getting Started

The number of features were many and the number of rows not many. A lot of variables were categorical and needed encoding. Missing value imputation was neccesaary too as there were plenty of columns with lots of missing values.

### Evaluation metric used

Root Mean Squared Logarithmic Error
Implementation:
```
def rmsle(y, y_pred):
        assert len(y) == len(y_pred)
        terms_to_sum = [(math.log(y_pred[i] + 1) - 
        math.log(y[i] + 1)) ** 2.0 
        for i,pred in enumerate(y_pred)]
        return (sum(terms_to_sum) * (1.0/len(y))) ** 0.5
 ```
### Key learning from the project
Linear models perform well when working with less amount of data. The more complex models like the Ensemble Learning techniques tend to overfit with less data

### Algorithm used for final model
Bayesian Ridge Regression

### Accuracy achieved
The RMSLE sscore for Train data was 0.010679 and that for Cross validation data was 0.010246. The model performed with an accuracy of 0.013454 for the Test data.

### Libraries used

* [Pandas](https://pandas.pydata.org/)
* [scikit-learn](https://scikit-learn.org/stable/) 
*  [Matplotlib](https://matplotlib.org) 
