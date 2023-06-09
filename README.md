# Stroke Prediction

## Overview
According to the World Health Organization (WHO), stroke is the 2nd leading cause of death globally, responsible for approximately 11% of total deaths.

This dataset is used to predict whether a patient is likely to get stroke based on the input parameters like gender, age, various diseases, and smoking status. Each row in the data provides relevant information about the patient.

## Results
- The current data indicates 95% of patients having No Stroke and only 5% of patients having a Stroke. 

![Stroke_NoStroke](https://github.com/fiyang89/proj4-team6/assets/120594187/dbe6f381-4321-463c-99df-6b8f02f042a7)

- Based on the [Stroke Risk Scorecard](https://www.phoebehealth.com/services/stroke-treatment/neurosciences-stroke-risk-factors), most patients in this dataset were categorized as Caution (56%) meaning a risk score of between 4-6.
- Patients with High Risk included those who identified as having hypertension, diabetes, smoker, heart disease, overweight, female, and/or a history of stroke. The results indicated 25% of patients who were at high risk.

![Stroke_Risk_Outcomes](https://github.com/fiyang89/proj4-team6/assets/120594187/cc7a3d7f-d830-4985-8b1b-f5a20faccafd)

- The most notable stroke correlations were age, heart disease, hypertension, diabetic, and being overweight.

![Stroke_Correlation](https://github.com/fiyang89/proj4-team6/assets/120594187/a36cc390-6810-4750-a34d-424110df358e)

- Females were clearly correlated with stroke outcome compared to males.

![AgeGender_Stroke_Risk_Outcomes](https://github.com/fiyang89/proj4-team6/assets/120594187/ed4bdf64-4872-4387-b3fe-48e181c1a897)

- Individuals who had heart disease were 80% likely to be at high risk for stroke.

![AgeHeartDisease_Stroke_Risk_Outcomes](https://github.com/fiyang89/proj4-team6/assets/120594187/1a723b7d-7fae-4497-8600-01d525e0fd9f)

- Individuals who had hypertension were 75% likely to be at a high risk for stroke.

![AgeHypertension_Stroke_Risk_Outcomes](https://github.com/fiyang89/proj4-team6/assets/120594187/1265967a-91c4-4469-9c5f-233bf4d732d2)

- Prediabetic and Diabetic were more likely to have a higher possibility of stroke as most individuals were either caution or high risk. 

![AgeDiabetes_Stroke_Risk_Outcomes](https://github.com/fiyang89/proj4-team6/assets/120594187/471a7c0e-83c1-4e4e-b402-c0a0760c78fe)

- Similar to diabetes outcome, individuals who were overweight, obese, or extremely obese fell into caution or high risk for stroke.

![AgeBMI_Stroke_Risk_Outcomes](https://github.com/fiyang89/proj4-team6/assets/120594187/2c727f99-86cc-4edb-93af-7e6740ae3c06)


## Summary
Summarize results. Recommendation.

## Data Model Implementation
- [Kaggle Dataset](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset) was cleaned, normalized, and standardized prior to model using Spark SQL. 
    - Before: 
    
    ![image](https://github.com/fiyang89/proj4-team6/assets/120594187/84e86d88-814f-4f28-b5e7-45d19537398d)


    - After:
    
    ![image](https://github.com/fiyang89/proj4-team6/assets/120594187/0cd60961-717b-4e94-a58a-23c405d9cabd)
    
- Utilized get_dummies within Pandas to encode our categorical variables into numerical ones.
    - Unbalanced Dataset: As eluded earlier in this report, our dataset was very imbalanced with 95% of the data with no stroke values. 
    - Balancing Techniques: We used SMOTE (Synthetically creates training data for minority class) and Random undersampling (undersamples majority class) to get a more balanced train set to train our data.
- Base Model Testing: Running base model testing with the same model architecture to find the ideal balancing technqiue.
    - Original unbalanced dataset, SMOTE technqiue and Random Under sampling technique.<br>
    
    ![Base Architecture](https://github.com/fiyang89/proj4-team6/blob/main/Images/Base_Model_Arch.png)
    <br>
    Resulted: Random Undersampling having the better ROC Score and Accuracy score relative to SMOTE technique:<br>
    ![Results](https://github.com/fiyang89/proj4-team6/blob/main/Images/Base_Model_Scores.png)
## Data Model Optimization
- The model was optimized resulting in changes in model performance using Python script.
    - Images of optimizations

## Sources
- [Kaggle Dataset](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset)
- [Stroke Risk Scorecard](https://www.phoebehealth.com/services/stroke-treatment/neurosciences-stroke-risk-factors)
- [Seaborn Documentation](https://seaborn.pydata.org/generated/seaborn.FacetGrid.html)
