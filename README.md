# Identifying Fraudulent Bank Accounts
As part of Know-Your-Customer checks or when a customer applies for a new line of credit

### The Challenge and Objective
More basic fraud detection methods work for many cases but not for all. The ones below can't detect fraud rings, fake IP addresses, hijacked devices, synthetic identities, stolen identities.
  * Endpoint - analyse users and their end-points (e.g. is it their PC or mobile phone?)
  * Navigation - analyse navigation behaviour & patterns (e.g. IP addresses, user ID normal behaviour)
  * Account - analyse the behaviour of a particular user and the channel they use

This mini-project involves looking at customers in a connected manner (instead of on a individual basis) to find patterns that could indicate a fraud ring
  * A group of people who mix and match a set of legitimate identification documents to create fake accounts. e.g. person A and B collaborate to create a new fake person C using person A's mobile and person B's social security number (could also be stolen IDs)
  * Difficult to use outlier analysis to catch these cases because when looking at fake person C on its own, they look perfectly normal as a customer. So when they build a seemingly legitimate credit score and request a huge loan in the future, the bank gives them the loan and they take the money and disappear.

TODO
 * Cross channel - analyse anomaly behaviour correlated across channels


### Reference Materials
* https://github.com/neo4j-contrib/gists/blob/master/other/BankFraudDetection.adoc
* https://www.youtube.com/watch?v=CR4z0mWbM-Y
  
### File descriptions
* BankFraudRings.ipynb - Jupyter notebook used to build and query the graph db
* data - folder containing CSVs with info about customers, their contact details, and financial product information


### Example Fraud Ring in Neo4j Browser
![alt text](https://github.com/mei-yong/BankFraudDetection/blob/master/images/fraudring.JPG)

### Potential fraud rings
![alt text](https://github.com/mei-yong/BankFraudDetection/blob/master/images/shared_info.JPG)

### Potential fraud rings - only accounts with financial risk (i.e. have a credit card or loan)
![alt text](https://github.com/mei-yong/BankFraudDetection/blob/master/images/financial_risk.JPG)
