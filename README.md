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

# Explaining Models with SHAP
![summary_plot_bar_rf_reg](https://github.com/Osmayda/Prediction-of-Product-Sales/assets/129660519/70d677a2-c7ef-4b25-acf3-92110339c53d)
## SHAP vs. Feature Importances
- SHAP and Feature Importances show the same top 5 features

**Similarities:**
- Both the SHAP bar plot and feature importances show Item_MRP and Outlet_Type_Grocery Store as the top features

**Differences:**
- The SHAP bar plot shows Outlet_Type_Supermarket Type3 as 3rd most important feature while the same feature ranks 4th on the Feature Importances
- Item_Visibility ranks 4th on the SHAP bar while it ranks 3rd on the Feature Importances

![2 summary_plot_dot_rf_reg](https://github.com/Osmayda/Prediction-of-Product-Sales/assets/129660519/50f798b7-bf93-4b11-b8ec-bbe191ceb9af)

**Summary Dot Plot Interpretation - Top 3 most important features**
- Item_MRP
    - higher counts of Item MRP increases predicted sales
      
- Outlet_Type_Grocery Store
    - A higher number of outlet type grocery stores decreases predicted sales
      
- Outlet_Type_Supermarket Type3
  
    - As the number of outlet type supermarket type 3 increases the higher the sales predicted

## For further information contact:
For any additional questions, please contact osmaydanino@hotmail.com
