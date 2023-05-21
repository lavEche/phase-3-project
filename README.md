
### Predicting SyriaTel Customer Churn
![Screenshot (350)](https://github.com/lavEche/project-phase-1/assets/124572155/bd4df6fc-61f3-40fd-a5bf-4bbd098d0db2)

### Bussiness Understanding
This project aims to provide SyriaTel with a model to help predict whether a customer churn with SyriaTel, a telecommunications company.In an article about churn reduction in the telecom industry by the Database Marketing Institute,the artical states that "industry retention surveys have shown that while price and product are important, most people leave any service because of dissatisfaction with the way they are treated". With this in mind, we aim to highlight areas where customer service could be improved. Through research I find from this dataset, that SyriaTel has a churn rate of roughly 15% in customers who have been with the company for less than 245 days.

## Objectives:

This project aims to:

    - Provide inferential statistics and visualisations based on this data.
    - Create predictive, supervised learning models from the data to predict churn
    - Investigate labeled data on 3333 customers who have held accounts with the company for less than 243 days.

    
### Data:¶
This project utilises data from the https://www.kaggle.com/becksddf/churn-in-telecoms-dataset dataset from Kaggle.

The target variable in this dataset that we aimed to predict was identified as the churn column.

The features of this dataset include locational information (state and area_code) as well as plan details such as call minutes, charges, customer services calls and whether the customer had an international plan and/or voice mail plan. Our model iterations utilised subsets of these features as well as aggregations of these features to determine which features would best predict cusomter churn.
The raw, csv dataset can be downloaded directly from the kaggle website

# Description of data
> import pandas as pd 

import numpy as np 

import seaborn as sns 

import matplotlib.pyplot as plt 

import plotly.express as px 

from sklearn.model_selection import train_test_split,cross_val_score,GridSearchCV 

from sklearn.metrics import accuracy_score,f1_score,recall_score,precision_score,confusion_matrix,roc_curve,roc_auc_score,classification_report # performance metrics

from sklearn.preprocessing import MinMaxScaler 

from scipy import stats

from sklearn.inspection import permutation_importance

from sklearn.tree import DecisionTreeClassifier

from sklearn.ensemble import RandomForestClassifier

from sklearn.linear_model import LogisticRegression

from sklearn.neighbors import KNeighborsClassifier

import warnings

warnings.filterwarnings('ignore')

# loading data

df=pd.read_csv('bigml_59c28831336c6604c800002a.csv')

# cleaning data

>cleaned(df)

# Models used + Methodology:

#### Applying SMOTE Technique to Resolve Unbalanced 'churn' Feature

This algorithm will help to overcome the overfitting problem posed by random oversampling. It will focus on the feature space to generate new instances with the help of interpolation between the positive instances that lie together. It also aims to balance class distribution by randomly increasing minority class examples by replicating them.

![Screenshot (340)](https://github.com/lavEche/project-phase-1/assets/124572155/86bf9d82-9f86-470e-bc3a-ffe648fdb59a)

![Screenshot (341)](https://github.com/lavEche/project-phase-1/assets/124572155/fdf6a534-7a27-4377-affc-d2d67433c6c8)

This project tests a variety of classification models including:

    - Decisioin Tree Classifier
  
  ![Screenshot (348)](https://github.com/lavEche/project-phase-1/assets/124572155/34463c14-163c-49ea-aa67-294f4c230fb6)

    - Logistic Regression Classifier
    
    ![Screenshot (346)](https://github.com/lavEche/project-phase-1/assets/124572155/1c24f58e-e17f-4cc2-b4fa-692a70883efb)

    - Random Forest Classifer
  
  ![Screenshot (347)](https://github.com/lavEche/project-phase-1/assets/124572155/a41c25ab-34e2-48bc-9069-6e78ae95cf46)

1 evaluated the models based on the Roc curve.


![Screenshot (349)](https://github.com/lavEche/project-phase-1/assets/124572155/2bfedf70-1fc2-45a0-873e-6b8933558646)


The decision behind choosing to evaluate the model on ROC curve was made by considering comparison of the curves, which you can assess which model has a better discriminatory power in terms of distinguishing between churned and non-churned customers. Models with higher AUC values generally indicate better performance. 

# Results, Future Investigations and Recommendations:

#### Conclusion:

The best model to use is a Random Forest Classifier which produced a 0.914 ROC/AUC score on the test data of the model's predictions on the test data.


### Recommendations and Future Investigations.
1.Further investigate the characteristics of customers who made a high number of calls to customer service. 

2. Given the high churn rate (over 42%) among international plan holders, focus on retention efforts for these customers. 

3.  Investigate the states with high churn rates to identify any specific trends or issues causing the churn. Analyze factors such as pricing, competition, network coverage, or customer satisfaction levels in these states.

4. Consider segmenting customers based on their characteristics, usage patterns, or preferences. 

5. Focus on enhancing the overall customer experience across different touchpoints.

6.  Implement proactive communication and outreach strategies to engage customers and address their needs. 

7.  Establish a system for continuous monitoring of key metrics and customer feedback. 

    
