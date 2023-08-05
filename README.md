# Prediction-of-Product-Sales
## Author: Osmayda Nino

# Business problem: 
The goal is to help the retailer understand the properties of products and outlets that play crucial roles in predicting sales.

## Data: 
https://drive.google.com/drive/u/1/folders/1igjqLYVDiIEkvvvNPx4fRKXO5ZwvnFDo

## Methods
The data was preprocessed. Duplicates were removed, missing items were imputed using the median, creating a "missing" value for nulls counts, and inconsistencies were fixed. 
Exploratory Data Analysis was completed using histograms, box plots, and heatmaps. 
Linear and Decision Tree Models were used to analyze the data.

# Results
From the metric scores, we can see that the mean absolute Error for the Decision Tree is lower than the one from the linear model. 

# Project 1 revisited - Importances and Coefficients
## LinearRegression coefficient plot
![top_15_largest_coefficients](https://github.com/Osmayda/Prediction-of-Product-Sales/assets/129660519/206fc0db-3bef-49de-b5c0-e3d316f49077)

- **Top 3 Most Impactful Features**
    - Outlet_Type_Grocery store
        - If you add one Outlet type grocery store the predicted sales would reduce by 1607.678.
    - Outlet_Type_Supermarket Type3
        - If you add one Outlet_Type_Supermarket Type3 the predicted sales would increase by 1524.724.
    - Item_Visibility
        - If you add one Item_Visibility the predicted sales would decline by 425.370.
# Project 1 revisited - Feature Importances
![feature_importances](https://github.com/Osmayda/Prediction-of-Product-Sales/assets/129660519/3622c8a5-a0f2-4ca3-83a2-e70294d81fbb)
- Top 5 most important features
    - Item MRP
    - Outlet_Type_Grocery Store
    - Item_Visibility
    - Outlet_Type_Supermarket Type3
    - Item_Weight

## For further information contact:
For any additional questions, please contact osmaydanino@hotmail.com



