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
Below is the snapshot of the data
<br>
# Data Preprocessing  
   The reviews data is in string format which needs to be converted to numeric format to find the quantitative sentiment score. Following are the steps <br> 
     1.Tokenization <br>
      &nbsp;&nbsp;&nbsp;&nbsp;    i.The sentences are being tokenized into words<br>
     2.Stemming<br>
       &nbsp;&nbsp;&nbsp;&nbsp;   i.Affixes or Prefixes are removed to reduce the dimensionality and get the words to its base form <br>
     3.Stop words<br>
       &nbsp;&nbsp;&nbsp;&nbsp;   i.Stop words which are frequently used are being removed as these dont contribute to the overall sentiment of the customer <br>
     4.Numeric formats <br>
        &nbsp;&nbsp;&nbsp;&nbsp;  i.Numeric formats have been removed as these are not useful in understanding the review <br>
# Feature Engineering 
   Positive words and Negative words <br>
         &nbsp;&nbsp;&nbsp;&nbsp; i.Finding the number of positive words and negative words for every review <br>
          &nbsp;&nbsp;&nbsp;&nbsp;ii.Storing number of positive words in positive and number of negative words in negative <br>
# Model Development
   The score is calculated using the formula: <br>
          Sentiment score = (#Positive)/(#Positive+#Negative) when #Positive>#Negative <br>
                        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  =-(#Negative)/(#Positive+#Negative) when #Positive>#Negative<br>
                        <img width="600" alt="Sentimentscore" src="https://user-images.githubusercontent.com/89437135/147394661-cdb53265-33ad-4630-8bd2-ffe5524f7b81.png">
<br>
# Results 
  1.From the analysis, it is clear that Airbnb implemented strategies which makes them unique in responding to the pandemic <br>
  2.Sentiment dropped after March 2020, but as the company takes remedial steps, sentiment increased over time <br>
  3.Top positive and negative comments did not change much in pre and post Covid  <br>
  4.Dirty and Crowded are highlighted negative comments post-Covid which can be suggestion to Airbnb hotels which are having low sentiment scores <br>
