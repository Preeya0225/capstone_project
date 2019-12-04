# Measles Outbreaks In European Countries 
---

_Author: Preeya Sawadmanod_ 

## Table of Contents 

* [Problem Statement](#Problem-Statement)
* [Executive Summary](#Executive-Summary)
* [Datasets](#Datasets)
* [Modeling](#Modeling)
    - [Evaluation of Model](#Evaluation-of-Model) 
* [Conclusion](#Conclusion)
    - [Limitations](#Limitations) 
* [Next Steps](#Next-Steps)

## Problem Statement 

The European Centre for Disease Prevention and Control (ECDC) was established in 2005. It is an EU agency aimed at strengthening Europe's defenses against infectious diseases. The core functions cover a wide spectrum of activities such as surveillance, epidemic intelligence, public health training, international relations, health communication, and etc. One interesting function is the vaccine-preventable diseases such as Measles and Rubella. 

Measles is an acute, highly contagious viral disease capable of causing epidemics. Infectivity is close to 100% in susceptible individuals and in the pre-vaccine era measles would affect nearly every individual during childhood. Immunization has dramatically reduced the incidence of measles in Europe but despite overall high immunization coverage, measles continues to cause frequent outbreaks. Globally, measles remains a leading cause of childhood deaths and an estimated 160,000 children die each year from complications of the disease. 

By looking at historical surveillance data in the European countries, can we build a time series model and predict when the next Measles outbreaks would most likely occur? The objective is to detect outbreaks earlier and aim to ensure timely responses to take appropriate public health measures. It is important detect outbreaks early on, especially since measles is a vaccine-preventable disease and childhood deaths can often be prevented. The goal of this project to develop a predictive model to forecast Measles outbreaks and in like every time series models, we can use mean squared error to evaluate our model.


## Executive Summary 

The ECDC publishes a monthly surveillance report on measles and rubella data submitted by the 30 European Union/European Economic Area (EU/EEA) countries in the ECDC Surveillance Atlas of Infectious Diseases. The routine disease data are submitted on a monthly basis by 30 EU/EEA countries and the data for this project was collected through the Surveillance Atlas of Infectious Diseases through the following [link](https://www.ecdc.europa.eu/en/measles/surveillance-and-disease-data/atlas). 

After obtaining the [CSV files](https://github.com/Preeya0225/capstone_project/tree/master/data), the data was cleaned by checking for duplicates, missing values and different data types. The cleaning process can be found in this [Notebook](./code/1_data_cleaning.ipynb). After the cleaning process, the data was then saved into a new CSV file.

In [Exploratory Data Analysis Notebook](./code/2_eda.ipynb) the Measles outbreaks data was analyzed by looking into each specific country of the 30 EU/EEA countries. During EDA shown in the plot below, Measles outbreaks in Germany occurred most frequently from 2000 - 2019 and resulted in the most suited country for predicting Measles outbreaks over time. Selecting Germany as our target country for predictions to further continue to our next step, Modeling.

![Germany outbreaks](./images/eda/outbreaks_Germany.jpeg)

During [Modeling](./code/3_modeling.ipynb) the data was preprocessed and then used to predict outbreaks in Germany with an ARIMA and a SARIMAX model. The SARIMAX model, also known as Seasonal Autoregressive Integrated Moving Average with eXogenous regressors model, resulted in approx. XXXX Mean Squared Error, which was the best model with the minimum Mean Squared Errors compared to our other models. 

In conclusion, utilizing our vaccination records and historical data from measles cases, we were able to obtain a model predicting Measles Outbreaks in Germany. 


## Datasets 

|Name|Descriptions|
|---|---|
|[ECDC_surveillance_data_Measles_reports.csv](./data/ECDC_surveillance_data_Measles_reports.csv)| This datasets includes Measles's Notification rate, Reported cases of Measles, Confirmed reported cases of Measles and Number of Deaths caused by Meales in 30 European Countries from 1999 - 2018.|
|[ECDC_surveillance_data_Measles.csv](./data/ECDC_surveillance_data_Measles.csv)| This datasets includes Vaccination rate of first and second dosage for Measles prevention in 30 different European Countries from 1999 - 2018.| 
|[measles.csv](./data/measles.csv)| This dataset is the combined and cleaned version of ECDC surveillance datasets including Measles outbreaks and Vaccination records. 

## Modeling 

In our time series model, the SARIMAX (1,0,0) X (x,x,12) model in the plot below shows our training set, testing set and predictions of reported confirmed cases of Measles outbreaks. The Mean Squared Error(MSE) resulted in X value. This model had the least MSE compared to other models, and can be concluded to be our best model.

![modeling](./images/modeling/SARIMAX_model.jpeg)

### Evaluation of Model 

* Looking into each outbreaks 

## Conclusion 

Overall, by looking at historical surveillance data in European countries, we were able to create a time series model predicting Measles outbreaks in Germany. This model could be use as an early warning systems 

However, there are many limitations with this model 


### Limitations

* Targeted Germany but what about other countries (Difficult to capture seasonality, trends)
> looking into Italy
> looking into Austria 
* Accurate data for vaccination rate especially newborns
* Herd Immunity 
* Outbreaks in certain community 
* Further deep dive if there are additional reasons for outbreaks > Travelers

## Next Steps 


<p align="center">
  <img width="400" height="400" src="./images/map.gif">
</p>

* Providing Real-Time data this can be used as continent-wide disease surveillance for early warning detections
* Predicting which country is most likely going to experience a Measles outbreaks 
* Using GeoSpatial data to create a model where countries are assigned higher risk if neighboring countries have outbreaks 



<!-- ECDC's Mission: 
 According to Article 3 of the Founding Regulation, ECDC's mission is to identify, assess and communicate current and emerging threats to human health posed by infectious diseases. In order to achieve this mission, ECDC works in partnership with national health protection bodies across Europe to strengthen and develop continent-wide disease surveillance and early warning systems. By working with experts throughout Europe, ECDC pools Europe's health knowledge to develop authoritative scientific opinions about the risks posed by current and emerging infectious diseases. -->


<!-- Evaluation and Conceptual Understanding

Does the student accurately identify and explain the baseline score?
Does the student select and use metrics relevant to the problem objective?
Does the student interpret the results of their model for purposes of inference?
Is domain knowledge demonstrated when interpreting results?
Does the student provide appropriate interpretation with regards to descriptive and inferential statistics?


Conclusion and Recommendations

Does the student provide appropriate context to connect individual steps back to the overall project?
Is it clear how the final recommendations were reached?
Are the conclusions/recommendations clearly stated?
Does the conclusion answer the original problem statement?
Does the student address how findings of this research can be applied for the benefit of stakeholders?
Are future steps to move the project forward identified? -->
