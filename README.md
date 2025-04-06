Jupiter Notebook : https://github.com/sonia-james/AIMLModule17/blob/main/Bank_Subscription_Analysis.ipynb
# 1. Business Understanding
Objective: The goal of this project is to predict whether a customer will subscribe to a term deposit based on various features, such as the client's personal information, contact details, and campaign characteristics. The data is related to phone calls made during a direct marketing campaign by a Portuguese banking institution.

### Business Problem:

The bank wants to increase the efficiency of its marketing campaigns. By predicting whether a client will subscribe to a term deposit based on past interactions and client information, the bank can focus resources on high-potential leads, improving conversion rates and minimizing marketing costs.
Goal: Build a predictive model that can classify whether a customer will subscribe to a term deposit (the target variable y). The model should aim to accurately predict this binary outcome.

# 2. Data Understanding
Data Collection: The dataset contains information about various factors like the client’s demographic details, campaign contact history, economic indicators, and campaign outcomes.

### Features:
Job: Type of job (e.g., 'admin.', 'blue-collar', 'technician', etc.)
Marital: Marital status (e.g., 'single', 'married', 'divorced')
Education: Level of education (e.g., 'high.school', 'university.degree')
Default: Whether the client has credit in default ('yes' or 'no')
Housing: Whether the client has a housing loan ('yes' or 'no')
Loan: Whether the client has a personal loan ('yes' or 'no')
Contact: Type of communication used for contacting the client (e.g., 'cellular', 'telephone')
Month: Last contact month of the year (e.g., 'jan', 'feb')
Day of Week: Last contact day of the week (e.g., 'mon', 'tue')
Duration: Duration of the last contact in seconds
Campaign: Number of contacts during the campaign
Pdays: Number of days since the client was last contacted during a previous campaign
Previous: Number of contacts performed before this campaign
Poutcome: Outcome of the previous marketing campaign ('success', 'failure', 'nonexistent')
y: Whether the client subscribed to a term deposit ('yes' or 'no') — target variable

# 3. Data Preparation
### Data Cleaning:
Data was pretty clean in this dataset. 
### Feature Engineering:
Convert categorical features (e.g., 'job', 'marital', 'education') into numeric representations using techniques like One-Hot Encoding or Label Encoding.
Scale numerical features such as duration, campaign, pdays, etc., using techniques like Standard Scaling
### Splitting Data:
Split the data into training and testing sets using train_test_split. Ensure stratified splitting so that the distribution of the target variable (y) is maintained across both sets.

In this phase, we build different models to predict whether a client will subscribe to a term deposit.

# 4. Model Selection
### Compared the models : 
* Logistic Regression
* K Nearest Neighbors
* Decision Tree Classifier
* Support Vector Classifier (SVC)

### Model Training
Trained the model  on the training data and tuned hyperparameters using  Grid Search to find the best-performing model.

### Model Evaluation:
Evaluated models using accuracy score on test and train data

# 5. Evaluation
### Comparison of Models:
Best tuned values for models : 
* Logistic Regression - C=1, max_iter=1000
* K Nearest Neighbors - n_neighbors=7
* Decision Tree Classifier - max_depth=5
* Support Vector Classifier (SVC) - C=1

### Test accuracy:
* Logistic Regression - 0.916363
* K Nearest Neighbors - 0.899854
* Decision Tree Classifier - 0.918548
* Support Vector Classifier (SVC) - 0.913571
  
### Observation : 

Decision Tree Classifier was found to have the best performance, and also completes processing in moderate time. 

### Key Insights / Business recommendations : 
* Positive Influencers:
  Variables such as duration, cons.price.idx, euribor3m, contact_cellular, and poutcome_success have a positive relationship with the dependent variable, suggesting that these factors increase the likelihood of success.
* Negative Influencers: Features like emp.var.rate, month_may, pdays, contact_telephone, and default_yes have a negative relationship with the dependent variable, implying that these factors are associated with a lower likelihood of success.
* Employment variation rate increases, the probability of the positive outcome decreases
* Increase in the consumer price index leads to an Increase subscription
* The duration has a strong positive effect, meaning the longer the duration of contact, the more likely it is that the outcome will be positive
* The number of employees is positively correlated with the outcome.
* Months August,March increases the likelihood of positive outcome
* The month May is negatively correlated with the outcome.
* The number of days since the last contact (pdays) negatively influences the outcome
* The default_yes feature, indicating whether the client has credit in default, negatively impacts the outcome.
