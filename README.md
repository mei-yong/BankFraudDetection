# Identifying Fraudulent Bank Accounts
* As part of Know-Your-Customer checks or when a customer applies for a new line of credit
* More basic fraud detection methods include:
   * Endpoint - analyse users and their end-points (e.g. is it their PC or mobile phone?)
   * Navigation - analyse navigation behaviour & patterns (e.g. IP addresses, user ID normal behaviour)
   * Account - analyse the behaviour of a particular user and the channel they use
   * But they can't detect fraud rings, fake IP addresses, hijacked devices, synthetic identities, stolen identities
* This mini-project involves using fraud ring detection logic
    * A group of people who mix and match a set of legitimate identification documents to create fake accounts. e.g. person A and B collaborate to create a new fake person C using person A's mobile and person B's social security number (could also be stolen IDs)
    * Difficult to use outlier analysis to catch these cases because when looking at fake person C on its own, they look perfectly normal as a customer. So when they build a seemingly legitimate credit score and request a huge loan in the future, the bank gives them the loan and they take the money and disappear.
    

### Reference Materials
* https://github.com/neo4j-contrib/gists/blob/master/other/BankFraudDetection.adoc
* https://www.youtube.com/watch?v=CR4z0mWbM-Y
  
### File descriptions
* BankFraudRings.ipynb - Jupyter notebook used to build and query the graph db


### Example Fraud Ring in Neo4j Browser
![alt text](https://github.com/mei-yong/BankFraudDetection/blob/master/images/fraudring.JPG)

### Potential fraud rings
![alt text](https://github.com/mei-yong/BankFraudDetection/blob/master/images/shared_info.JPG)

### Potential fraud rings - only accounts with financial risk (i.e. have a credit card or loan)
![alt text](https://github.com/mei-yong/BankFraudDetection/blob/master/images/financial_risk.JPG)
