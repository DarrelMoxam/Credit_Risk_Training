# Credit_Risk_Training
Mentor Project Classification modeling

 
 An IBM generated dataset of credit risk training redacted was given as the data set to work on, luckily didn’t 
have to source the dataset online but instead, it was provided as a CSV by my mentor.

 

 After reading in the data, I began with the basic EDA and observing the data to find any missing, 
 duplicate or messy data in the dataset. No missing values were detected but the data itself had duplicates but due 
 to the size, I decided to drop the few duplicates that were present as I thought it wouldn’t matter.

 

 After which I proceeded with the scaling of the data so It will be easier to model once its time. 
 After applying to scale it was time to split the data into test and train data and X and Y with X being the 
 features and y being the label which is necessary for modeling data.

 

 I was at a block in which I was confused as to what exactly to do next. I took some time and research on 
 how to execute specific models and what to notice when the model has run. The models I used were XGBOOST, SVC,
 Decision Tree Classifier, Random Forest Classifier, Logistic Regression, and SGDClassifier. For each of the models,
 I followed a specific pattern for the modeling. In a specific order, I fitted the model, predicted the model, 
 performed a confusion matrix, Cross-Validation score with k folds, did a classification report and finally the accuracy score. 
 This was done with all 6 models and each outcome was different than the other.

 

The Use case was to build classification models that would predict which customers should be accurately labeled as 
‘Risk’ or ‘No Risk’ and select the best model to use. Once all models were created I focused on the confusion matrix and 
classification report for each model. I decided to look into Type 1 and type 2 errors and from there I drew the conclusion 
that what I needed to focus on were the Specificity and Classification error. Classification Error definition is overall, 
how often is the classifier incorrect while Specificity is when the actual value is negative, how often is the prediction 
correct. All 5 had different results that viewed differents stats on the Classification Report and Confusion Matrix. 
The Decision tree had an accuracy level of 1 which is pretty good but it’s too perfect and the issue with is was the Training
accuracy dropped when applied. So I decided to go with the model that was second to that. Which was the RandomForestClassifer 
which had a Classification error of 0.0240722 and Precision of 0.9859578. The worst Classification model that was trained was 
the  SGDClassifier with a Classification error of 0.353059 and precision of 0.64694082.
