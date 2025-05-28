# Stroke Prediction Models
Machine Learning Models for Stroke Prediction
---

## Background
The focus of this project is to build supervised models that predict stroke. 
Stroke is when there is an abrupt disruption of blood flow to the brain. 
This is caused by blood vessel blockage, narrowing or bursting. 
According to the Nation Institutes of Health (NIH), nearly 800,000 Americans suffer a 
stroke every year, with some of these cases being fatal. 
If an individual survives a stroke, the neurological effects can be mild to severe, 
and may include cognitive decline, movement problems and emotional dysregulation. 
The NIH lists several risk factors for stroke, some of which are unmodifiable, 
and some can be modified. 

## Language
- Python
  - [NumPy](https://numpy.org/)
  - [pandas](https://pandas.pydata.org/)
  - [statsmodels](https://www.statsmodels.org/stable/index.html)
  - [Scikit-learn](https://scikit-learn.org/stable/)
  - [Seaborn](https://seaborn.pydata.org/)
  - [Matplotlib](https://matplotlib.org/)

## Data 

- Stroke Dataset is available through Kaggle: 
  - Fedesoriano. (2020). Stroke Prediction Dataset. 
  - Retrieved from https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset.
- StrokeDataCleaning.ipynb - Downloads, explores, and cleans raw stroke data 'healthcare-dataset-stroke-data.csv'. Returns cleaned data in CSV format, 'stroke_clean.csv'.
  - Features before cleaning
    - id: unique identifier
    - gender: "Male", "Female" or "Other"
    - age: individual's age
    - hypertension: 1 if the individual has hypertension 0 if not
    - heart_disease: 1 if the individual has heart disease 0 if not
    - ever_married: "No" or "Yes"
    - work_type: "children", "Govt_jov", "Never_worked", "Private" or "Self-employed"
    - bmi: body mass index
    - Residence_type: "Rural" or "Urban"
    - avg_glucose_level: average blood glucose level 
    - smoking_status: "formerly smoked", "never smoked", "smokes" or "Unknown"*
    - stroke: 1 if the individual suffered a stroke and 0 if not
  - Entries containing NA and Unknown were removed
  - Categorical features were converted to binary integers using [Pandas get_dummies function](https://pandas.pydata.org/docs/reference/api/pandas.get_dummies.html)
  - Data is not balanced with most enties being labeled as not experiencing stroke
     ![Stroke Percentage](https://github.com/user-attachments/assets/f01fa3fc-c431-4f3b-9703-7e6960cd737d)


## Reference
U.S. Department of Health and Human Services. (2023, June 12). Stroke. 
National Institute of Neurological Disorders and Stroke
https://www.ninds.nih.gov/health-information/disorders/stroke 


