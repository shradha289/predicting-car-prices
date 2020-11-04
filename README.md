# predicting-car-prices
We need to build the model to determine the price of a used car.We are interested in the following parameters :

- the quality of the prediction
- the speed of the prediction
- the time required for training \

The dataset can be found here: www.kaggle.com/dataset/f8a4f6645bbf81179d976bfd42fa80ee167f68e4408da355810110f0dc6ac001

Step 1: Preprocess the data \
We will remove anomalies, fill missing values(where possible), reduce the number of categories for features (there are around 250 categories for Model column), remove uninformative features.

Step 2: Prepare data for model training \
Since we will be building RandomForest and Linear Regression models among others, we need to encode categorical features. One hot encoding has been used for this purpose. For models which deal only with numeric data it is better to use dummification instead of label encoding. Label encoding only maps each string to an integer and the model will wrongly interpret this as having a numeric relationship with target variable and other features. We will also scale numeric variables using StandardScaler. LightGBM and Catboost can work with categorical features so there is no need to send encoded features for model training.

Step 3: Model building \
We will build Linear Regression fo sanity check. Random Forest, and stochastic gradient boosting trees, Xgboost, LightGBM, Catboost.

The statistic used as a measure of model's performance is RMSE. RMSE for test set for each model along with training time and prediction time have been stored in a dataframe for comparison.
