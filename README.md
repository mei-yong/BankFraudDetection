# Identifying Fraudulent Bank Accounts
* As part of Know-Your-Customer checks or when a customer applies for a new line of credit
* Based on fraud ring detection logic
    * A group of people who mix and match a set of legitimate identification documents to create fake accounts. e.g. person A and B collaborate to create a new fake person C using person A's mobile and person B's social security number (could also be stolen IDs)
    * Difficult to use outlier analysis to catch these cases because when looking at fake person C on its own, they look perfectly normal as a customer. So when they build a seemingly legitimate credit score and request a huge loan in the future, the bank gives them the loan and they take the money and disappear.

* Used the below tutorial as a foundation
    * https://github.com/neo4j-contrib/gists/blob/master/other/BankFraudDetection.adoc
    
* BankFraudRings.ipynb - Jupyter notebook used to build and query the graph db


### Example Fraud Ring in Neo4j Browser
![alt text](https://github.com/mei-yong/BankFraudDetection/blob/master/images/fraudring.JPG)

### Potential fraud ring
![alt text](https://github.com/mei-yong/BankFraudDetection/blob/master/images/shared_info.JPG)

### Potential fraud ring - only accounts with financial risk (i.e. have a credit card or loan)
![alt text](https://github.com/mei-yong/BankFraudDetection/blob/master/images/financial_risk.JPG)
