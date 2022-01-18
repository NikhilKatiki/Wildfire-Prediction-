# Wildfire-Prediction-
  1. Introduction
  2. Objective 
  3. Data Dictionary
  4. Data Pre-processing
  5. Feature Engineering 
  6. Model Development 
  8. Results
# Introduction 
  1. There has been increased effort in understanding how wildfires starts and what causes wildfires to increase <br>
  2. Wildfire prediction has become a key aspect to both researchers who study controlled fires and the meterologists who are using hot spots and update the routes that are critical to conditions <br>
  3. For preventive measures, fire weather forecasting uses atmospheric conditions to evaluate wildifire risk 
# Objective 
  1.The prediciton of wildfire using the weather related attributes is one of the objectives  <br> 
  2.Our objective is not only limited to just predicting rather inferencing the model we get from the linear regression to understand the impact of weather attributes on wildfires <br>
# Data Sources and Data Dictionary 
  1. Train.csv - This file consists of wildfires frequency along with the date it happened and the reporting unit <br>
Below is the snapshot of the data <br>
<image>;

  3. InyoNationalForest.nc - This file is the weather data which consists of the following attributes <br>
 &nbsp;&nbsp;&nbsp;&nbsp;i.Precipitation<br>
 &nbsp;&nbsp;&nbsp;&nbsp;ii.Temperature <br>
 &nbsp;&nbsp;&nbsp;&nbsp;iii.Soil level moisture <br>
Below is the snapshot of the data <br>
# Data Understanding 
  &nbsp;&nbsp;&nbsp;&nbsp;i. The frequency of wildfires are following a bell shaped distribution <br>
  <image>;
    <br>
  
   &nbsp;&nbsp;&nbsp;&nbsp;ii. The trend in the average number of wildfires is varying a lot and is mostly random <br>
    <image>;
      <br>
# Feature Engineering 
  &nbsp;&nbsp;&nbsp;&nbsp;i.Features are generated from the weather dataset<br>
  &nbsp;&nbsp;&nbsp;&nbsp;ii.It is highly likely to cause the wildfire when the weather conditions are extreme <br>
  &nbsp;&nbsp;&nbsp;&nbsp;iii.Therefore, Features which can capture the edge cases are being generated. Examples of such features are Max, Min and Mean of corresponsing weather variables <br>
  &nbsp;&nbsp;&nbsp;&nbsp;iv.Below is the correlation matrix of the variables in the final dataset <br>
  <image> ;
    <br>
# Model Development
    &nbsp;&nbsp;&nbsp;&nbsp; Model development is an iterative process. The predictor variable is continuous and the following approaches are being tested for prediction modelling 
    &nbsp;&nbsp;&nbsp;&nbsp; i.Linear Regression
    &nbsp;&nbsp;&nbsp;&nbsp; ii.CAT Boost Regression 
    &nbsp;&nbsp;&nbsp;&nbsp; iii. Random Forest Regressor 
## Linear Regression 
    &nbsp;&nbsp;&nbsp;&nbsp; i. It is clear from the correlation matrix that most of the variables are auto correlated which violates the assumption of Linear regression
    &nbsp;&nbsp;&nbsp;&nbsp; ii.Therefore, Variance Inflation factor (Linear relationship between the one independent variable and other independent varibles) is being checked and established a cutoff of 7<br>
    &nbsp;&nbsp;&nbsp;&nbsp; iii. EVen though, Variables are being removed in every iteration due to multicollinearity, the accuracy of the model isn't varying much <br>
    &nbsp;&nbsp;&nbsp;&nbsp; iv. The final model can be called as "Parsimonious model" with only Pev_max, month indicator and tp_min variables <br>
 ## CAT Boost algorithm
    &nbsp;&nbsp;&nbsp;&nbsp;i.One of the main reasons to choose CAT boost is that it can perform well even if the data is less <br>
    &nbsp;&nbsp;&nbsp;&nbsp; ii.Also, since the month is a categorical variable, using CAT boost can be more beneficial 
 ## Random Forest Regressor 
    &nbsp;&nbsp;&nbsp;&nbsp;i.One of the main reasons to choose CAT boost is that it can perform well even if the data is less <br>
    &nbsp;&nbsp;&nbsp;&nbsp; ii.Also, since the month is a categorical variable, using CAT boost can be more beneficial     
# Results 
    1. Linear Regression performed much better than the other non linear advanced algorithms
    2. With increase in pev_max, there is an decrease in the number of wildfires 
    3. The increase in tp directly corresponds to the increase in the number of wildfires 
# Future Scope 
    1. Adding more features which can 
   
    
