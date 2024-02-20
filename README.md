# Predictive-Analytic-Project---NYP

**Project Title**: Predictive Analytic Project<br/>
**Date Completed**: 23-08-2022<br/>
**Team Members**: Shermaine, Rawtbhik, Shi Min, Zhang Xiang<br/>

## Tasks
1. Collect data from multiple sources using appropriate collection tools and techniques that comply with data and privacy ethics.
2. Perform data pre-processing techniques to impute data, transform, reshape and protect the data in accordance with the business requirements and data protection principles.
3. Apply relevant predictive modelling techniques to predict the desired business outcomes to meet the service expectation of the key stakeholders.
4. Work collaboratively in a team to develop dashboards using data storytelling approach for an effective narrative and visual representation of their predictive analytics project.

## Project Scope & Scenario
Predictive analytics plays an important role in helping organizations make critical business decisions based on insights and information derived from collected data. Today, given some conditions, businesses want to know what is mostly likely to happen and identify actions that maximizes desirable outcomes. This is taking place across multiple industries, for example, healthcare, manufacturing, finance, retail, marketing manufacturing, human resources, cyber security and education.

In this project, you are to develop a predictive analytics model using the skills you have acquired in the other units:
- data collection/wrangling to develop effective data storytelling visualization and dashboards.
- Predictive models using supervised and/or unsupervised learning techniques.
- Protection of data privacy.

