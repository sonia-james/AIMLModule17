# 1.Business Understanding
Objective: The goal of this project is to predict whether a customer will subscribe to a term deposit based on various features, such as the client's personal information, contact details, and campaign characteristics. The data is related to phone calls made during a direct marketing campaign by a Portuguese banking institution.

### Business Problem:

The bank wants to increase the efficiency of its marketing campaigns. By predicting whether a client will subscribe to a term deposit based on past interactions and client information, the bank can focus resources on high-potential leads, improving conversion rates and minimizing marketing costs.
Goal: Build a predictive model that can classify whether a customer will subscribe to a term deposit (the target variable y). The model should aim to accurately predict this binary outcome.

# 2.Data Understanding
Data Collection: The dataset contains information about various factors like the client’s demographic details, campaign contact history, economic indicators, and campaign outcomes.

Features:

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
