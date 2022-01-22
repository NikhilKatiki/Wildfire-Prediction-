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
<img width="406" alt="01" src="https://user-images.githubusercontent.com/89437135/150622564-b7833340-7dba-4069-b970-623b1e1ef88d.png">
<br>
  2. InyoNationalForest.nc - This file is the weather data which consists of the following attributes <br>
 &nbsp;&nbsp;&nbsp;&nbsp;i.Precipitation<br>
 &nbsp;&nbsp;&nbsp;&nbsp;ii.Temperature <br>
 &nbsp;&nbsp;&nbsp;&nbsp;iii.Soil level moisture <br>
Below is the snapshot of the data <br>
<img width="476" alt="05" src="https://user-images.githubusercontent.com/89437135/150622788-6629c1e4-929f-4642-9151-afe2bf778bd0.png">

# Data Understanding 

  &nbsp;&nbsp;&nbsp;&nbsp;i. The frequency of wildfires are following a bell shaped distribution <br>
  <img width="317" alt="02" src="https://user-images.githubusercontent.com/89437135/150622622-70abe374-e296-46b0-9c40-dc9756a84d19.png">
    <br>
  
   &nbsp;&nbsp;&nbsp;&nbsp;ii. The trend in the average number of wildfires is varying a lot and is mostly random <br>
    <img width="424" alt="03" src="https://user-images.githubusercontent.com/89437135/150622637-b585312a-1c8a-4d27-b3be-edca123fb802.png">

# Feature Engineering 
  &nbsp;&nbsp;&nbsp;&nbsp;i.Features are generated from the weather dataset <br>
  &nbsp;&nbsp;&nbsp;&nbsp;ii.It is highly likely to cause the wildfire when the weather conditions are extreme <br>
  &nbsp;&nbsp;&nbsp;&nbsp;iii.Therefore, Features which can capture the edge cases are being generated. Examples of such features are Max, Min and Mean of corresponsing weather variables <br>
  &nbsp;&nbsp;&nbsp;&nbsp;iv.Below is the correlation matrix of the variables in the final dataset <br>
  <img width="544" alt="04" src="https://user-images.githubusercontent.com/89437135/150622662-48a838f4-3232-420d-bc4f-1f644bd08191.png">
# Model Development
    Model development is an iterative process. The predictor variable is continuous and the following approaches are being tested for prediction modelling 
    i.Linear Regression
    ii.CAT Boost Regression 
    iii. Random Forest Regressor 
## Linear Regression 
    i. It is clear from the correlation matrix that most of the variables are auto correlated which violates the assumption of Linear regression
    ii.Therefore, Variance Inflation factor (Linear relationship between the one independent variable and other independent varibles) is being checked and established a cutoff of 7
    iii. EVen though, Variables are being removed in every iteration due to multicollinearity, the accuracy of the model isn't varying much 
    iv. The final model can be called as "Parsimonious model" with only Pev_max, month indicator and tp_min variables 
 ## CAT Boost algorithm
    i.One of the main reasons to choose CAT boost is that it can perform well even if the data is less 
    ii.Also, since the month is a categorical variable, using CAT boost can be more beneficial 
 ## Random Forest Regressor 
    i.One of the main reasons to choose CAT boost is that it can perform well even if the data is less <br>
    ii.Also, since the month is a categorical variable, using CAT boost can be more beneficial     
# Results 
    1. Linear Regression performed much better than the other non linear advanced algorithms
    2. With increase in pev_max, there is an decrease in the number of wildfires 
    3. The increase in tp directly corresponds to the increase in the number of wildfires 
# Future Steps 
    1. More variables which can impact Wildfires can be included in the model 
    2. Time series forecasting can also be done to predict the number of Wildfires
    
   
    
