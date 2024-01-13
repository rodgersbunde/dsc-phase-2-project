# Real Estate Agency
Predictive Modelling for House Prices in King County



![awesome](https://images.unsplash.com/photo-1560518883-ce09059eeffa?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8Mnx8aG91c2UlMjByZW50YWx8ZW58MHx8MHx8fDA%3D)


### Overview
The primary goal of the project is to build a predictive model that can estimate/predict the house prices in King County, Washington, USA based on its features, provide valuable insights through comparative market analysis to facilitate informed decision making. The target audience includes real estate analysts, real estate investors, data scientists, machine learning practioners,financial institutions, potential home buyers and potential tenants.
Business and Data Understanding

### Stakeholder Audience
The primary stakeholders for this project are real estate professionals, potential homebuyers, and sellers in King County. The predictive model aims to assist real estate professionals in estimating property values more accurately, empowering them to make well-informed decisions. Homebuyers and sellers can benefit from a deeper understanding of the factors influencing house prices, aiding in setting realistic expectations and facilitating informed transactions.

### Data Understanding
For this project, we will be using the King County House Sales dataset, which contains information about house sales in a northwestern county. The dataset includes various features such as the number of bedrooms, bathrooms, living area size, condition of the house, presence of additional amenities, and more.
The dataset has 20 columns and over 21500 records, covering house sales between May 2014 and May 2015. The data is suitable for the project because it provide relevant information about the features that affect the house prices in King County. The dataset was obtained from GitHub.
The King County House Sales dataset contains the following columns;
- Price - Sale price (prediction target),
- bedrooms - Number of bedrooms,
- bathrooms - Number of bathrooms,
- sqft_living - square footage of living space in the home,
- sqft_lot - square footage of the lot,
- floors - Number of floors (levels) in house,
- view - Quality of view from house,
- condition - How good the overall condition of the house is. Related to maintenance of house,
- grade - Overall grade of the house. Related to the construction and design of the house,
- sqft_above - Square footage of house apart from basement,
- sqft_basement - square footage of the basement,
- yr_built - Year when house was built,
- yr_renovated - Year when the houses were renovated,
- zipcode - ZIP Code used by the United States Postal Service,
- sqft_living15 - The square footage of interior housing living space for the nearest 15 neighbours.
- sqft_lot15 - The square footage of the land lots of the nearest 15 neighbours, and
- sell_yr - Date the house was sold.

For our analysis we decided to choose the following columns price, bedrooms, bathrooms, sqft_living condition, yr_built, sell_yr and house_age of which are expected to have an impact on the price of the house.

### Modeling
Regression Results
Modeling
In this section, a comprehensive approach to building and evaluating linear regression models for predicting house prices is presented. Both simple linear regression and multiple linear regression models are explored, employing carefully selected features from the earlier sections of the notebook.
Simple Linear Regression
The initial analysis involves a simple linear regression model to establish a baseline understanding of the relationship between the target variable, 'price,' and the chosen predictor, 'sqft_living.' The graph illustrates a clear linear relationship, and the baseline model's summary reveals key statistics:
- Baseline Model Summary:
 - R-squared: 0.493
 - Adjusted R-squared: 0.493
 - F-statistic: 2.097e+04
 - P-value (F-statistic): 0.00
 - Coefficients:
 - Constant: -43988.892194
 - sqft_living: 280.863014
The R-squared value indicates that sqft_living explains 49.3% of the variation in price. Both coefficients have statistically significant p-values (0.000), affirming the linear relationship's significance.

#### Multiple Linear Regression
To enhance predictive accuracy, multiple linear regression models are constructed, considering additional features such as 'bathrooms,' 'house_age,' and 'condition.' A detailed feature analysis identifies multicollinearity issues, leading to the selection of a robust model.

### Model 1
- Model Features:
- bathrooms, sqft_living, house_age, condition
##### Model Summary:
- R-squared: 0.454
 - Adjusted R-squared: 0.453
- F-statistic: 3473.0
- P-value (F-statistic): 0.00
#### Coefficients:
- Constant: 11.8221
- bathrooms: 0.1384
- sqft_living: 0.0003
- house_age: 0.0037
- condition: 0.0119

#### Evaluation Metrics:
- MAE: 0
- RMSE: 0.4

### Model 2
•Model Features:
•bedrooms, sqft_living, bathrooms, house_age, condition
#### Model Summary:
- R-squared: 0.465
- Adjusted R-squared: 0.465
- F-statistic: 2913.0
- P-value (F-statistic): 0.00
#### Coefficients:
- Constant: 11.9325
- bedrooms: -0.0765
- sqft_living: 0.0004
- bathrooms: 0.1572
- house_age: 0.0039
- condition: 0.0166
#### Evaluation Metrics:
- MAE: 0
- RMSE: 0.3

The selection of Model 2 is justified based on its higher R-squared value (46.5%), indicating a better explanation of variance in the dependent variable.

### Regression Results
Model Diagnostics

Ensuring the selected model adheres to linear regression assumptions, diagnostic plots are generated for key features:
- sqft_living: Residuals show homoscedasticity, normality, and linearity.
- condition: Residual analysis confirms the assumptions.
- bathrooms: The diagnostic plots exhibit conformity to linear regression assumptions.
- house_age: Residual plots indicate satisfactory adherence to assumptions.
- bedrooms: The model meets the assumptions of normality, homoscedasticity, and linearity.
#### Results for Model 2
The model demonstrates promising results:
- Prob (F-statistic): 0.000, below the standard alpha of 0.05.
- R-squared: 0.465, explaining 46.5% of housing price variability.
- Coefficients: Significant p-values for all coefficients.
#### Interpretation of Coefficients:
- Bedrooms: Negative impact on price.
- Sqft_living: Positive impact on price.
- Bathrooms: Positive impact on price.
- House_age: Positive impact on price.
- Condition: Positive impact on price.

The model's confidence intervals provide a nuanced understanding of the coefficient estimates.

### Conclusion
The chosen model (Model 2) explains 46.5% of the variability in house prices. It incorporates features such as bedrooms, square footage, bathrooms, house age, and condition. Model diagnostics confirm adherence to regression assumptions, including normality, homoscedasticity, and linearity. The detailed results provide stakeholders with a nuanced understanding of the model's predictive capabilities.

### Future Considerations
- Continuous Retraining: Given the dynamic nature of the real estate market, periodic retraining of the model with updated data is essential to maintain accuracy.

- Regional Variables: Incorporating localized factors such as proximity to schools and transportation can enhance the model's predictive capabilities for the unique characteristics of King County.

- Validation and Testing: Regularly comparing model predictions with actual prices and refining the model based on real-world performance ensures ongoing relevance and reliability.

- Alternative Models: Exploring non-linear models and polynomial regression may capture more complex relationships not accounted for in linear models.

- Economic Factors: Analyzing how economic recessions or changes in interest rates influence house prices can provide valuable insights into market dynamics.


