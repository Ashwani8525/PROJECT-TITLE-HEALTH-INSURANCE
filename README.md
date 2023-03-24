# PROJECT-TITLE-HEALTH-INSURANCE
HEALTH INSURANCE CROSS SELL PREDICTION

# PROBLEM DISCRIPTION


Our client is an insurance company that has provided Health Insurance to it's customers. now they need your help in building a model to predict whether the policyholders (customers) from the past year will also be interested in Vehicle insurance provided by the company. An insurance policy is an agreement by which a company undertakes to provide a guarantee of compensation for specified loss, damage, illness, or death in return for the payment of a specified premium. A premium is sum of money that the customer needs to pay regularly to an insurance company for this guarantee. For example, you may pay a premium of a Rs. 5000 each year for a health insurance cover of Rs. 200,000/- so that if, God forbid, you fall ill and need to be hospitalised in that year, the insurance premium will bear the cost of hospitalisation etc. for upto Rs. 200,000. Now, if you are wondering how can company bear such high hospitalisation cost when it charges a premium of only Rs. 5000/-, that is where the concept of probabilities comes in picture. For example, like you, there may be 100 customers who would be paying a premium of Rs. 5000 every year, but only a few of them (say 2-3) would get hospitalized that year and not everyone.This way everyone shares the risk of everyone else. Just like medical insurance, there is vehicle insurance where every year customer needs to pay a premium of certain amount to insurance provider company so that in case of unfortunate accident by the vehicle, the insurance provider company will provide a compensation (called 'sum assured') to the customer. Building a model to predict whether a customer would be interested in vehicle insurance is extremely helpful for the company because it can then accordingly plan its communication strategy to reach out to those customers and optimise its business model and revenue. Now, in order to predict, whether the customer would be interested in Vehicle insurance, you have information about demographics (gender, age, region code), Vehicles(Vehicle age, Damage), Policy (Premium, sourcing channel),etc.





# Business Goal


Building a model to predict whether a customer would be interested in Vehicle Insurance is extremely helpful for the company because it can then accordingly plan its communication strategy to reach out to those customers and optimise its business model and revenue.



# Data Discription



The Dataset used for the analysis includes the following columns:

id : Unique ID for the customer

Gender : Gender of the customer

Age : Age of the customer

Driving_License : 0 - Customer does not have DL,1 - Customer already has DL

Region_Code : Unique code for the region of the customer

Previously_Insured : 1 - Customer already has Vehicle Insurance, 0-Customer doesn't have Vehicle Insurance

Vehicle_Age : Age of the Vehicle Vehicle_Damage : 1 - Customer got his/her vehicle damaged in the past. 0 -Customer didn't get his/her vehicle damaged in the past.

Annual_Premium : The amount customer needs to pay as premium in the year

PolicySalesChannel : Anonymized Code for the channel of outreaching to the customer ie. Different Agents, Over Mail, Over Phone, In Person, etc.

Vintage : Number of Days, Customer has been associated with the company

Response : 1 - Customer is interested, 0 - Customer is not interested


# METHODS USED

Descriptive Statistics

Data Visualization

Machine Learning

# TECHNOLOGIES
Python

Pandas

Numpy

Matplotlib

Seaborn

Scikit-learn

XGBoost

# Execution Instruction

The order of execution of the program files is as follows:

HEALTH INSURANCE CROSS SELL PREDICTION.ipynb
HEALTH_INSURANCE_CROSS_SELL_PREDICTION.ipynb contains the entire code for Data exploration/Data processing/transformation/model development

# BEST MODEL



From all the above models that we tried to train and predict the output, we can conclude that Bagging Classifier is the best model for our data set. The best parameter of this model is {'n_estimators': 200}. Its Accuracy Score is 0.85, Precision is 0.31, Recall is 0.15, F1_Score is 0.20, ROC_AUC_Score is 0.55 and Log_Loss is 4.98. Its Elapsed time is 03 minutes and 21 seconds.

We can see that we have other models with higher Accuracy Score than Bagging Classifier. But the problem with those models is, their Precision and Recall values are zero which means True Positives are zero. That means those models are unable to predict correct output if any customer is ready to take vehicle insurance. And as we all know, classification accuracy alone can be misleading if you have an unequal number of observations in each class. This is exactly the case with our data set.

Hence, Bagging Classifier is the best model for our data set.

NOTE: You might get a slight difference in result every time you run because we are using Halving_Randomized_Search_CV to perform hyperparameter tunning which randomly selects the combination of parameters to tune the model.



# CONCLUSION



Through Exploratory Data Analysis, we categorized Age as YoungAge, MiddleAge, and OldAge, then we categorized the Region_Code as Region_A, Region_B, Region_C. We categorized the Policy_Sales_Channel into channel_A, channel_B, channel_C. Further, we observed that customers belonging to youngAge are more interested in vehicle response. We observed that customers having vehicles older than 2 years are more likely to be interested in vehicle insurance. Similarly, customers having damaged vehicles are more likely to be interested in vehicle insurance.

Further, we applied Machine Learning Algorithms to determine whether a customer would be interested in Vehicle Insurance

There was overfitting issues while using Random forest method. We tackled that with hyperparameter tuning.
Annual Premium column has the highest importance among all the features.
We are getting 85% accuracy for both test and train dataset while using Random Forest model with hyperparameter tuning.
Hence, we can deploy this model

# References
https://towardsdatascience.com

https://www.analyticsvidhya.com

https://machinelearningmastery.com
