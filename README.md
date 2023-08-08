# Prediction-of-Product-Sales

## Author: Osmayda Nino

# Business problem: 
The goal is to help the retailer understand the properties of products and outlets that play crucial roles in predicting sales.

## Data: 
https://drive.google.com/drive/u/1/folders/1igjqLYVDiIEkvvvNPx4fRKXO5ZwvnFDo
## Source: https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/

# Data Dictionary for this dataset:


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
    - The higher the item MRP (maximum retail price) the higher the predicted sales
      
- Outlet_Type_Grocery Store
    - A higher number of outlet type grocery stores decreases predicted sales
      
- Outlet_Type_Supermarket Type3
  
    - as the number of outlet type supermarket type 3 increases the higher the sales predicted

## **Local Explanations**
**High Sales**
![image](https://github.com/Osmayda/Prediction-of-Product-Sales/assets/129660519/0f69ee9d-74ba-49d8-b474-15e7fe744f1d)
**Interpretation**
- a significant push toward the right indicates higher sales
- 265.2 of a list price of a product goes to sales
- major features: Outlet_Type_Grocery Store and Item_Visibility


- Outlet size is the feature that is driving the sales downward.

**Low Sales**
![image](https://github.com/Osmayda/Prediction-of-Product-Sales/assets/129660519/20b5bb6f-61d6-46c1-8d78-452e281efdb2)
**Interpretation**
- a significant push to the left indicating lower sales
- 32.06 of a list price of a product goes to sales
- major feature: Outlet_Type_Supermarket Type3
- Outlet_Size_Small is the feature that is driving sales up


**LIME Tabular Explanation**

**High Sales**

![image](https://github.com/Osmayda/Prediction-of-Product-Sales/assets/129660519/49ba61d4-9c3d-4e90-be64-77e5dcf7f981)
![image](https://github.com/Osmayda/Prediction-of-Product-Sales/assets/129660519/bd865f8e-499f-4c16-bd1c-e684712d260c)
- Predicted Value is 5198.55. 

Interpreting our Features with the 'negative' and 'positive' bar chart

    - Negative (lower sales). These are features that contribute to lower sales. Some of the features include:
        - Outlet_Type_Supermarket Type1
        - Item_Type_Soft Drinks
        - Outlet_Size_High
    - Positive (higher sales). These are features that contribute to higher sales. Some of the features include: 
        - Outlet_Type_Grocery Store
        - Item_MRP
        - Item_Type_Canned

**Low Sales**

![image](https://github.com/Osmayda/Prediction-of-Product-Sales/assets/129660519/101c9861-915b-4532-978a-e54852c5a306)
![image](https://github.com/Osmayda/Prediction-of-Product-Sales/assets/129660519/7911afb9-7e40-4bb3-b2cb-95e67128841f)


- Predicted Value is 723.46. 

Interpreting our Features with the 'negative' and 'positive' bar chart

    - Negative (lower sales). These are features that contribute to lower sales. Some of the features include:
        - Item_MRP
        - Outlet_Type_Supermarket Type3
        - Item_Type_Starchy Foods
    - Positive (higher sales). These are features that contribute to higher sales. Some of the features include: 
        - Outlet_Type_Grocery Store
        - Outlet_Type_Supermarket Type1
        - Item_Type_Frozen Foods
        
## For further information contact:
For any additional questions, please contact osmaydanino@hotmail.com
