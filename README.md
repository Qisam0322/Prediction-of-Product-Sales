# Prediction-of-Product-Sales
## Maximizing Retail Profits through Data-Driven Sales Forecasts and Strategic Insights

**SAM QI**: 

### Business problem:

Efficient inventory management, optimal pricing strategies, and strategic product placement are paramount for retail store suppliers aiming to maximize their profits. However, making informed decisions in these areas can be challenging without precise product sales forecasts and strategic insights.

### Data:
Big Mart Sales data
https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/

For this dataset, there were 8523 rows and 12 columns.


### Methods 
#### Data Preparation

- 17.17% of data is missing for 'Item Weight'. Null values are missing at random. Decided to use Median to fill Nulls.
- 28.28% of data is missing for 'Outlet Size'. Null values are missing at random. Decided to use 'MISSING' to fill Nulls.
- Fixed Inconsistency in 'Item Fat Content'.
- For ordinal column 'Outlet_Size', categories order=NA,SMALL,MEDIUM,HIGH


## Results

### Visual 1 Heatmap of Features Correlations

![heatmap new](https://github.com/Qisam0322/Prediction-of-Product-Sales/assets/144630065/02ed5fb5-f0b5-46d9-80f7-cb69a06d452d)

From the graph, Product store sales and Max retail price have a positive correlation of 0.57. However, the correlation is moderate. There is no noticeable correlation (>0.3 or <-0.3) other than Product store sales and MRP.

### Visual 2 Product Counts by Categories groupby LowFat vs Regular

![Count of product by categories with LowFat:Regular](https://github.com/Qisam0322/Prediction-of-Product-Sales/assets/144630065/cc23b880-7f9a-4352-8192-013c85e6cb20)

The count plot provides valuable insights on the distribution of product counts within each category, groupby by LowFat and Regular. Overall, the company tends to stock a higher quantity of low-fat products than regular ones. However, it's noteworthy that in the 'meat' and 'breakfast' categories, the company maintains a larger inventory of regular products as opposed to low-fat alternatives.

### Visual 3 Product Count by Categories

![Product count by categories](https://github.com/Qisam0322/Prediction-of-Product-Sales/assets/144630065/9c9eb747-1b64-47fc-bd21-d1a2d2d3c913)

The count plot above shows the product counts for each category. 'Fruit and vegetable' and 'snack foods' have the highest counts of product and 'seafood' has the lowest count of product.

## Model

### Machine Learning Using the Following Models:
    - Linear Regression Model
    - Random Forest Regressor Model
    - Tuned Random Forest Regressor Model
    
## Models Evaluated & Results

- Linear Regression Model (Testing Set):
 - MAE = 804.048
 - MSE = 1,194,230.406
 - RMSE = 1,092.808
 - R^2 = 0.567

- Random Forest Regressor Model (Testing Set):
 - MAE = 767.081
 - MSE = 1,216,212.220
 - RMSE = 1,102.820
 - R^2 = 0.559

- Tuned Random Forest Regressor Model (Testing Set):
 - MAE = 728.426
 - MSE = 1,096,412.715
 - RMSE = 1,047.097
 - R^2 = 0.603

-Overall I would recommend using the tuned random forest model for prediction because the model has a higher R2 value on test data(R^2=0.603 rf > R^2=0.559 lr) and the model is less underfit than the default random forest model and less overfitting than the linear regression model. 

-The tuned random forest model on test data has a R-squared value of 0.603 indicating that about 60.3% of the variance in 'Outlet Sales' can be explained by the features we're using in our model. The model does a reasonably good job at predicting outlet sales based on the features we provided. However, there are still other factors not included in our model that affect the target. So, while it's decent, there's room for improvement.

-The tuned random forest model on test data has a RMSE of 1,047.097 indicating on average our prediction is off by about $1,047.
RMSE tends to penalize larger errors more. Test data has a RMSE of 1,047.097 which is higher than its MAE of 728.426 suggesting that there might be some predictions that are quite far off. 

## Visualizing Feature Importances and Coefficients
### Visualizing Coefficients
![visualizingcoeffi ](https://github.com/Qisam0322/Prediction-of-Product-Sales/assets/144630065/34477326-9c8c-4172-b31d-49ec9c22833f)
- Noticed there are 'huge' numbers even after multicollinearity has been addressed. 
- Products being in 'Outlet type supermarket type1' decrease product sales by 2,802,533,635,874,159.50
- Products being in Outlet store #018 decreased product sales by 2,028,310,560,894,618.75
- Products being in Outlet Type Supermarket Type2 decrease product sales by 1,970,907,249,834,724.50
- Other features that have large positive correlations with the targets are Outlet_Identifier_OUT013, Outlet_Establishment_Year,and Outlet_Size.

### Visualizing Feature Importances
![featureimportancesgraph](https://github.com/Qisam0322/Prediction-of-Product-Sales/assets/144630065/18fa5f2b-2db6-49a2-9ba2-81c8a69b1fda)

Top 5 important features our model used the most for predicting our target.
- Item_MRP
- Outlet_type_grocery store
- Outlet_Identifier_OUT027
- Outlet_Type_Supermarket Type3
- Outlet_Establishment_Year
- Other than the features above, other features seem to have been used 'less' by our model for predicting our target. 

## Recommendations:
### For Store product supplier:

- Regular seafood products have the highest average product store sales.
- MRP has a moderate positive correlation with Store Product sales. 
- 50% of the product sales are around $1000 to $3000 with the median being around $1900. 25% of product sales fall between $0 to $1000.
- OUTLET027 has the highest average store product sales.
- Supermarket Type 3 has the highest average store product sales.

## Limitations & Next Steps

Store product suppliers can use the insights from the visuals to make decisions on product replacement, and inventory management, and refine pricing strategies to maximize product sales. 

### For further information


For any additional questions, please get in touch with **qi.sam0322@gmail.com**

