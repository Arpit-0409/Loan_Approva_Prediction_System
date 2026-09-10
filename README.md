# Loan_Approval_Prediction_System

Loan Approval System is a classification supervised Machine Learning prediction Model which takes input such as credit_score , debt-income-ratio , loan_amount , loan_term  etc. To predict whether an applicant 
should get loan approved or not.

main task of this model - is to minimize the high-risk customer who were previously getting approved.

features - 
Pipeline Integration: Processes input data using a pre-trained model.pkl handling encoding and scaling seamlessly.

Strict Feature Alignment: Enforces exact column order and data types required by the model.
Built-in Diagnostics: Includes script utilities to inspect model class mappings and decision thresholds.

Preprocessing - 
   There were around 5% missing values in every column so  i impute all the missing values
   with mean , knn and  random imputation and i found random imputation was giving best results as
   compared to other two because distrbution of data was almost same as it was before but in mean and  
    knn imputation distribution of data was changed.
    So i selected Random Imputation for Filling missing values


EDA - 

found a relationship b/w credit_score and loan_approved using Histogram -
 applicant whose credit_score was above 650 were getting loan_approved.

 on the other hand relationship b/w debt_income ratio and loan_approved using scatter histogram.
 applicant whose debt income ratio was less than 0.4 were getting loan_approved.


 Then train the model on three ML Algorthims
 Logistic Regression , KNN , NAIVE bayes.

 . LOGISTIC REGRESSION -
                           PRECISION WAS 89 % - means 89% rejecting  probability of high-risk customer.
                           RECALL was 72% - means detecting probability of
                           good customer.

2. K Nearest Neighbour -
                          Precision was 69% - means 77% rejecting probability of high-risk customer.
                          Recall was 50 % -  means detecting probability of good customer.

4.   NAIVE BAYES -
                           Precision was 89% - means 86% rejecting probability of high-risk customer.
                           Recall was 70 % -  means detecting probability of good customer


NOW  AFTER COMPARING ALL THE THREE RESULT WE FOUND KNN PERFORMS POORELY PRECISON IS QUITE NORMAL BUT RECALL IS VERY BAD IT NOT ABLE TO IDENTIFY GOOD CUSTOMERS .             BECAUSE WE HAVE SO MANY FEATURES IN OUR DATASET SO IT BECOME VERY DIFFICULT FOR KNN TO CALUCLATE DISTANCES B/W THEM . SO IT WILL NOT BE THE IDEAL CHOICE                     FOR LOAN APPPROVAL SYSTEM.



 NOW Logistic Regression and Naive bayes both are performing good but our main task is to minimize the precision but also to keep balance of recall score
 so finding out balance b/w precison and recall we use f1 score .
 
Later on i apply some feature engnieering technique to improve model's performance-

                
1. then i created more impact of credit score and debt income ratio by squaring them .
now precision is 88% but recall had a spike from 70% to 75% and f1 score is also 81 % which is quite good than Logistic regression

Therefore at the last we compare all of the confusion matrix of the model and found naive bayes was preidcting max values correct and also keeping the balance b/w precision(false positive) and recall(false negative)
    

   



