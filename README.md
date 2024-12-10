# Housing Prices Model Card
### Basic Information
* **Person(s) developing model**: Jackson P.,'jackson.pentecost@gwu.edu', Edwin O.,'edwin.ordonez@gwu.edu' Ambuja S.,'asharma22@gwu.edu', Mehek L., 'mehek.lasker@gwu.edu'  
* **Model date**: December, 2024
* **Model version**: 1.0
* **License**: MIT 2.0
* **Model implementation code**:
  
### Intended Use
* **Primary intended uses**: This model is an predictor of sales price, with an use case for determining general sales prices based on a variety of housing features.
* **Primary intended users**: Students in DNSC 3288 or at GWU.
* **Out-of-scope use cases**: Any use beyond an educational case is out-of-scope.

### Training Data
* **Source of Training Data**: Kaggle Housing Prices Competition, https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques
* **How training data was divided**: 70% Training and 30% Validation
* **Number of rows** 1,022 in Training Data, 438 in Validation
* Data Dictionary

| Name                | Modeling Role         | Measurement Level      | Description                                                                 |
|---------------------|-----------------------|------------------------|-----------------------------------------------------------------------------|
| **SalePrice**       | target               | float                  | The property's sale price in dollars.                                      |
| **MSSubClass**      | input                | int                    | The building class.                                                        |
| **MSZoning**        | input                | categorical            | The general zoning classification.                                         |
| **LotFrontage**     | input                | float                  | Linear feet of street connected to property.                               |
| **LotArea**         | input                | float                  | Lot size in square feet.                                                   |
| **Street**          | input                | categorical            | Type of road access.                                                       |
| **Alley**           | input                | categorical            | Type of alley access.                                                      |
| **LotShape**        | input                | categorical            | General shape of property.                                                 |
| **LandContour**     | input                | categorical            | Flatness of the property.                                                  |
| **Utilities**       | input                | categorical            | Type of utilities available.                                               |
| **LotConfig**       | input                | categorical            | Lot configuration.                                                         |
| **LandSlope**       | input                | categorical            | Slope of property.                                                         |
| **Neighborhood**    | input                | categorical            | Physical locations within Ames city limits.                                |
| **Condition1**      | input                | categorical            | Proximity to main road or railroad.                                        |
| **Condition2**      | input                | categorical            | Proximity to main road or railroad (if a second is present).               |
| **BldgType**        | input                | categorical            | Type of dwelling.                                                          |
| **HouseStyle**      | input                | categorical            | Style of dwelling.                                                         |
| **OverallQual**     | input                | int                    | Overall material and finish quality.                                       |
| **OverallCond**     | input                | int                    | Overall condition rating.                                                  |
| **YearBuilt**       | input                | int                    | Original construction date.                                                |
| **YearRemodAdd**    | input                | int                    | Remodel date.                                                              |
| **RoofStyle**       | input                | categorical            | Type of roof.                                                              |
| **RoofMatl**        | input                | categorical            | Roof material.                                                             |
| **Exterior1st**     | input                | categorical            | Exterior covering on house.                                                |
| **Exterior2nd**     | input                | categorical            | Exterior covering on house (if more than one material).                    |
| **MasVnrType**      | input                | categorical            | Masonry veneer type.                                                       |
| **MasVnrArea**      | input                | float                  | Masonry veneer area in square feet.                                        |
| **ExterQual**       | input                | categorical            | Exterior material quality.                                                 |
| **ExterCond**       | input                | categorical            | Present condition of the material on the exterior.                         |
| **Foundation**      | input                | categorical            | Type of foundation.                                                        |
| **BsmtQual**        | input                | categorical            | Height of the basement.                                                    |
| **BsmtCond**        | input                | categorical            | General condition of the basement.                                         |
| **BsmtExposure**    | input                | categorical            | Walkout or garden level basement walls.                                    |
| **BsmtFinType1**    | input                | categorical            | Quality of basement finished area.                                         |
| **BsmtFinSF1**      | input                | float                  | Type 1 finished square feet.                                               |
| **BsmtFinType2**    | input                | categorical            | Quality of second finished area (if present).                              |
| **BsmtFinSF2**      | input                | float                  | Type 2 finished square feet.                                               |
| **BsmtUnfSF**       | input                | float                  | Unfinished square feet of basement area.                                   |
| **TotalBsmtSF**     | input                | float                  | Total square feet of basement area.                                        |
| **Heating**         | input                | categorical            | Type of heating.                                                           |
| **HeatingQC**       | input                | categorical            | Heating quality and condition.                                             |
| **CentralAir**      | input                | categorical            | Central air conditioning.                                                  |
| **Electrical**      | input                | categorical            | Electrical system.                                                         |
| **1stFlrSF**        | input                | float                  | First floor square feet.                                                   |
| **2ndFlrSF**        | input                | float                  | Second floor square feet.                                                  |
| **LowQualFinSF**    | input                | float                  | Low quality finished square feet (all floors).                             |
| **GrLivArea**       | input                | float                  | Above grade (ground) living area square feet.                              |
| **BsmtFullBath**    | input                | int                    | Basement full bathrooms.                                                   |
| **BsmtHalfBath**    | input                | int                    | Basement half bathrooms.                                                   |
| **FullBath**        | input                | int                    | Full bathrooms above grade.                                                |
| **HalfBath**        | input                | int                    | Half baths above grade.                                                    |
| **Bedroom**         | input                | int                    | Number of bedrooms above basement level.                                   |
| **Kitchen**         | input                | int                    | Number of kitchens.                                                        |
| **KitchenQual**     | input                | categorical            | Kitchen quality.                                                           |
| **TotRmsAbvGrd**    | input                | int                    | Total rooms above grade (does not include bathrooms).                      |
| **Functional**      | input                | categorical            | Home functionality rating.                                                 |
| **Fireplaces**      | input                | int                    | Number of fireplaces.                                                      |
| **FireplaceQu**     | input                | categorical            | Fireplace quality.                                                         |
| **GarageType**      | input                | categorical            | Garage location.                                                           |
| **GarageYrBlt**     | input                | int                    | Year garage was built.                                                     |
| **GarageFinish**    | input                | categorical            | Interior finish of the garage.                                             |
| **GarageCars**      | input                | int                    | Size of garage in car capacity.                                            |
| **GarageArea**      | input                | float                  | Size of garage in square feet.                                             |
| **GarageQual**      | input                | categorical            | Garage quality.                                                            |
| **GarageCond**      | input                | categorical            | Garage condition.                                                          |
| **PavedDrive**      | input                | categorical            | Paved driveway.                                                            |
| **WoodDeckSF**      | input                | float                  | Wood deck area in square feet.                                             |
| **OpenPorchSF**     | input                | float                  | Open porch area in square feet.                                            |
| **EnclosedPorch**   | input                | float                  | Enclosed porch area in square feet.                                        |
| **3SsnPorch**       | input                | float                  | Three season porch area in square feet.                                    |
| **ScreenPorch**     | input                | float                  | Screen porch area in square feet.                                          |
| **PoolArea**        | input                | float                  | Pool area in square feet.                                                  |
| **PoolQC**          | input                | categorical            | Pool quality.                                                              |
| **Fence**           | input                | categorical            | Fence quality.                                                             |
| **MiscFeature**     | input                | categorical            | Miscellaneous feature not covered in other categories.                     |
| **MiscVal**         | input                | float                  | $Value of miscellaneous feature.                                           |
| **MoSold**          | input                | int                    | Month sold.                                                                |
| **YrSold**          | input                | int                    | Year sold.                                                                 |
| **SaleType**        | input                | categorical            | Type of sale.                                                              |
| **SaleCondition**   | input                | categorical            | Condition of sale.                                                         |

 ### Test Data
