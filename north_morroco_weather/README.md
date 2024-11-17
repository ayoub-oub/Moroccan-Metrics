
## Project Overview

The project showcases a comprehensive and practical approach to analyzing and forecasting weather data in Morocco. After obtaining data from NOAA for all 21 Moroccan weather stations spanning from 1990 to the present, we focused on the station in Melilla, which provided the most extensive dataset. Using this data, we implemented both a SARIMA model and a Random Forest Regressor to develop an accurate model for predicting temperature trends.

## Local Setup
### Installation
To follow this project, please install the following locally:

+ JupyerLab
+ Python 3.8+
+ Python packages
+ pandas
+ scikit-learn

### Data

We'll download our dataset from [NOAA](https://www.ncdc.noaa.gov/cdo-web/search), a US government agency.
* You can follow these instructions to download the data:
* Go to  [NOAA](https://www.ncdc.noaa.gov/cdo-web/search) Search
* Enter the years you want data for (I recommend starting with 1990).
* Click add to [cart](https://www.ncdc.noaa.gov/cdo-web/search) on the stations.
* Go to the  [cart](https://www.ncdc.noaa.gov/cdo-web/search)
* Select the csv format and click continue.
* Select all of the checkboxes for data types.
* Enter your email and click continue.
* You'll get an email with a link to download the data.
* Make sure to take a look at the [data documentation](https://www1.ncdc.noaa.gov/pub/data/cdo/documentation/GHCND_documentation.pdf) as well.

## Project documentation
After selecting data from one station (Mellilia), we apply the following steps:
1. **Data Preprocessing:**
   - Effective handling of missing data with imputation using the mean.
   - Normalization of numerical features using `MinMaxScaler` ensures the data is suitable for machine learning models.

2. **Feature Engineering:**
   - Conversion of temperatures from Fahrenheit to Celsius is user-friendly and domain-relevant.
   - Extraction of temporal features such as `month` and `season` adds context for seasonal trends.
   - Moving averages (`TAVG_MA7`, `TAVG_MA30`) are excellent features for capturing short- and long-term trends.

3. **Data Visualization:**
   - Use of line plots to show temperature trends and moving averages aids understanding of patterns.
   - Correlation heatmaps provide insights into relationships between variables.

4. **Time Series Modeling:**
   - SARIMA model application is appropriate for capturing seasonal patterns in temperature data.
   - Forecast visualization with observed data effectively communicates predictions.

5. **Machine Learning Approach:**
   - Training a Random Forest Regressor on engineered features to predict temperature is well-suited for the data.
   - Splitting data into training and testing sets ensures a robust evaluation of model performance.

6. **Evaluation Metrics:**
   - Use of MAE and RMSE as evaluation metrics provides a clear measure of model accuracy.
7. **Additional Visualizations:**
   - Include histograms or boxplots of temperature data before and after imputation to visualize data distributions.

### Suggestions for Improvement:
1. **Data Validation:**
   - Consider performing exploratory data analysis (EDA) to check for outliers and data quality issues before imputation and normalization.

2. **Feature Importance:**
   - After training the Random Forest model, analyze feature importance to understand which variables contribute most to the predictions.

3. **Model Optimization:**
   - Explore hyperparameter tuning for both SARIMA (e.g., grid search for `order` and `seasonal_order`) and Random Forest (e.g., depth, number of estimators) for potentially better results.

4. **Cross-Validation:**
   - Use cross-validation instead of a single train-test split to ensure the model’s robustness.

5. **Advanced Imputation:**
   - For missing values, consider more advanced methods like KNN imputation or leveraging time-series methods for temperature variables.


### Outcomes:
- The MAE and RMSE provide a quantitative summary of your model's performance. If MAE and RMSE values are low, it suggests your predictions are close to the observed data.
- The  ability to combine statistical, time-series, and machine learning approaches shows versatility.

