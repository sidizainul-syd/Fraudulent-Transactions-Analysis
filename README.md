# Fraudulent-Transactions-Analysis
This dataset obtained from kaggle "https://www.kaggle.com/dataset/58ea43a05b203eca4de1d23aaed6c819a7625691eaaa033775e31783d70847b6" . 

Ran few analysis and try to create model that able to classify transactions as fraud. The dataset is severly imbalance hence the correlation was very low. But did few analysis to understand the behaviour of the fraud transactions. 

Analysis Finding Summary

- Fraud is bold enough to make fraudulent transactions to account that are already flagged, but comparing to other fraudulent transactions the amount of transactions smaller. Indicating the person have self awareness about his account could be flagged.
- Receipients of fraud account did move around the money in large sum of money to non flagged account comparing to flagged account. 
- Fraudulent transactions focus more on customer type of receipents as shown in dataset only customer type labelled as fraudulent transactions. Avoiding merchant probably because merchant account could be auditted.
- Highest correlated variables is Transaction to Fraud Account (Mainly we mark those transactions) and lowest would be Fraud Account Making Transaction. Indicating the fraudster clever enough to hide their transactions mainly due to creat fraudulent transactions to non flagged account.


Suggestion

- Dataset severely imbalance but it does replicate the real world as fraudulent transaction is harder to detect. Probably can launch investigation towards recepients of transactions that receive transactions from Fraudelent flagged account.
- Step described in data description as a real life time in hour, but not mentioning whether it is 00:00 AM or 12:00 PM. It is good to learn when the fraudulent transactions happen. It is better to provide the day of each transactions so we can learn more whether transactions were made on weekend or weekdays. 
- Create associations of each account, to learn their relationship to each other. 

Model Development

- Currently running on auto ml of PyCaret. Early assesment, shows that it overfitting using default parameter of sklearn logistic regression. High accuracy but bad in other important metrics. Important metrics to be evaluate here is Recall in order to access how well the actual fraudlent transaction that our model predicted as fraud. Early assesment shows it doing so well in predicting non fraud but compares to Fraud very bad.