* **Source of test data**:  Kaggle Housing Prices Competition, https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques
* **Number of rows in test data**: 1,459
* **State any differences in columns between training and test data**: Test data does not include Sales Price column, as Sales Price is the variable our model is attempting to predict. 
  
### Model details
* **Columns used as inputs in the final model**: ['MSSubClass', 'LotArea', 'OverallQual', 'OverallCond', 'YearBuilt', 'YearRemodAdd', 'MasVnrArea', 'BsmtFinSF1', 'TotalBsmtSF', 'GrLivArea', 'BsmtFullBath', 'FullBath', 'BedroomAbvGr', 'KitchenAbvGr', 'TotRmsAbvGrd', 'Fireplaces', 'GarageCars', 'WoodDeckSF', 'ScreenPorch']
* **Column(s) used as target(s) in the final model**: 'SalePrice'
* **Type of model(s)**: Backwards Stepwise Linear Regression Model & Decision Tree 
* **Software used to implement the model**: Python, scikit-learn
* **Version of the modeling software**: 1.5.2 
* **Hyperparameters or other settings of your model**:
  (X, y, significance_level=0.05)



### Quantitative Analysis 
* **R2 Outputs**:
  * R-squared for Training Set: 0.7894
  * R-squared for Validation Set: 0.8284
  * R-squared for Test Set: 0.8174

* **ROC**:

Below is the ROC curve for the Backwards Stepwise Regression Model
![image](https://github.com/user-attachments/assets/d6eb061e-6844-4d5b-a5b1-1122dfdb614a)
The Area Under the Receiver Operating Characteristic Curve measures the model's ability to distinguish between classes.

* **Correlation Heatmap**:

Below is the Correlation Heatmap
![image](https://github.com/user-attachments/assets/78a60883-fd67-4246-8874-545f682fae6d)

### Ethical Considerations
* **Potential negative impacts of using our model**:
  * Subjective Data, i.e., Kitchen quality and Quality of basement finished area.
  * Bias in the model would be amplified if data has any bias.
  * Model can become overfit and perform poorly on unseen data.
    
* **Potential uncertainties relating to the impacts of using our model**:
  * The model could create a feedback loop in the housing industry.
  * The model could be breaking Fair Housing Laws unintentionally.
  * Making sure all the data collected was with consent and being used ethically