### Project Requirements
![Screenshot 2022-09-07 182406](https://user-images.githubusercontent.com/98081173/188855764-09cf787f-86ff-4aa8-a616-7d955fe54708.png)

## Business Objectives
In the present situation, our main objective is to propose a project to develop categorical predictive models of 85% accuracy to detect common health problems in our global population and the factors contributing to those health issues. As health problems are on the rise, our team believes that early detection and response are essential and a vital part of providing healthcare services with accuracy and effectiveness. Additionally, these predictions will help pinpoint factors associated with major health problems, so that potential patients will be aware of them and take preventive measures to avoid becoming victims of such problems. 

Due to a shortage of healthcare professionals, it will also be difficult to provide high-quality and accurate care to every patient. Hence, we are confident that our machine learning techniques will be able to detect health problems more accurately through algorithms and computer analysis, thereby reducing healthcare stress, delayed detection and human error.

## Empathy
**Engage** - During our interviews with the two doctors mentioned above, we found that strokes and diabetes are on the rise, requiring prompt and accurate detection.

**Observe** - Looking at our current healthcare conditions, especially with infectious diseases on the rise, we see that the healthcare industry is severely understaffed, so they will need help detecting common health problems to reduce their workload, checking and recommending each patient.

## Main & Sub Tasks
Main Task
Determine the important factors that contribute to an individual getting common health problems
> - Data Collection 
> - Data Understanding
> - Data Cleaning / Pre-processing
> - Data Modelling
> - Report Writing
Sub-Task
-	Provide final predictive of at least 85% accuracy 
-	Identify business objectives
    -	Select our datasets to use
    - Determine which industry we want to work with 
    - Consult industry professionals 
- Prepare data for modelling 
    - Data visualisation and understanding using software tools mentioned here 
    - Select which variables to use
- Data modelling 
    - Focusing on logistic regression, support vector machine, decision tree/ random forest, neural network and with the help of SAS Viya, we will train, test and tune our models to provide our most accurate and effective model for recommendations
- Report writing 
    - Document down our process throughout this project 
    - Combine our different models and documentations
    - Set and meet timelines (Gantt Chart)
- Final presentation 
    - Finalising and selecting best model 
    - Prepare slides and rehearsal


## Data Collection and Exploration
As we have found out that stroke and diabetes are on the rise, we have decided to split the task to focus on these two health conditions. Stroke will be done and documented by Shi Min and Shermaine, while Diabetes will be done and documented by ZhangXiang and Rawtbhik. The data collected and prepared are sourced from Kaggle and the individual selected data source can be found below: 
- Stroke – Stroke Prediction|Visualization & Prediction
- Diabetes –   Diabetes Prediction | BRFSS2015 (https://www.cdc.gov/brfss/annual_data/annual_2015.html)

### Diabetes
This Behavioural Risk Factor Surveillance System (BRFSS) dataset is administered and supported by CDC's Population Health Surveillance Branch, under the Division of Population Health at the National Centre for Chronic Disease Prevention and Health Promotion.
The BRFSS dataset that we have obtained is an ongoing surveillance system designed to measure behavioural risk factors for the non-institutionalised adult population (aged 18 years of age and older) residing in the United States.
This dataset contains 441,455 responses and has 330 features (columns). These features are either questions directly asked of participants or calculated variables based on individual participant responses.
There are features that include tobacco use, HIV/AIDS knowledge and prevention, exercise, immunisation, health status, healthy days, health-related quality of life, health care access, hypertension awareness, arthritis burden, chronic health conditions, alcohol consumption, fruits and vegetable consumption, and seatbelt use.
This data is helpful in identifying the numerous preventive health practices and risk behaviours that are linked to chronic diseases, injuries, and preventable infectious diseases that affect the population. 
However, based on professional opinions and some diabetes disease research done regarding factors influencing diabetes and other chronic health conditions, we have reasons to believe that the selected desirable features (columns) that we have chosen would help us achieve the ideal analysis goal that we have in mind.

## Data Understanding
Based on professional opinions and some diabetes disease research done regarding factors influencing diabetes and other chronic health conditions, we have reasons to believe that the selected desirable features (columns) that we have chosen would help us achieve the ideal analysis goal that we have in mind.

Dataset was understood through a codebook example as below:

![Codebook](https://user-images.githubusercontent.com/98081173/188919870-e82e5b6b-1549-4bfd-8224-3542e71e67a9.png)


![Tableau](https://user-images.githubusercontent.com/98081173/188919468-7944725f-c659-4387-a0a1-a5b265f762df.png)

Data was observed through chart created with Tableau and documented as below.
This chart above shows us the number of respondents who are diagnosed with diabetes, non-diabetics and borderline diabetes.
> - Value 1 is respondents with diabetes (male and female).
> - Value 2 are female respondents only who say they were told that they were diagnosed with diabetes during pregnancy.
> - Values 3 & 4 are respondents who do not have diabetes or are experiencing borderline diabetes.
Since our target variable is to produce a binary outcome, we will reduce it to 2 values by creating values 1 and 0.  1 for respondents with diabetes and 0 for non-diabetics.
As shown in the chart above it was found that there are values like “Null”, 7 which represents “Don’t Know”/”Not Sure” and 9 represents “Refused to answer”. These data recorded down would not generate any useful findings. Only data that is able to tell if a person has or does not have diabetes are considered to support our modelling.

In summary, the following columns need to be cleaned after doing visualisation on the uncleaned dataset:
1.	Diabetes (DIABETE3)
2.	Diets (_FRTLT1, _VEGLT1)
3.	Smoking (SMOKDAY2, SMOKER3)
4.	High Blood Pressure ( _RFHYPE5)
5.	High Cholesterol (_RFCHOL)
6.	Alcohol Consumption (_RFDRHV5)
7.	Other Chronic Health Conditions (CVDSTRK3, CVDRHD4, HAVARTH3)
8.	General/Mental Health (DIFFWALK, PACAT1, DECIDE, ADDEPEV2)
9.	Demographics (SEX, AGEG5YR, _BMI5)


## Data Preperation/Cleaning
Under the section on data cleaning, KNIME was used to clean our dataset which contains 441,455 responses and has 330 features (columns). After cleaning, only 130,260 responses and 20 features remain including an additional column “Partition” added to partition our data into “Testing” and “Training” Set.  
Below is an overview of the process of data cleaning:
![Cleaning1](https://user-images.githubusercontent.com/98081173/188920614-af2dd5ef-136f-4321-a65b-f06bff8d819a.png)
![Cleaning2](https://user-images.githubusercontent.com/98081173/188920635-4b7fcc90-ce28-4da3-87d2-a5383aad18cc.png)

### Steps taken:
1.	Variable Selection
2.	Data Transformation
3.	Generate an Unbalanced dataset with Partitioning.
4.	Generate a Balance dataset with Partitioning
5.	Generate Clean Dataset
6.	Selecting Dataset [Balanced Vs Unbalanced]

In the end, balanced dataset was selected for modelling, as it return a better result.

## Modelling

Via SAS Viya


