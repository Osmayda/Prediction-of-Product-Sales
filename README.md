# Prediction-of-Product-Sales

## Author: Osmayda Nino

# Business problem: 
The goal is to help the retailer understand the properties of products and outlets that play crucial roles in predicting sales.

## Data: 
https://drive.google.com/drive/u/1/folders/1igjqLYVDiIEkvvvNPx4fRKXO5ZwvnFDo
## Source: https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/

## Data Dictionary for this dataset:
![image](https://github.com/Osmayda/Prediction-of-Product-Sales/assets/129660519/3424c24c-a9be-46af-856d-7f1c11ddfa5d)

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
![image](https://github.com/Osmayda/Prediction-of-Product-Sales/assets/129660519/7517d1de-97ad-4d41-b57b-b813773ed4d9)
**Interpretation**
- a significant push toward the right indicates higher sales
- the higher the item_MRP (Maximum Retail Price) of the product the higher the revenue

- major features that drive the price up are:
    - the item was not sold at Outlet_Type_Grocery Store
    - the item sold had a visibility of 0.02588


**Low Sales**
![image](https://github.com/Osmayda/Prediction-of-Product-Sales/assets/129660519/f1ede1c8-9d10-415e-a803-c5747f993070)
**Interpretation**
- a significant push to the left indicating lower sales
- items with lower MRP (Maximum Retail Price) bring in less revenue

- major features that drive sales down are: 
    - item was not sold at an Outlet_Type_Supermarket Type3
    - item MRP was the lowest at 32.06 Rupees


**LIME Tabular Explanation**

**High Sales**

![image](https://github.com/Osmayda/Prediction-of-Product-Sales/assets/129660519/49ba61d4-9c3d-4e90-be64-77e5dcf7f981)
![image](https://github.com/Osmayda/Prediction-of-Product-Sales/assets/129660519/bd865f8e-499f-4c16-bd1c-e684712d260c)

**Interpretation**

According to LIME, these features negatively affected the sales of the highest-priced item sold.

   - the item was not sold at an Outlet_Type_Supermarket Type1
   - the item is not sold at an Outlet_Size_High
   
The item with the highest Item_MRP did not have these features: 
    -Item_Type_Soft Drinks
   - Item_Fat_Content_Regular
   - Item_Type_Household
   
According to LIME, these features increased the sales of the highest price item sold.  
   - the item was not sold at Outlet_Type_Grocery Store but rather that it was sold at an Outlet_Type_Supermarket Type1
   - the Item_Visibility was 0.03
   - Item_MRP was the highest at 265.22 Rupees
   - it is an Item_Type_Canned

**Low Sales**

![image](https://github.com/Osmayda/Prediction-of-Product-Sales/assets/129660519/101c9861-915b-4532-978a-e54852c5a306)
![image](https://github.com/Osmayda/Prediction-of-Product-Sales/assets/129660519/7911afb9-7e40-4bb3-b2cb-95e67128841f)

**Interpretation**

According to LIME, these features negatively affected the sales of the lowest-priced item sold
  - Item_MRP was the lowest at 32.06 Rupees
  - item was not sold at an Outlet_Type_Supermarket Type3
        
The item with the lowest Item_MRP did not have these features: 
   - item was not an Item_Type_Seafood
   - item was not an Item_Type_Snack Foods
   - item was not an Item_Type_Hard Drinks
   - item was not an Item_Type_Breakfast
   - item was not an Item_Type_Solf Drinks
        
According to LIME, these features contributed to higher sales of the lowest-priced item sold

   - item was not sold at Outlet_Type_Grocery Store
   - item was not sold at Outlet_Type_Supermarket Type2
   - item was sold at Outlet_Type_Supermarket Type1
        
## For further information contact:
For any additional questions, please contact osmaydanino@hotmail.com
