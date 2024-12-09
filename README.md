# Housing Prices Model Card
### Basic Information
* **Person(s) developing model**: Jackson P.,'jackson.pentecost@gwu.edu', Edwin O.,'edwin.ordonez@gwu.edu' Ambuja S.,'asharma22@gwu.edu', Mehek L., 'mehek.lasker@gwu.edu'  
* **Model date**: December, 2024
* **Model version**: 1.0
* **License**: MIT 2.0
* **Model implementation code**:
  
### Intended Use
* **Primary intended uses**: This model is an *example* probability of default classifier, with an *example* use case for determining eligibility for a credit line increase.
* **Primary intended users**: Students in GWU DNSC 6301 bootcamp.
* **Out-of-scope use cases**: Any use beyond an educational example is out-of-scope.

### Training Data
* **Source of training data**: Kaggle Housing Prices Competition, https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques
* **How training data was divided into training and validation data**: 70% training, 30% validation
* **Number of rows in training and validation data**:
  * Total number of rows: 1,460
  * Training rows: 1,022
  * Validation rows: 438

 ### Test Data
* **Source of test data**:  Kaggle Housing Prices Competition, https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques
* **Number of rows in test data**: 1,459
* **State any differences in columns between training and test data**: Test data does not include Sales Price column, as Sales Price is the variable our model is attempting to predict. 
  
### Model details
* **Columns used as inputs in the final model**: '
* **Column(s) used as target(s) in the final model**: 'SalePrice'
* **Type of model(s)**: Backwards Stepwise Linear Regression Model & Decision Tree 
* **Software used to implement the model**: Python, scikit-learn
* **Version of the modeling software**: 1.5.2 
* **Hyperparameters or other settings of your model**: 
