## Detecting Early Readmission of Diabetes Patients
![MSHS-MSDE85-2col-770x420](https://github.com/user-attachments/assets/bf3a3dd0-ca54-48c2-ba79-e013dcd9a1af)

#### Author : [Sabrina Sayed](https://github.com/sabrinasayed99)

## Overview:
Diabetes is one of the most dangerous diseases across the world. I have grown up seeing my family members struggling to manage their diabetes and have lived long enough to lose multiple relatives to the disease. In the United States, diabetes is growing amongst young people, leaving the most vulnerable communities in danger. Researchers have forecasted if the rate of new diagnoses continues to increase, Type 1 diabetes cases would increase about 65% and Type 2 diabetes cases would increase about 700%.
https://www.cdc.gov/diabetes/data-research/research/young-people-diabetes-on-rise.html
     
I was curious to explore how our healthcare system and hospitals are managing the disease. [Studies have reported diabetes increases the risk of a 30 day readmission by at least 17% and up to 2.5 fold. The increased risk of readmission is most pronounced when diabetes is the primary reason for hospitalization](https://onlinelibrary.wiley.com/doi/10.1155/2014/781670). It is widely recognized that the management of hyperglycemia (high blood sugar) in hospitalized patients has a significant bearing on morbidity and mortality; however, for non-ICU inpatients in particular, evidence shows hyperglycemia management is often arbitrary and leads to either no treatment at all or wide fluctuations in glucose, due to the lack of formalized protocols in non-ICU environments.

## The Problem:
This project utilizes the U.C. Irvine 'Diabetes Dataset From 130 U.S. Hospitals (1999-2008)' to predict the early admission of patients, less than 30 days after discharge. Readmission can be a strong indicator of quality of care. When unplanned readmission is high, it can indicate low quality of care, lack of treatment, or disorganization.

According to the NIH, the annual cost of readmissions within 30 days of discharge is $20-25 billion, based on the most inclusive readmission rates of 16-20% among diabetes patients in the United States. Readmissions can also cause unnecessary emotional, physical, and social burdens for patients. To efficiently implement interventions intended to reduce readmission risk and the associated costs, it is critical to understand the causes of readmissions as well as to identify patients at higher risk. 

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
- Languages: Python
- Libraries: scikit-learn, sci-py, pandas, numpy, matplotlib, seaborn, SQL.

## Methods:
I built a baseline Decision Tree Classifier model, a Logistic Regression model, and a second Decision Tree Classifier. I utilized various encoding and scaling techniques including OneHotEncoder, StandardScaler, and LabelEncoder. I used hyperparameter tuning techniques like Synthetic Minority Oversampling to address the class imbalance in the dataset. I prioritized recall as my main metric upon evaluation. 

## Results: 
The third model I built, a Decision Tree Classifier, proved to be the best predictor of early readmission patients with a recall score of 91% and precision of 9%. 
![Model_3_Classifier_Tree_SMOTE](https://github.com/user-attachments/assets/d844bf60-57d2-4f5b-8331-f469f899d251)
![Model_3_CFMAT_SMOTE](https://github.com/user-attachments/assets/447c4c5f-b144-40ad-a7c6-290eda2beb2c)


Through data exploration, there was a great deal of missing data for Hemoglobin A1C and glucose levels. These are 2 of the most important  indicators of the efficacy of diabetes treatment. There was a strong correlation between patients who did not get these measurements taken and those who were readmitted to the hospital within 30 days of discharge.  
    
![Glucose_Measured_Significance](https://github.com/user-attachments/assets/4410f0d7-372e-4d83-85f1-85f246500eac)
![Glucose_Results_Distribution](https://github.com/user-attachments/assets/99858934-4da3-449b-8320-2869364009f6)
![HbA1c_Result_Distribution](https://github.com/user-attachments/assets/004f7fae-84ae-4772-a8ca-00db28992390)


For our intents and purposes we are prioritizing recall score over the precision score because the cost of missing a patient at risk of early readmission is much higher than one that that is not. The average readmission rate for a hospital is 15% and the cost of each readmission is about $15,000. Implementing this model would mean we could prevent 91% of those readmissions and save a total of $17 million per year, assuming the hospital admits 10,000 patients per year.

## Recommendations:
Improve quality of care for diabetes patients by establishing a formalized protocol for hyperglycemia management in  non-ICU floors. It is clear that measuring Hemoglobin A1C and Glucose in diabetes patients
is a strong predictor of readmission. These measurements are strong indicators of treatment efficacy and the state of the patient.

## Next Steps:
Collect more recent data from more hospitals
Collect more representative data inclusive of minority populations 
Continue research into predictors of readmission for non-diabetes patients


## Directory:
[Presentation](file:///Users/sabrinasayed/Downloads/EARLY%20READMISSION%20OF%20DIABETES%20PATIENTS.pdf)
[Dataset](https://archive.ics.uci.edu/dataset/296/diabetes+130-us+hospitals+for+years+1999-2008)

## Repository Files:

### Cleaned Data 
Cleaned Data folder contains the cleaned dataframe that was used for exploratory data analysis and modeling

### Data
Contains the raw data files, databases, and alternative dataframes built from filtering features

### EDA
Includes jupyter notebook of data exploration, data cleaning, alternative databases, SQL queries, statistical analyses, and graphical visualizations of feature relationships.

### Modeling Notebooks
Includes 3 jupyter notebooks of baseline model, second model, and third model

### Images
Stores images of all visualizations that were created.

### EARLY READMISSION OF DIABETES PATIENTS.pdf
A pdf version of the presentation slides.
