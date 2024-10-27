## Detecting Early Readmission of Diabetes Patients

![Image](url)

#### Author : [Sabrina Sayed](https://github.com/sabrinasayed99)

## Overview:
     Diabetes is one of the most dangerous diseases across the world. I have grown up seeing my family members struggling to manage their diabetes and have lived long enough to lose multiple relatives to the disease. [In the United States, diabetes is growing amongst young people, leaving the most vulnerable communities in danger. Researchers have forecasted if the rate of new diagnoses continues to increase, Type 1 diabetes cases would increase about 65% and Type 2 diabetes cases would increase about 700%] (https://www.cdc.gov/diabetes/data-research/research/young-people-diabetes-on-rise.html). 
     
     I was curious to explore how our healthcare system and hospitals are managing the disease. [Studies have reported diabetes increases the risk of a 30 day readmission by at least 17% and up to 2.5 fold. The increased risk of readmission is most pronounced when diabetes is the primary reason for hospitalization](https://onlinelibrary.wiley.com/doi/10.1155/2014/781670). It is widely recognized that the management of hyperglycemia (high blood sugar) in hospitalized patients has a significant bearing on morbidity and mortality; however, for non-ICU inpatients in particular, evidence shows hyperglycemia management is often arbitrary and leads to either no treatment at all or wide fluctuations in glucose, due to the lack of formalized protocols in non-ICU environments.

## The Problem:

    This project utilizes the U.C. Irvine 'Diabetes Dataset From 130 U.S. Hospitals (1999-2008)' to predict the early admission of patients, less than 30 days after discharge. Readmission can be a strong indicator of quality of care. When unplanned readmission is high, it can indicate low quality of care, lack of treatment, or disorganization.

    According to the NIH, the annual cost of readmissions within 30 days of discharge is $20-25 billion, based on the most inclusive readmission rates of 16-20% among diabetes patients in the United States. Readmissions can also cause unnecessary emotional, physical, and social burdens for patients. To efficiently implement interventions intended to reduce readmission risk and the associated costs, it is critical to understand the causes of readmissions as well as to identity patients at higher risk. 

## Data:
    The Diabetes Dataset From 130 U.S. Hospitals (1999-2008) provides data on diabetes patients' hospitalization. Sensitive data like the patient's race, gender, and age was included in the categorical data along with diagnoses, reason for admission, prescriptions, lab results, insurance code, and discharge disposition. Numerical data includes the time spent in the hospital, number of medications received during the visit and number of procedures. There is heavy class imbalance with patients readmitted within 30 days being the minority class. 


## Features:
- Encounter ID
- Patient number
- Race Values
- Gender Values
- Age 
- Weight
- Admission type
- Discharge disposition
- Admission source
- Time in hospital
- Payer code
- Medical specialty
- Number of lab procedures
- Number of procedures
- Number of medications 
- Number of outpatient visits
- Number of emergency visits 
- Number of inpatient visits 
- Diagnosis 1
- Diagnosis 2 
- Diagnosis 3 
- Number of diagnoses 
- Glucose serum 
- Diabetes medications 
- 24 features for medications 
- Readmitted Days to inpatient readmission
  
## Tech Stack:
Languages: Python
Libraries: scikit-learn, sci-py, pandas, numpy, matplotlib, seaborn, SQL.

## Methods:
    I built a baseline Decision Tree Classifier model, a secondary Logistic Regression model, and a third Decision Tree Classifier with reduced features. I utilized various encoding and scaling techniques including OneHotEncoder, StandardScaler, and LabelEncoder. I used hyperparameter tuning techniques like SMOTE to handle class imbalance and prioritized precision and recall as my main metrics upon evaluation.

## Results: 
    The third model, a Decision Tree Classifier, proved to be the best predictor of early readmission patients with a recall score of 91% and . 
    ![decision tree ]
    ![confusion matrix]

    Through data exploration, there was a great deal of missing data for Hemoglobin A1C and glucose levels. These are 2 of the most important  indicators of the efficacy of diabetes treatment. There was a strong correlation between patients who did not get these measurements taken and those who were readmitted to the hospital within 30 days of discharge.  

    ** SHow Missing Hemoglobin and glucose results***
    
    For our intents and purposes we are prioritizing recall score over the precision score because the cost of missing a patient at risk of early readmission is much higher than one that that is not. If 20% of diabetes patients are at risk of readmission, using this model we can prevent 90% of those readmissions and save a total of $18 billion. 

    
	
    
