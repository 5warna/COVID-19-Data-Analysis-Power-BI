# COVID-19-Data-Analysis-Power-BI

Coronavirus disease (COVID-19) is an infectious disease caused by the SARS-CoV-2 virus. Most people infected with the virus will experience mild to moderate respiratory illness and recover without requiring special treatment. 

This report presents a comprehensive analysis of the COVID-19 dataset, which contains information about different disease symptoms(COVID Disease Degree). The report aims to explore factors influencing patient survival and gain insights into patterns and trends related to the disease. By analyzing this dataset, we can better understand the circumstances surrounding the infectious disease and identify key factors that contributed to survival rates.

### Dataset Description

The datasets consists of several medical predictor variables and one target variable (Classification Final). Predictor variables includes age, sex, patient type, different pregnancy-related situations, patients with various conditions, and more.

### DATA QUALITY:

Before conducting the analysis, performed a thorough data quality check to ensure data integrity and consistency. This process involved handling spelling check, adding conditional columns, and addressing any inconsistencies in the dataset.

### Analysis done on:

Cards: Total Patients, Patients Hospitalized, Total Patients Survived, Total Patients Died, Total Male Patients, Total Female Patients, Average Age, Patients Returning Home, Chronic Obstructive Pulmonary Patients, Asthma Patients, Tobacco User Patients, Cardio Vascular Patients, Diabetes Patients, Hypertension Patients, Obesity Patients, Renal Chronic Patients, Immunosuppressed Patients, Other Disease Patients.

Slicers: Age(groups), Gender, Intensive Care Unit, Level of Ventilator, Institution Type, Medical Level, Pregnancy, COVID Disease Degree.

Donut Chart: COVID 19 Disease Degree in Patients, Different levels of Ventilator Support.

Pie Chart: Hospitalized Pneumonia Patients, Patients with ventilator in ICU.

Clustered Column/Bar Chart: COVID 19 Disease Degree by Gender, Immunosuppressed Patients, Tobacco User Patients, Asthma Patients Hospitalized or Home, Cardiovascular with Respiratory Problems, Survived with Pneumonia and Ventilator.

Matrix: Patients Survived and Died with Disease, Patients Survived and Died with Different Diseases.

Funnel: Patients Hospitalized with Disease Type.

Stacked Area Chart: Pregnancy Patients, Patients Survived and Died with Ventilator.

Ribbon Chart: Intensive Care Unit Patients, COPD Patients Hospitalized or Home.

Stacked Bar Chart: Patients Survived and Died with Ventilator.

### Data Analysis Expressions (DAX) Formulas used in Measures:

Average Age = AVERAGE(Covid_Dataset[AGE])

Female Count = CALCULATE(COUNTROWS('Covid_Dataset'),'Covid_Dataset'[Gender] = "Female")

Male Count = CALCULATE(COUNTROWS('Covid_Dataset'),'Covid_Dataset'[Gender] = "Male")

Patient Hospitalized = CALCULATE(COUNTROWS('Covid_Dataset'),'Covid_Dataset'[PATIENT_TYPE] = 2)

Patient Returning Home = CALCULATE(COUNTROWS('Covid_Dataset'),'Covid_Dataset'[PATIENT_TYPE] = 1)

Total Asthma Patients = CALCULATE(COUNTROWS('Covid_Dataset'),'Covid_Dataset'[ASTHMA] = 1)

Total Cardio Vascular Patients = CALCULATE(COUNTROWS('Covid_Dataset'),'Covid_Dataset'[CARDIOVASCULAR] = 1)

Total COPD Patients = CALCULATE(COUNTROWS('Covid_Dataset'),'Covid_Dataset'[COPD] = 1)

Total Diabetes Patients = CALCULATE(COUNTROWS('Covid_Dataset'),'Covid_Dataset'[DIABETES] = 1)

Total Hypertension Patients = CALCULATE(COUNTROWS('Covid_Dataset'),'Covid_Dataset'[HIPERTENSION] = 1)

Total Immunosuppressed Patients = CALCULATE(COUNTROWS('Covid_Dataset'),'Covid_Dataset'[INMSUPR] = 1)

Total Obesity Patients = CALCULATE(COUNTROWS('Covid_Dataset'),'Covid_Dataset'[OBESITY] = 1)

Total Other Disease Patients = CALCULATE(COUNTROWS('Covid_Dataset'),'Covid_Dataset'[OTHER_DISEASE] = 1)

Total Patient Died = CALCULATE(COUNTROWS(Covid_Dataset),Covid_Dataset[Patient Survived] = 0)

Total Patient Survived = CALCULATE(COUNTROWS(Covid_Dataset),Covid_Dataset[Patient Survived] = 1)

Total Patients = COUNT(Covid_Dataset[Patient Survived])

Total Renal Chronic Patients = CALCULATE(COUNTROWS('Covid_Dataset'),'Covid_Dataset'[RENAL_CHRONIC] = 1)

Total Tobacco User Patients = CALCULATE(COUNTROWS('Covid_Dataset'),'Covid_Dataset'[TOBACCO] = 1)

