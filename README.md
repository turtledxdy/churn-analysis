# Churn Analysis of a bank 

[Data source](https://docs.google.com/document/d/1aXmR4Uv8OIxVarXNxC8OoBJsc-iBP2LV/edit?usp=drive_link&ouid=115026402983328081349&rtpof=true&sd=true)

## ETL
-	Remove unused columns
-	Change data types
-	Merge 1:1 tables, mark CustomerInfo table to not load

## Data shaping
-	Link fact and dimension tables
-	Check everything is linked correctly
-	Set data category for GeographyLocation as Country/Region

## Analysis
**It was hypothesized before the analysis that the following factors would affect the exit rate…**
-	CreditScore (*customer with a higher credit score is less likely to leave the bank*)
-	Age (*older customers are less likely to leave their bank than younger ones*)
-	Tenure (*older clients are more loyal and less likely to leave a bank*)
-	Balance (*people with a higher balance in their accounts are less likely to leave the bank*)
-	HasCrCard (*people with a credit card are less likely to leave the bank*)
-	IsActiveMember (*active customers are less likely to leave the bank*)
-	EstimatedSalary (*people with lower salaries are more likely to leave the bank*)

**and would be interesting to see if the following factors affect the exit rate.**
-	Geography
-	Gender

## Findings
It was found that Tenure, HasCrCard and EstimatedSalary has little to no impact on churn rate. Customer with CreditScore lower than 400 has a 100% exist rate. This might be due to policies or legislation that terminates a customer’s relationship if they have poor credit score. Customer with extremely high balance tend to have high churn rate but this might be due to not a lot of people having extremely high balance. Overall, Balance and Churn rate do not seem to have any correlation. 

It is true that active members are less likely to leave the bank. However, it was found that middle age people are more likely to leave the bank. The relationship between Age and Churn Rate is more of a bell shape and not a linear inverse as expected.

The analysis also shows that Gender and Geography do affect churn rate. Women and people who are in Germany are more likely to leave the bank.

By making a Key Influencers chart, it was found that NumOfProducts - which was not thought to have an impact - in fact has the most impact on churn rate. Customers who have purchased more than 3 products through the bank are at least 80% more likely to leave the bank.

## Conclusion
NumOfProducts, Age, IsActiveMember, Gender, and Geography all impacts the churn rate. Any programs that seek to decrease churn rate would have to take these into consideration.
Would recommend gathering date for when customers exist to calculate monthly churn rate and to determine if customers left due to certain events. The company could also set up a customer exit survey to better understand the causes.
