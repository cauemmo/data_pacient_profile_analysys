# Data Project Documentation: Patient Profile Analysis with Heart Diseases
![image](https://github.com/user-attachments/assets/a84266c4-266a-42fa-96c2-f151b50b20da)

### Table of Contents
- [Context and Overview](#context-and-overview)
- [Data Structure Overview](#data-structure-overview)
- [Executive Summary](#executive-summary)
- [Detailed Insights](#detailed-insights)
- [Recommendations for Next Steps](#recommendations-for-next-steps)
- [Streamlit Application](#streamlit-application)
- [Technical and Exploratory Data Analysis](#technical-and-exploratory-data-analysis)

# Context and Overview
The analysis was conducted to address a critical issue faced by the organization: how to identify the main risk factors for heart disease in different population groups and prioritize preventive initiatives. The increasing costs associated with cardiovascular disease treatments and the high prevalence of related conditions emphasize the need for a data-driven approach to improve health outcomes and reduce expenses. The organization seeks to understand behavioral patterns and clinical characteristics contributing to the increase in heart disease cases. Factors such as age, gender, blood pressure, and lifestyle habits (e.g., smoking and physical activity) are essential for creating an efficient prevention plan.

### Business Questions:
#### Risk Factors Analysis: 
- What are the main risk factors associated with heart disease in the analyzed population?
#### Cholesterol Impact: 
- Is there a significant relationship between elevated cholesterol levels and the presence of heart disease?
#### Vulnerable Groups: 
- Which groups (segmented by age, gender, or behavior) are most vulnerable?
#### Lifestyle Influence:
- How do lifestyle factors (e.g., smoking, alcohol consumption, and physical activity) influence cardiovascular risk?
#### Campaign Targeting:
- Which campaigns should we focus on to maximize preventive impact? 

## Relevant Links:
- Interactive Dashboard:
- Analysis Notebooks: 

# Data Structure Overview
The dataset contains 70,000 records and 13 columns, as described below:
- id: Unique identifier.
- age: Age in days.
- gender: Gender (1 for female, 2 for male).
- height: Height in cm.
- weight: Weight in kg.
- ap_hi: Systolic blood pressure.
- ap_lo: Diastolic blood pressure.
- cholesterol: Cholesterol level (1: normal, 2: above normal, 3: much above normal).
- gluc: Glucose level (1: normal, 2: above normal, 3: much above normal).
- smoke: Smoker (0: no, 1: yes).
- alco: Alcohol consumption (0: no, 1: yes).
- active: Physical activity (0: no, 1: yes).
- cardio: Heart disease diagnosis (0: no, 1: yes).
  
#### Entity-Relationship Diagram (ERD): 

![Captura de Tela (810)](https://github.com/user-attachments/assets/960eea40-4a98-4d88-b6b1-3b6bfb128494)


# Executive Summary
The main insights obtained include:
#### 1.	Risk Factors Analysis: 
- The most relevant risk factors for heart disease are elevated BMI, high blood pressure, and obesity. Individuals with elevated BMI have a 76% prevalence of heart disease, indicating a direct relationship between body weight and cardiovascular risk.
![image](https://github.com/user-attachments/assets/9d0e1048-91ee-4f1b-ad3e-2f9d67caed7f)


#### 2.	Cholesterol Impact: 
- There is a strong relationship between elevated cholesterol and heart disease. Individuals with above-normal cholesterol levels have a 36% higher prevalence of heart disease compared to those with normal cholesterol levels.
  ![image](https://github.com/user-attachments/assets/f1cc6369-3589-4a8f-890f-e118fc1b8e8b)
#### 3.	Vulnerable Groups: 
- Individuals over 60 years old represent 35% of heart disease cases, while those under 40 years old represent only 5%. Men have a slightly higher risk (52%) compared to women (48%).
  ![image](https://github.com/user-attachments/assets/10016dd8-7e20-407f-971e-a1dfac5453a9)

#### 4.	Lifestyle Influence:
- Physically inactive individuals have an 8% higher prevalence of heart disease compared to active individuals. Interestingly, smokers showed a 3% lower prevalence compared to non-smokers, which may indicate bias or underlying factors.
  ![image](https://github.com/user-attachments/assets/fcb939f1-3fff-4917-8c13-32600f9795db)

#### 5.	Prediction Model Insights:
- The prediction model highlights that BMI, high blood pressure, and age are the most important factors in identifying heart disease risks.
  ![Captura de Tela (804)](https://github.com/user-attachments/assets/e8990312-b2cb-41d0-bde1-5ff4d65e1f3a)

#### 6.	Campaign Targeting:
- Campaigns should prioritize groups with elevated BMI, hypertension, and physical inactivity. Additionally, it is essential to implement initiatives focused on older populations and educate about the importance of maintaining a healthy weight.


# Statistical Breakdown


Specific analyses based on executive summary aspects:
![Captura de Tela (811)](https://github.com/user-attachments/assets/9de5a9b7-79f5-411c-b231-f31b22433dfb)
#### Cholesterol and Heart Disease: 
- The overall average cholesterol level in the population is 1.37, with a standard deviation of 0.68. Individuals with a positive diagnosis have an average cholesterol level of 1.87, significantly higher than those without a diagnosis (1.12).
#### Blood Pressure: 
- The average systolic blood pressure is 128.8 mmHg. Individuals with pressure above 140 mmHg have a 68% prevalence of heart disease.
#### Physical Activity: 
- 80.4% of the population is physically active. Among the inactive population (19.6%), the prevalence of heart disease is 8% higher.
#### Confusion Matrix: 
- Indicates 3418 false negatives, suggesting improvements in the model to reduce prediction errors.
  ![Captura de Tela (806)](https://github.com/user-attachments/assets/7e46370a-91c3-44c3-9ab3-960b05b937ee)

#### ROC Curve: 
- The AUC of 0.79 reflects good overall model performance but indicates room for improvement.
![Captura de Tela (805)](https://github.com/user-attachments/assets/0e959ab6-eb29-4518-9195-ee427d70ccb9)

# Recommendations for Next Steps
#### Risk-Focused Campaigns: 
- Develop personalized campaigns for individuals with elevated BMI and hypertension, emphasizing the importance of lifestyle changes to reduce cardiovascular risks.
#### Corporate Initiatives: 
- Establish partnerships with companies to offer health and wellness programs for employees. Benefits such as regular screenings and gym access can improve workers' health indicators.
#### Physical Activity Incentives: 
- Launch free community programs, such as group walks or sports events, to encourage healthy habits in less active communities.
#### Healthy Eating Promotion: 
- Partner with the food industry to increase the availability of healthy options in supermarkets and restaurants, along with clear labels promoting cardiovascular benefits.
#### Regional Monitoring: 
- Identify regions with a higher prevalence of risk factors and allocate resources to these areas, promoting localized initiatives tailored to community needs.

#### These recommendations were adjusted to offer practical and strategic solutions aligned with the business context, aiming to reduce the prevalence of heart disease and improve population outcomes.

# Streamlit Application
- In this project phase, an interactive application was developed where users can input their personal and health information through a form. The information requested in the form includes all the features used during the model training, such as weight, age, blood pressure (both systolic and diastolic), cholesterol levels, glucose, and other variables related to cardiovascular risk factors. The objective of this application is to allow users to enter their data and, based on the information provided, the model predicts the probability of developing heart disease. Through this interaction, users receive a personalized and immediate prediction directly related to their individual risk factors.
![image](https://github.com/user-attachments/assets/5cedab3a-e056-43e7-a78f-2bbee95e9375)
- In addition to the percentage prediction of the likelihood of developing heart disease, the application was configured to provide personalized tips based on the risk level identified by the model. The risk level is divided into three main categories: low, medium, and high. Depending on the probability calculated by the model, the user receives specific guidance suitable for their risk level. These tips aim to help the user better understand their situation and take appropriate action based on the results obtained. Thus, the application not only provides a quantitative prediction but also offers recommendations that can assist in preventing or managing risk factors, depending on the profile identified.
![image](https://github.com/user-attachments/assets/b220b5b3-b641-452c-bb7b-1bab8f25a702)

# Technical and Exploratory Data Analysis

### Data Cleaning Process

During the data preparation process, the following steps were carried out to ensure the quality and consistency of the information:

#### Data Loading Correction:
- The data loading was adjusted using the correct separator (';'), ensuring the proper delimitation and structuring of the columns.
#### Age Conversion:
- Age, originally stored in days, was converted to years to facilitate interpretation and data analysis.
#### Unrealistic Value Treatment:
- Records with values outside acceptable limits for certain variables were removed:
  - Height: limited to values between 140 and 200 cm.
  - Weight: restricted to values between 40 and 200 kg.
  - Systolic Blood Pressure: values between 80 and 220 mmHg.
  - Diastolic Blood Pressure: values between 40 and 120 mmHg.
It was also ensured that systolic pressure was greater than diastolic pressure in all records.
#### Removal of Null Values and Duplicates:
- All records with missing values in any relevant column were removed.
- Duplicates were eliminated to avoid counting identical information repeatedly.
#### Outlier Treatment:
- Extreme outliers in continuous variables were identified and removed based on statistical techniques such as the interquartile range (IQR).
#### Gender Reclassification:
- Gender was mapped to binary values (0 and 1), simplifying analysis.
#### Impact of Cleaning:
After the cleaning process, the dataset was reduced from 70,000 to 68,424 records. This represented a reduction of approximately 2.3%, eliminating potentially problematic data such as unrealistic values, incomplete records, and duplicates. This process was essential to ensure the integrity of subsequent analyses.

### Correlation Analysis
![image](https://github.com/user-attachments/assets/0cd17526-46e5-4812-a32b-06361a7f60a7)
#### Weight and BMI:
- The strongest correlation found was between weight and body mass index (BMI), with a correlation coefficient of 0.86. This result is expected since BMI is directly calculated from an individual's weight and height. Such a high correlation indicates that as weight increases, BMI also significantly increases, reinforcing the importance of weight control for maintaining a healthy BMI.
#### Blood Pressure and Heart Disease:
- A strong positive correlation was observed between systolic blood pressure (ap_hi) and diastolic blood pressure (ap_lo), with a correlation coefficient of 0.67. This correlation indicates that, generally, when systolic pressure is high, diastolic pressure also tends to be high. This behavior is consistent with the physiology of the cardiovascular system, where both types of blood pressure are influenced by common factors such as vascular resistance and blood volume.
#### Cholesterol and Glucose:
- Among metabolic factors, the correlation between cholesterol and glucose was moderate, with a coefficient of 0.45. Patients with elevated cholesterol levels tend to have elevated glucose levels, suggesting a possible relationship between dyslipidemia and glycemic dysregulation. This correlation highlights the importance of an integrated approach in managing metabolic risk factors to prevent cardiovascular disease.
#### Smoking and Gender:
- Another relevant point is the correlation between smoking and gender, which was 0.34. This moderate value indicates that one gender has a higher prevalence of smokers. This information can be crucial for directing smoking cessation campaigns and gender-based interventions.
#### Weight and Blood Pressure:
- Additionally, a weak correlation was observed between weight and systolic blood pressure, with a coefficient of 0.26. Although the correlation is smaller, it suggests that an increase in weight may be associated with an increase in systolic blood pressure, highlighting the importance of weight control for cardiovascular health.
#### Age and Blood Pressure:
- The correlation between age and systolic blood pressure was also weak, with a coefficient of 0.20. This indicates that as age increases, there is a tendency for systolic blood pressure to rise, although this relationship is not very strong. This finding is consistent with the general trend of increasing blood pressure with aging.
#### Age and Cardiovascular Disease:
- Finally, the correlation between age and the presence of cardiovascular disease was 0.24. Although weak to moderate, this correlation suggests that the likelihood of developing cardiovascular diseases slightly increases with age. This finding is important for developing prevention strategies targeting older populations.

