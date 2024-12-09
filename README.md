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

* Data Dictionary
* ═══╤═══════════════╤════════════════════════════════════════════════════════════════════╕
│    │ Feature       │ Description                                                        │
╞════╪═══════════════╪════════════════════════════════════════════════════════════════════╡
│  0 │ SalePrice     │ The property's sale price in dollars. This is the target variable. │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│  1 │ MSSubClass    │ The building class                                                 │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│  2 │ MSZoning      │ The general zoning classification                                  │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│  3 │ LotFrontage   │ Linear feet of street connected to property                        │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│  4 │ LotArea       │ Lot size in square feet                                            │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│  5 │ Street        │ Type of road access                                                │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│  6 │ Alley         │ Type of alley access                                               │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│  7 │ LotShape      │ General shape of property                                          │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│  8 │ LandContour   │ Flatness of the property                                           │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│  9 │ Utilities     │ Type of utilities available                                        │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 10 │ LotConfig     │ Lot configuration                                                  │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 11 │ LandSlope     │ Slope of property                                                  │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 12 │ Neighborhood  │ Physical locations within Ames city limits                         │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 13 │ Condition1    │ Proximity to main road or railroad                                 │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 14 │ Condition2    │ Proximity to main road or railroad (if a second is present)        │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 15 │ BldgType      │ Type of dwelling                                                   │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 16 │ HouseStyle    │ Style of dwelling                                                  │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 17 │ OverallQual   │ Overall material and finish quality                                │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 18 │ OverallCond   │ Overall condition rating                                           │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 19 │ YearBuilt     │ Original construction date                                         │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 20 │ YearRemodAdd  │ Remodel date                                                       │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 21 │ RoofStyle     │ Type of roof                                                       │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 22 │ RoofMatl      │ Roof material                                                      │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 23 │ Exterior1st   │ Exterior covering on house                                         │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 24 │ Exterior2nd   │ Exterior covering on house (if more than one material)             │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 25 │ MasVnrType    │ Masonry veneer type                                                │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 26 │ MasVnrArea    │ Masonry veneer area in square feet                                 │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 27 │ ExterQual     │ Exterior material quality                                          │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 28 │ ExterCond     │ Present condition of the material on the exterior                  │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 29 │ Foundation    │ Type of foundation                                                 │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 30 │ BsmtQual      │ Height of the basement                                             │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 31 │ BsmtCond      │ General condition of the basement                                  │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 32 │ BsmtExposure  │ Walkout or garden level basement walls                             │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 33 │ BsmtFinType1  │ Quality of basement finished area                                  │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 34 │ BsmtFinSF1    │ Type 1 finished square feet                                        │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 35 │ BsmtFinType2  │ Quality of second finished area (if present)                       │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 36 │ BsmtFinSF2    │ Type 2 finished square feet                                        │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 37 │ BsmtUnfSF     │ Unfinished square feet of basement area                            │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 38 │ TotalBsmtSF   │ Total square feet of basement area                                 │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 39 │ Heating       │ Type of heating                                                    │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 40 │ HeatingQC     │ Heating quality and condition                                      │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 41 │ CentralAir    │ Central air conditioning                                           │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 42 │ Electrical    │ Electrical system                                                  │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 43 │ 1stFlrSF      │ First Floor square feet                                            │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 44 │ 2ndFlrSF      │ Second floor square feet                                           │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 45 │ LowQualFinSF  │ Low quality finished square feet (all floors)                      │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 46 │ GrLivArea     │ Above grade (ground) living area square feet                       │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 47 │ BsmtFullBath  │ Basement full bathrooms                                            │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 48 │ BsmtHalfBath  │ Basement half bathrooms                                            │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 49 │ FullBath      │ Full bathrooms above grade                                         │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 50 │ HalfBath      │ Half baths above grade                                             │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 51 │ Bedroom       │ Number of bedrooms above basement level                            │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 52 │ Kitchen       │ Number of kitchens                                                 │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 53 │ KitchenQual   │ Kitchen quality                                                    │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 54 │ TotRmsAbvGrd  │ Total rooms above grade (does not include bathrooms)               │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 55 │ Functional    │ Home functionality rating                                          │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 56 │ Fireplaces    │ Number of fireplaces                                               │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 57 │ FireplaceQu   │ Fireplace quality                                                  │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 58 │ GarageType    │ Garage location                                                    │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 59 │ GarageYrBlt   │ Year garage was built                                              │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 60 │ GarageFinish  │ Interior finish of the garage                                      │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 61 │ GarageCars    │ Size of garage in car capacity                                     │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 62 │ GarageArea    │ Size of garage in square feet                                      │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 63 │ GarageQual    │ Garage quality                                                     │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 64 │ GarageCond    │ Garage condition                                                   │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 65 │ PavedDrive    │ Paved driveway                                                     │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 66 │ WoodDeckSF    │ Wood deck area in square feet                                      │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 67 │ OpenPorchSF   │ Open porch area in square feet                                     │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 68 │ EnclosedPorch │ Enclosed porch area in square feet                                 │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 69 │ 3SsnPorch     │ Three season porch area in square feet                             │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 70 │ ScreenPorch   │ Screen porch area in square feet                                   │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 71 │ PoolArea      │ Pool area in square feet                                           │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 72 │ PoolQC        │ Pool quality                                                       │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 73 │ Fence         │ Fence quality                                                      │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 74 │ MiscFeature   │ Miscellaneous feature not covered in other categories              │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 75 │ MiscVal       │ $Value of miscellaneous feature                                    │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 76 │ MoSold        │ Month Sold                                                         │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 77 │ YrSold        │ Year Sold                                                          │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 78 │ SaleType      │ Type of sale                                                       │
├────┼───────────────┼────────────────────────────────────────────────────────────────────┤
│ 79 │ SaleCondition │ Condition of sale                                                  │
╘════╧═══════════════╧════════════════════════
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
