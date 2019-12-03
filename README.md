# Measles Outbreaks In European Countries 
---

_Author: Preeya Sawadmanod_ 

## Table of Contents 

* [Problem Statement](#Problem-Statement)
* [Executive Summary](#Executive-Summary)
* [Datasets](#Datasets)
* [Modeling](#Modeling)
* [Evaluation](#Evaluation)
* [Conclusion](#Conclusion)
* [Next Steps](#Next-Steps)

## Problem Statement 

Introduction: 

- Measles outbreak 

- Where did get the data? Adding website 


- Problem Statement? 
Analyze and determine the spread of epidemic diseases such as Measles in European Countries. Building a time series model that could predict when the next outbreak of epidemic would most likely be. 


- Why is it important 
ECDC's Mission: 
The European Centre for Disease Prevention and Control (ECDC) was established in 2005. It is an EU agency aimed at strengthening Europe's defences against infectious diseases. According to Article 3 of the Founding Regulation, ECDC's mission is to identify, assess and communicate current and emerging threats to human health posed by infectious diseases. In order to achieve this mission, ECDC works in partnership with national health protection bodies across Europe to strengthen and develop continent-wide disease surveillance and early warning systems. By working with experts throughout Europe, ECDC pools Europe's health knowledge to develop authoritative scientific opinions about the risks posed by current and emerging infectious diseases.

About ECDC
ECDC is an EU agency aimed at strengthening Europe's defences against infectious diseases. The core functions cover a wide spectrum of activities: surveillance, epidemic intelligence, response, scientific advice, microbiology, preparedness, public health training, international relations, health communication, and the scientific journal Eurosurveillance. ECDC disease programmes cover antimicrobial resistance and healthcare-associated infections; emerging and vector-borne diseases; food- and waterborne diseases and zoonoses; HIV, sexually transmitted infections and viral hepatitis; influenza and other respiratory viruses; tuberculosis; and vaccine-preventable diseases. In 2019, ECDC continues to contribute to health security, giving particular attention to the following areas:

- Tackle antimicrobial resistance
- Improve vaccine coverage in the EU
- Support the European Commission and the Member States in addressing the Sustainable Development Goals in the area of HIV, TB and hepatitis
- Further support the European Commission and the Member States in strengthening the preparedness for cross-border health threats
- Focus on strategic partnerships to create synergy and avoid duplication of work
- Further enhance ECDC’s operational performance and monitoring. 


* Is it clear what the goal of the project is?
* What type of model will be developed?
* How will success be evaluated?
* Is the scope of the project appropriate?
* Is it clear who cares about this or why this is important to investigate?
* Does the student consider the audience and the primary and secondary stakeholders?

## Executive Summary 

The ECDC publishes a monthly surveillance report on measles and rubella data submitted by the 30 European Union/European Economic Area (EU/EEA) countries in the ECDC Surveillance Atlas of Infectious Diseases. The routine disease data are submitted on a monthly basis by 30 EU/EEA countries and the data for this project was collected through the Surveillance Atlas of Infectious Diseases through the following [link](https://www.ecdc.europa.eu/en/measles/surveillance-and-disease-data/atlas). 

After obtaining the [CSV files](../data), the data was cleaned by dropping 

In Data cleaning 

In this notebook, we are going to load in our datasets and clean it. The initial step is to look into each datasets and combine them together in order to accelerate the cleaning process. The cleaning process in this notebook consists of the followings steps:

Renaming columns as lowercases in names is easier to further process
Dropping rows/columns such as duplicates or uninformative columns
Checking for missing values and impute missing values if necessary
Checking for different data types
After the cleaning process, the data is going to be safe into a new CSV file.


In EDA 


<!-- Data Cleaning and EDA

Are missing values imputed/handled appropriately?
Are distributions examined and described?
Are outliers identified and addressed?
Are appropriate summary statistics provided?
Are steps taken during data cleaning and EDA framed appropriately?
Does the student address whether or not they are likely to be able to answer their problem statement with the provided data given what they've discovered during EDA?
 -->


In Modeling 



<!-- Preprocessing and Modeling

Is text data successfully converted to a matrix representation?
Are methods such as stop words, stemming, and lemmatization explored?
Does the student properly split and/or sample the data for validation/training purposes?
Does the student test and evaluate a variety of models to identify a production algorithm (AT MINIMUM: Bayes and one other model)?
Does the student defend their choice of production model relevant to the data at hand and the problem?
Does the student explain how the model works and evaluate its performance successes/downfalls? -->

## Datasets 

|Name|Descriptions|
|---|---|
|[ECDC_surveillance_data_Measles_reports.csv](../data/ECDC_surveillance_data_Measles_reports.csv)| This datasets includes Measles's Notification rate, Reported cases of Measles, Confirmed reported cases of Measles and Number of Deaths caused by Meales in 30 European Countries from 1999 - 2018.|
|[ECDC_surveillance_data_Measles.csv](../data/ECDC_surveillance_data_Measles.csv)| This datasets includes Vaccination rate of first and second dosage for Measles prevention in 30 different European Countries from 1999 - 2018.| 
|[measles.csv](../data/measles.csv)| This dataset is the combined and cleaned version of ECDC surveillance datasets including Measles outbreaks and Vaccination records. 

## Modeling 

## Evaluation 

## Conclusion 

## Next Steps 


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