# EDA_Elite_Sports_Cars_FM1112
EDA on Sports Car Dataset analyzing features like Engine Size, Horsepower, Price, Mileage & Market Demand. Includes data cleaning, outlier detection, encoding, scaling, and visualizations (histogram, scatter, heatmap) to uncover trends, correlations, and insights for predictive modeling.

#### Dataset Name: sports_car_dataset.csv
##### Rows: 219
##### Columns: 13

#### Column Details:
##### 1] Brand – Name of the car manufacturer (e.g., Nissan, Ferrari, Bugatti).
##### 2] Year – Manufacturing year of the car.
##### 3] Continent – Region where the brand originates (Asia, Europe, USA).
##### 4] Engine_Size – Engine capacity (in liters).
##### 5] Horsepower – Engine power output in HP.
##### 6] Torque – Rotational force produced by the engine (Nm).
##### 7] Weight – Vehicle weight in kilograms.
##### 8] Top_Speed – Maximum achievable speed (km/h).
##### 9] Acceleration_0_100 – Time taken to accelerate from 0 to 100 km/h (seconds).
##### 10] Fuel_Type – Type of fuel used (Petrol, Diesel, Electric).
##### 11] Price – Market price of the car (in USD).
##### 12] Mileage – Fuel efficiency (km/l or equivalent).
##### 13] Market_Demand – Demand level of the car (Low, Medium, High).

 This dataset provides a comprehensive view of car performance, economy, and demand patterns for EDA and predictive modeling.

 #### Key Findings & Insights

##### Insights
Several numeric columns (like Engine_Size, Horsepower, Top_Speed) had missing values which were imputed using mean.
Negative or invalid entries (e.g., negative Engine_Size or Acceleration) were detected and corrected.
Outliers were detected mainly in Engine_Size, Horsepower, Weight, and Acceleration_0_100.
These were treated using capping and removal methods.
Text columns (like Brand, Fuel_Type, Market_Demand) were standardized to lower case for uniformity.
Strong positive correlation between Engine_Size and Horsepower.
Mild negative correlation between Price and Mileage (indicating higher-priced cars are less fuel-efficient).
Europe dominates in high-performance car production.
Scatter plots and pairplots showed clusters for different fuel types.
Stacked bar charts indicated that Market Demand is higher for Electric and Diesel models in recent years.

##### Trends and Anomalies
###### Trends:
###### •Newer models (post-2015) show higher horsepower and engine sizes with improved acceleration.
###### Electric cars are becoming more common after 2010 with increasing top speeds and price.
###### Mileage tends to decrease as price and engine size increase, showing a trade-off between power and efficiency.
###### European brands dominate in premium and high-performance segments.

###### Anomalies:
####### Some entries had negative or unrealistic values (e.g., negative Engine_Size, very high Top_Speed), which were corrected or treated.
####### A few outliers still exist in Horsepower and Weight, likely representing rare supercars.

##### Relationships Between Features
####### Engine_Size ↔ Horsepower: Strong positive correlation — larger engines produce more power.
####### Price ↔ Mileage: Negative correlation — expensive cars are less fuel-efficient.
####### Top_Speed: Moderate positive relationship — higher torque often improves top speed.
####### Year ↔ Electric Models: Positive trend — newer cars are more likely to be electric.
####### Market_Demand ↔ Fuel_Type: Electric and Diesel models show higher market demand in recent years.
####### Engine_Size ↔ Horsepower: Strong positive correlation — larger engines produce more power.
####### Price ↔ Mileage: Negative correlation — expensive cars are less fuel-efficient.
####### Torque ↔ Top_Speed: Moderate positive relationship — higher torque often improves top speed.
####### Year ↔ Electric Models: Positive trend — newer cars are more likely to be electric.
####### Market_Demand ↔ Fuel_Type: Electric and Diesel models show higher market demand in recent years.

##### Implications for Modeling
####### Highly correlated features like Engine_Size and Horsepower may cause multicollinearity — one can be removed.
####### Fuel_Type, Market_Demand, and Continent are good categorical predictors for price and mileage.
####### Extreme values in Horsepower, Weight, and Acceleration_0_100 can bias regression models — capping or robust models (like Random Forest) are preferable.
####### Since numeric features vary widely in range (e.g., Price vs Engine_Size), normalization or standardization is needed for models like KNN or SVM.
####### Use Label Encoding for ordinal data and One-Hot Encoding for nominal features to ensure compatibility with ML algorithms.
####### Imputation using mean (numeric) and mode (categorical) ensures no data loss, supporting better model performance.
####### The cleaned dataset is now suitable for predictive modeling — particularly Price Prediction or Market Demand Classification.

##### Conclusion
The EDA of the Sports Car Dataset revealed key insights into performance, pricing, and demand trends. Strong correlations exist between engine size, horsepower, and price, while higher-priced cars show lower mileage. After cleaning, scaling, and encoding, the dataset is ready for accurate predictive modeling.
