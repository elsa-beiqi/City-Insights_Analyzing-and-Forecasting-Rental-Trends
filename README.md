# Data-Exploration_Analyzing-Housing-and-Visit-Patterns

## Project Overview
This project explores various urban metrics, including average rent, population size, household data, and both physical and virtual visit trends across multiple cities. The goal is to understand and visualize key patterns and relationships within the data, as well as to gain insights into specific Metropolitan Statistical Areas (MSAs). Additionally, the project applies time series forecasting models to predict future trends in average rent:
1. Pattern Identification for Average Rent: Initial forecasting models (ARIMA and Exponential Smoothing) focus solely on historical rental price patterns.
2. Enhanced Forecasting with Additional Variables (i.e. independent variables): The final model (Random Forest Regression) incorporates additional independent variables (population, household data, and visit trends) to enhance prediction accuracy.

The dataset includes the following columns:
1. City: The name of the city/MSA
2. Average Rent: Average rental prices in the MSA
3. Total Population: Total population within the MSA
4. Total Household: Total number of households
5. Physical Visits: Count of physical visits
6. Virtual Visits: Count of virtual (online) visits

## Results and Observations
### Correlation Analysis
Correlation Coefficients: 
Examined correlations between average_rent and other features, finding notable associations with variables such as total_population, physical_visits, and virtual_visits. This analysis helped prioritize features for predictive modeling by highlighting those most closely related to rental prices.

## Forecasting Models
1. ARIMA Model
The ARIMA model was chosen for its ability to capture linear trends and seasonality in time series data.
While ARIMA effectively captured general trends, the discrepancy between training and testing RMSE suggests it might not fully generalize, particularly if there are non-linear relationships in the data that it cannot easily capture.

2. Exponential Smoothing Model
Exponential Smoothing was selected for its strength in handling seasonality by weighting recent observations more heavily. This approach is beneficial for data with seasonal or cyclic patterns, as it emphasizes recent trends while smoothing out past fluctuations.
It performed reliably by focusing on the seasonality and general trend without overfitting to specific data points.

3. Random Forest Regression
A Random Forest Regressor was used to capture complex and potentially non-linear relationships between average_rent and multiple features (total_population, total_household, physical_visits, and virtual_visits).
It offered flexibility in capturing complex feature interactions but may have overfit the training data, as evidenced by the high test RMSE.

All three models forecasted upward trends in rental prices, consistent with historical data.
