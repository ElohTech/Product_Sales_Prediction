# Product_Sales_Prediction

Predicting the Number of Food Items Sold

## The analysis includes inspecting, cleaning, and modeling the dataset to predict the number of food items sold

#### Author: Phuong Huynh

### Business problem:
We will predict the number of food items sold at various stores by understanding how different properities/features of products and outlet stores play a crucial role in items sold. 

### Data:
- Item_Identifier	
- Item_Weight	
- Item_Fat_Content	
- Item_Visibility	
- Item_Type	Item_MRP	
- Outlet_Identifier	
- Outlet_Establishment_Year	
- Outlet_Size	Outlet_Location_Type	
- Outlet_Type	Item_Outlet_Sales

## Methods
- We view, inspect, and clean the data
- The next step is to fill in missing data
- For numerical columns, we fill in with the median values
- For categorical columns, we fill in with one hot encoder
- For ordinal columns, we fill in with ordinal encoder
- The dataset is then put through different models to predict product sales

## Results:


Here are examples of some of the data visualizations
### Visual 1: Item Type Count
![image](https://github.com/pahtech/Product_Sales_Prediction/assets/121314458/a7b5a260-735c-4914-83e6-df6532c3ac55)

- This shows the categories of items that were sold





### Visual 2: Correlation Heatmap
![image](https://github.com/pahtech/Product_Sales_Prediction/assets/121314458/93dac4e4-f41c-40c7-8104-85b68607de81)


- This heatmap shows the correlation between the features in the dataset. It will help us understand which feature is more important when trying to predict the target, Item_Outlet_Sales.

## Model
Our models include a linear regression model, and default and tuned random forest models using GridSearchCV.

- Because our target is a number (item sales), we will use regression metrics to evaluate the performance of each model.
- Important metrics for regression models include  Mean Absolute Error (MAE), Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and R2 (R^2).
- The R2 score tells us what percentage of the variation in the target the model can explain. We will use this for our primary metric.
- The RMSE tells us how far on average we can expect our real value is from our predicted value. It gives the units in the same unit (in $) as our target.

  
## Model Evaluation
 Our models have the following results:
- The Linear Regression Model is able to correctly predict the sales on an average of $1,093 off from the true value based on its RMSE. 
- The Default Random Forest Model is able to correctly predict the sales on an average of $1,104 from of the true value based on its RMSE. 
- The Tuned Random Forest Model is able to correctly predict the sales on an average of $1,047 off from the true value based on its RMSE.
- Of the three models, we will also see that the Tuned Random Forest Model did the best on the test dataset because it has the highest R2 score.

## Recommendations:
We recommend the use of the Tuned Random Forest Model. 

## Limitations & Next Steps
To achieve a higher metric, the model can include more hyperparameters and their options in its tuning. 

### For further information
For any additional questions, please contact Phuong Huynh.
