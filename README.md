# Stroke Prediction

## Overview
According to the World Health Organization (WHO), stroke is the 2nd leading cause of death globally, responsible for approximately 11% of total deaths.

This dataset is used to predict whether a patient is likely to get stroke based on the input parameters like gender, age, various diseases, and smoking status. Each row in the data provides relevant information about the patient.

## Results
- The current data indicates 95% of patients having No Stroke and only 5% of patients having a Stroke. 
- Based on the [Stroke Risk Scorecard](https://www.phoebehealth.com/services/stroke-treatment/neurosciences-stroke-risk-factors), most patients in this dataset were categorized as Caution (56%) meaning a risk score of between 4-6.
- Patients with High Risk included those who identified as having hypertension, diabetes, smoker, heart disease, overweight, female, and/or a history of stroke. The results indicated 25% of patients who were at high risk.
- The most notable stroke correlations were age, heart disease, hypertension, diabetic, and being overweight.
- 
- Data Preprocessing
- Compiling, Training, and Evaluating the Model

## Summary
Summarize results. Recommendation.

## Data Model Implementation
- [Kaggle Dataset](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset) was cleaned, normalized, and standardized prior to model using Spark SQL. 
    - Before:
    ![image](https://github.com/fiyang89/proj4-team6/assets/120594187/84e86d88-814f-4f28-b5e7-45d19537398d)


    - After:
    
    ![image](https://github.com/fiyang89/proj4-team6/assets/120594187/0cd60961-717b-4e94-a58a-23c405d9cabd)
    
- A Python script initialized, trained, and evaluated the model
    - Image of training models
    - Image of classification accuracy or r-squared

## Data Model Optimization
- The model was optimized resulting in changes in model performance using Python script.
    - Images of optimizations

## Data Model Visualization

![Stroke_NoStroke](https://github.com/fiyang89/proj4-team6/assets/120594187/dbe6f381-4321-463c-99df-6b8f02f042a7)

![Stroke_Risk_Outcomes](https://github.com/fiyang89/proj4-team6/assets/120594187/cc7a3d7f-d830-4985-8b1b-f5a20faccafd)

![Stroke_Correlation](https://github.com/fiyang89/proj4-team6/assets/120594187/a36cc390-6810-4750-a34d-424110df358e)

![AgeGender_Stroke_Risk_Outcomes](https://github.com/fiyang89/proj4-team6/assets/120594187/ed4bdf64-4872-4387-b3fe-48e181c1a897)

![AgeHeartDisease_Stroke_Risk_Outcomes](https://github.com/fiyang89/proj4-team6/assets/120594187/1a723b7d-7fae-4497-8600-01d525e0fd9f)

![AgeHypertension_Stroke_Risk_Outcomes](https://github.com/fiyang89/proj4-team6/assets/120594187/1265967a-91c4-4469-9c5f-233bf4d732d2)

![AgeDiabetes_Stroke_Risk_Outcomes](https://github.com/fiyang89/proj4-team6/assets/120594187/471a7c0e-83c1-4e4e-b402-c0a0760c78fe)

![AgeBMI_Stroke_Risk_Outcomes](https://github.com/fiyang89/proj4-team6/assets/120594187/2c727f99-86cc-4edb-93af-7e6740ae3c06)

Sources: [Kaggle Dataset](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset), [Stroke Risk Scorecard](https://www.phoebehealth.com/services/stroke-treatment/neurosciences-stroke-risk-factors), [Seaborn Documentation](https://seaborn.pydata.org/generated/seaborn.FacetGrid.html)
