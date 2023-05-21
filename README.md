
### Predicting SyriaTel Customer Churn¶

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

# Models used + Methodology:

This project tests a variety of classification models including:

    - Decisioin Tree Classifier
    - Logistic Regression Classifier
    - Random Forest Classifer
   
1 evaluated the models based on the Roc curve.

The decision behind choosing to evaluate the model on ROC curve was made by considering comparison of the curves, which you can assess which model has a better discriminatory power in terms of distinguishing between churned and non-churned customers. Models with higher AUC values generally indicate better performance. 

# Results, Future Investigations and Recommendations:

#### Best model:

Our best model was a Random Forest Classifier which produced a 0.914 ROC/AUC score on the test data of the model's predictions on the test data.


### Recommendations and Future Investigations.
1.Further investigate the characteristics of customers who made a high number of calls to customer service. 
2. Given the high churn rate (over 42%) among international plan holders, focus on retention efforts for these customers. 
3.  Investigate the states with high churn rates to identify any specific trends or issues causing the churn. Analyze factors such as pricing, competition, network coverage, or customer satisfaction levels in these states.
4. Consider segmenting customers based on their characteristics, usage patterns, or preferences. 
5. Focus on enhancing the overall customer experience across different touchpoints.
6.  Implement proactive communication and outreach strategies to engage customers and address their needs. 
7.  Establish a system for continuous monitoring of key metrics and customer feedback. 

    
