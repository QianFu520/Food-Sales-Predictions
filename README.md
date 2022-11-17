# Food-Sales-Predictions
 ![Food](food.png)
 ## Sales Prediction for Food Items Sold at Various Stores
 
 **Qian Fu**
 
 ## Business problem:
 
 The goal of this is to help the retailer understand the properties of products and outlets that play crucial roles in increasing sales.

## Data Source:

Original data source from https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/

## Data Dictionary

![dictionary](dictionary.png)

## Part 1: Data Exploring and Cleaning

### Overview of the tasks done in this part:

•	Original, there were 8523 rows and 12 columns.

•	Dropping unnecessary columns and duplicated rows.

•	Addressing missing values in two columns.

•	Fixing inconsistencies.

•	Obtaining the summary statistics of numerical columns.

### Results.

After cleaning, we have a dataset with 8523 rows and 9 columns which including:

•	4 numerical features: Item_weight, Item_Visibility, Item_MRP, and Item_outlet_sales.

•	2 ordinal features: Item_fat_content and Outlet_size.

•	3 nominal features: Item_type, outlet_location_type, and Outlet_type.

## Part 2: Visualizations for Exploratory Data Analysis (EDA)

### Overview of the tasks done in this part:

	Univariate Visuals: Explore the distribution of each column of data.

•	Bar charts: plotting categorical frequencies.

•	Histograms: plotting continuous distribution.

•	Boxplots: checking any outliers.

	Multivariate Visuals: Explore relationships between variables and differences in groups.

•	Heatmap: looking for correlations between each feature.

•	Scatterplot: checking correlations between numerical features and item sales(target).

•	Bar charts: grouping by categorical columns based on average item sales.

### Results

**Distribution of the Item Sales**

![sales](itemsales.png)

This histogram shows that the majority of the sales are around $2000.

**Are there any outliers in item sales?**

![outliers](outliers.png)

we can see that there are a lot outliers above $6000.

**The average item sales based on the outlet's type, location, and size.**

![outlet](outlet.png)

we can see that the outlet type plays crucial role in increasing sales.

## Part 3: Explanatory Visualizations Tell a Story.

**In this part, through three questions, we can deeply understand how properties of products and outlets that play crucial roles in increasing sales.**

**Q 1: How food type and fat type impact the sales?**

![type](typefat.png)

Answer: From this barchart we can see that:

•	Some food types have higher sales on the food with low fat. Ex: soft drinks, snack, breakfast.

•	Some food types have higher sales on the food with regular fat. Ex: dairy, seafood, meat.

•	Overall, food with low fat have higher sales.

•	Only seafood has a significant sale’s difference on the different fat type.

**Q 2: Does Outlet Type makes big difference in Sales?**

![type](outlettype.png)

Answer: From this pie chart we can see that:

•	Supermarket type3 contributes almost half of the sales.

•	Supermarket type 1 and type 2 have no big difference on sales.

•	Grocery store has very little sales compared to other three outlet types.

**How the outlet size and outlet location distribute in each outlet type?**

![type](sizetype.png)

Answer: From these pie charts we can see that:

•	For the supermarket type 3 outlet, which makes the most sales, its outlet size is all medium and location type is all Tier 3. Same as supermarket type 2 outlet.

•	Supermarket type 1 outlet has all three outlet location types and outlet size types. But almost half of the outsize type is medium.

•	Grocery store type outlet makes much less sales compared to other 3 outlet types, but half of its outlet location type and outlet size type are Tier3 and medium.

•	Overall, outlets with medium size and Tier 3 location tend to make more sales.

## Part 4: Machine Learning: Training Models to Make the Best Prediction

**Overview of the tasks done in this part:**

In this part, data cleaning is done in two parts: before data spilt and after data spilt to prevent data leakage. After data spilt, columntransformer is created for getting data ready for machine learning. Last, training different models to find out the best model to make the prediction.

**Maching Learning Using the Following Models:**

    - Linear Regression Model
    
    - Decision Tree Regressor Model
    
    - Tuned Decision Tree Regressor Model
    
    - Random Forest Regressor Model
    
    - Tuned Random Forest Regressor Model
    
**Models Evaluated & Results:**

* Linear Regression Model (Testing Set):
  * R^2 = 0.56
  * MAE = 805.6
  * MSE = 1198348.6
  * RMSE = 1094.7
  
* Decision Tree Regressor Model (Testing Set):
  * R^2 = 0.115
  * MAE = 1077.609
  * MSE = 2441050.699
  * RMSE = 1562.386
  
* Tuned Decision Tree Regressor Model (Testing Set):
  * R^2 = 0.595
  * MAE = 738.317
  * MSE = 1118185.973
  * RMSE = 1057.443

* Random Forest Regressor Model (Testing Set):
  *  R^2 = 0.547
  * MAE = 773.579
  * MSE = 1249404.569
  * RMSE = 1117.768

* Tuned Random Forest Regressor Model (Testing Set):
  * R^2 = 0.547
  * MAE = 775.755
  * MSE = 1249085.757
  * RMSE = 1117.625
  
**The Final Model Chosen was `Linear Regression Model`.**

  * For the testing set on the model, `56.6%` of the variance in y was explained by x.
    
  * The Mean Absolute Error was off by about `$805.567`.
    
  * The Mean Squared Error was `$1198348.589`.
    
  * The Root Mean Squared Error had a calculation of `$1094.691`.
  
we can see that comparing to other models, this model performances the highest R2 score and lowest RMSE score. So, using this model to make prediction of the food sales based on the properties of the food and the outlet type with different outlet location and outlet size can be considerd more reliable. 

## Recommendations

* From properties of food and outlet:
  * Overall, most of the food with low fat make more sales. But for some food type, for example, seafood with regular fat is more popular. So, we can consider the food type when we decide to adjust the fat type of the food to increase the sales.
  * The list price of the product has a positive correlation with the sales. we can consider to increase some popular items' list price to increase the sales.
  * For the outlet, we can choose supermarket type 3 outlet type with location type is Tier3 and medium outlet size. 
  
 * Model Performance
   * Overall, the best model is definitely the Linear Regression Model. There was still some bias in the model, but by far it outperformanced the other models were trained here.
   
## Limitations & Next Steps

From here, we can use the insights from the visuals to decide what to change or adjust to make a increasement on the sales. But I believe there are other factors that make influence of the sales. In reality, we can actually go to the store that makes the best sales to investigate what they have done to increase the sales. For example, a great customer service definitely help to increase the sales. 

## For Further Information

For any additional questions, please contact:

* Qian Fu (Data Scientist)

* qfu885612@gmail.com


