# Household energy use prediction
### By – Ajay das
### (part of IBM advanced data science capstone project)

### Files:

1. **01_EnergyUsePrediction_etl:** Data file import notebook
2. **02_EnergyUsePrediction_data_exp:** Data Exploration notebook
3. **03_EnergyUsePrediction_feature_eng:** Feature engineering notebook
4. **04_EnergyUsePrediction_model_def_train_eval:** Model training and evaluation notebook
5. **EnergyUsePrediction:** Combined notebook for 1 through 4
6. **energydata_complete.csv:** Data file


### Dataset Information:

* Source: Open-source data located at UC Irvine ML website https://archive.ics.uci.edu/ml/datasets/Appliances+energy+prediction
* Collection of temperature sensors and humidity sensors measurements installed in one house, appliances/lights energy use and weather station data.
* Temperature, Humidity and Energy use data was collected and averaged to every 10 minutes over 4.5 months (Jan 11 to May 27, 2016)
* Weather data downloaded from public dataset from nearest weather station (Chievres Airport, Belgium)
* Data has 19,735 observations and 29 columns

### Objective and Use Cases

* Predict energy use by appliances based on temperature, humidity, other weather conditions and date time
* Manage household energy use if high dependency on any feature is discovered
* Identify unusually high energy use if deviation of actual energy use from predicted energy use exceeds threshold and notify user to take action to lower it
* Trigger preventive maintenance notification if appliance energy use is abnormal and does not follow prediction

### Solution

* Data exploration was performed to understand the features and identify any relationship between the features and energy use
* Exploration of statistical summary and trend of variables to identify predictive capability of the features
* Energy use was converted to log scale to help improve predictability
* Correlation analysis and hourly, weekly and monthly group plots to identify any patterns to help in feature engineering and feature selection
* Final model used 11 features (5 humidity, 3 temperature, 3 weather) with accuracy score (R^2) of 0.74
