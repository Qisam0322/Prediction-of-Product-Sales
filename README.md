# Prediction-of-Product-Sales
## Maximizing Retail Profits through Data-Driven Sales Forecasts and Strategic Insights

**SAM QI**: 

### Business problem:

Efficient inventory management, optimal pricing strategies, and strategic product placement are paramount for retail store suppliers aiming to maximize their profits. However, making informed decisions in these areas can be challenging without precise product sales forecasts and strategic insights.

### Data:
Big Mart Sales data
https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/


### Methods 
#### Data Preparation

- 17.17% of data is missing for 'Item Weight'. Null values are missing at random. Decided to use Median to fill Nulls.
- 28.28% of data is missing for 'Outlet Size'. Null values are missing at random. Decided to use 'MISSING' to fill Nulls.
- Fixed Inconsistency in 'Item Fat Content'.




## Results

### Visual 1 Heatmap of Features Correlations

![heatmap new](https://github.com/Qisam0322/Prediction-of-Product-Sales/assets/144630065/02ed5fb5-f0b5-46d9-80f7-cb69a06d452d)

From the graph, Product store sales and Max retail price have a positive correlation of 0.57. However, the correlation is moderate. There is no noticeable correlation (>0.3 or <-0.3) other than Product store sales and MRP.

### Visual 2 Product Counts by Categories groupby LowFat vs Regular

![Count of product by categories with LowFat:Regular](https://github.com/Qisam0322/Prediction-of-Product-Sales/assets/144630065/cc23b880-7f9a-4352-8192-013c85e6cb20)

The count plot provides valuable insights into the distribution of product counts within each category, groupby by LowFat and Regular. Overall, the company tends to stock a higher quantity of low-fat products compared to regular ones. However, it's noteworthy that in the 'meat' and 'breakfast' categories, the company maintains a larger inventory of regular products as opposed to low-fat alternatives.

#### Visual 3 Product Count by Categories

![Product count by categories](https://github.com/Qisam0322/Prediction-of-Product-Sales/assets/144630065/9c9eb747-1b64-47fc-bd21-d1a2d2d3c913)

The count plot above shows the product counts for each category. 'Fruit and vegetable' and 'snack foods' have the highest counts of product and 'seafood' has the lowest count of product.

## Model

### Machine Learning Using the Following Models:
    - Linear Regression Model
    - Decision Tree Regressor Model
    - Tuned Decision Tree Regressor Model
    - Random Forest Regressor Model
    - Tuned Random Forest Regressor Model
    
## Models Evaluated & Results

- Linear Regression Model (Testing Set):
  - R^2: -1.442820300359156e+22
  - MAE: 2065461996953278.5
  - MSE: 6.752807031244359e+31
  - RMSE: 8217546489825512.0

- Decision Tree Regressor Model (Testing Set):
  - R^2: 0.186
  - MAE: 41512.219
  - MSE: 3809835283.133
  - RMSE: 61723.863

- Tuned Decision Tree Regressor Model (Testing Set):
  - R^2: 0.462
  - MAE: 34610.985
  - MSE: 2517885802.26
  - RMSE: 50178.539

- Random Forest Regressor Model (Testing Set):
  - R^2: 0.56
  - MAE: 31872.362
  - MSE: 2061515521.69
  - RMSE: 45403.915

- Tuned Random Forest Regressor Model (Testing Set):
  - R^2: 0.563
  - MAE: 31998.943
  - MSE: 2044264641.827
  - RMSE: 45213.545
