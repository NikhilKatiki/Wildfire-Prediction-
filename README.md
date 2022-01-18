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
<image>

  3. InyoNationalForest.nc - This file is the weather data which consists of the following attributes <br>
 &nbsp;&nbsp;&nbsp;&nbsp;i.Precipitation<br>
 &nbsp;&nbsp;&nbsp;&nbsp;ii.Temperature <br>
 &nbsp;&nbsp;&nbsp;&nbsp;iii.Soil level moisture <br>
Below is the snapshot of the data <br>
# Data Understanding 
  &nbsp;&nbsp;&nbsp;&nbsp;i. The frequency of wildfires are following a bell shaped distribution <br>
  <image>
    <br>
   &nbsp;&nbsp;&nbsp;&nbsp;ii. The trend in the average number of wildfires is varying a lot and is mostly random <br>
    <image>
      <br>
# Feature Engineering 
  &nbsp;&nbsp;&nbsp;&nbsp;i.Features are generated from the weather dataset<br>
  &nbsp;&nbsp;&nbsp;&nbsp;ii.It is highly likely to cause the wildfire when the weather conditions are extreme <br>
  &nbsp;&nbsp;&nbsp;&nbsp;iii.Therefore, Features which can capture the edge cases are being generated. Examples of such features are Max, Min and Mean of corresponsing weather variables <br>
  &nbsp;&nbsp;&nbsp;&nbsp;iv.Below is the correlation matrix of the variables in the final dataset <br>
  <image> 
    <br>
# Model Development
## Linear Regression 
    
# Results 
  1.From the analysis, it is clear that Airbnb implemented strategies which makes them unique in responding to the pandemic <br>
  2.Sentiment dropped after March 2020, but as the company takes remedial steps, sentiment increased over time <br>
  3.Top positive and negative comments did not change much in pre and post Covid  <br>
  4.Dirty and Crowded are highlighted negative comments post-Covid which can be suggestion to Airbnb hotels which are having low sentiment scores <br>
