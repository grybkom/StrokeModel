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
- **StrokeDataCleaning.ipynb** - Downloads, explores, and cleans raw stroke data 'healthcare-dataset-stroke-data.csv'. Returns cleaned data in CSV format, 'stroke_clean.csv'.
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
  - Data is not balanced with most enties being labeled as not experiencing stroke.

![stroke_percentage](https://github.com/user-attachments/assets/cc2ed9d0-6060-4f09-841a-1be7e225c037)
![age_stroke_distribution](https://github.com/user-attachments/assets/f2c1869a-aae7-46dd-b361-2f7a4b3af679)

## Models
- StrokeModels.ipynb - loads cleaned data, 'stroke_clean.csv' and performs predictive modeling.
- Different Models were built and their performance metrics were compared, Logistic Regression, K-Nearest Neighbors (KNN), Support Vector Machine (SVM), Random Forest, and XGBoosted (XGB).
- Synthetic Minority Over-sampling Technique (SMOTE) was applied to the training data to compensate for the class imbalance and all the models were assess again with the over-sampled data.

## Results
- Some of the models, such as logistical regression, achieved a very high accuracy with the original (not over-sampled) data. However, this is because these models were simply labeling everything as not stroke.

- The best model as far as detecting stroke was the SVM trained on over-sampled data. 
![confussion_matrix_svm](https://github.com/user-attachments/assets/7f44464f-7996-4324-9474-555c178f41c5)
![confussion_matrix_svm_smote](https://github.com/user-attachments/assets/90baeee6-65df-4616-aa9b-083b0949ae23)

## To Do
- [ ] Assess class weighting to address class imbalance.
- [ ] Assess [SMOTEENN](https://imbalanced-learn.org/stable/references/generated/imblearn.combine.SMOTEENN.html) to address class imbalance.
- [ ] Apply grid search for hyperparameters max_depth, learning_rate, and n_estimators for XGB model.
- [ ] Apply grid search for hyperparameters C, gamma, and kernel for SVM model. 

## Reference
U.S. Department of Health and Human Services. (2023, June 12). Stroke. 
National Institute of Neurological Disorders and Stroke
https://www.ninds.nih.gov/health-information/disorders/stroke 


