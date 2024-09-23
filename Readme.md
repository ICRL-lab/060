# Mobile Price Prediction

## Introduction

The aim of this project is to perfrom Mobile Price prediction using multiple ML algorithms and DL using custom ANN.

## Dataset

 A mobile price prediction data set was used for the project. The dataset was collected from Kaggle that was basically a csv file with the various columns of attributes. The details of the used data set are following:

- Name: Mobile-Price-Prediction(Kaggle)
- Mode: Tabular Data
- Number of Samples: 807
- Number of Features:7
- Type: Regression
- Number of Classes: 0

## Preprocessing

The preprocessing steps of the proposed project are the following:
**1. Feature Identification**
**Numerical Features:** Identified by selecting columns with data types int64 or float64.
**Categorical Features:** Identified by selecting columns with the data type object.
**2. Pipeline for Numerical Features**
**Imputation:** Handles missing values using the SimpleImputer with the strategy set to 'mean'. This replaces missing values with the mean of the respective column.
**Scaling:** Normalizes the numerical features using the StandardScaler, which standardizes features by removing the mean and scaling to unit variance.
 **3.Pipeline for Categorical Features**
**Imputation:** Handles missing values using the SimpleImputer with the strategy set to 'most_frequent'. This replaces missing values with the most frequently occurring value in the column.
**Encoding:** Converts categorical features into a one-hot encoded format using OneHotEncoder. The handle_unknown='ignore' parameter ensures that any new categories encountered during transformation are ignored, preventing errors.

## Models

For the mobile price prediction following models were trained with the tuned hyper parameters:

- PCA
    -	n_components=5
- LinearRegression
- Ridge
- Lasso
- DecisionTreeRegressor
- RandomForestRegressor
- SVR
- Custom ANN:
    -	Epochs:10000
    -	Five Linear layers
    -	Loss: MSEloss
    -	Optimizer: Adam (lr=0.001)

    ## Results

    The results of the trained model are the following:


| Model                  | MAE         | MSE           | R2       |
|------------------------|-------------|---------------|----------|
| PCA                    | 9904.482    | 315661433.375 | 0.436635 |
| Linear Regression       | 9907.580107 | 315661200.8   | 0.436636 |
| Ridge Regression        | 9904.482438 | 315661400.8   | 0.436635 |
| Lasso Regression        | 9907.228152 | 315661200.8   | 0.436636 |
| Decision Tree           | 140.963307  | 1.229908e+06  | 0.997805 |
| Random Forest           | 1189.549406 | 1.688650e+07  | 0.969862 |
| Support Vector Regression (SVR) | 13216.376798 | 7.158032e+08  | -0.277502 |
| Custom ANN              | 5822.8037   | 1.00609104e+08 | 0.7632  |
	

<br>
<img src = images/image2.png>


<br>

<img src = images/image1.png>