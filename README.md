# N26 Home Challenge
## Task 1 - Exploratory Test Charters
### Device Information
Model| iOS
-----|---
iPhone X|14.4.2

### Application
App|Version
---|-------
Monefy for iOS|1.3.18

### Test Charters
Test Charter|Target|Resource|Information|Priority|Comment|Duration|Quality Attribute
-----------|------|--------|----------|--------|------|--------|----------------
1|Language settings|1 tester|To evaluate if language is correctly set based on user selection|High|Basic feature|15 mins|Reliability
2|Currency settings|1 tester|To evaluate if main currency is set based on user selection and correctly applied to all accounts and transactions (expense and income)|High|Basic feature|15 mins|Reliability
3|Balance settings|1 tester|To evaluate if settings (budget mode, carry over, future recurring records) are correctly applied based on user selection.|High|Basic feature|10 mins|Reliability
4|Account|1 tester|To evaluate if account i.e cash, payment card, paypal etc can be added, updated and removed|High|Basic feature|15 mins|Accuracy
5|Income|2 testers|To evaluate if income can be added, updated and removed|High|Basic feature|30 mins|Accuracy
6|Expense|2 testers|To evaluate if expense can be added, updated and removed|High|Basic and key feature|30 mins|Accuracy
7|Transaction list|2 testers|To evaluate if the Transaction list accurately show all income and expense transactions|High|Basic and key feature|30 mins|Accuracy
8|Chart|2 testers|To evaluate if Spending distribution is accurately displayed on the chart based on the expense transactions|High|Basic and key feature|30 mins|Accuracy
9|Balance|2 testers|To evaluate if the Balance accurately shows the correct value taking into account: (1) all income and expense transactions, (2)account settings (Include or Not include in Balance), and (3) balance settings (budget mode, carry over)|High|Basic and key feature|60 mins|Accuracy
10|Exception handling|2 testers|To evaluate if the app is capable of handling exceptions for invalid user input and/or user navigations|High|Basic feature|90 mins|Reliability
11|Categories from default|1 tester|To evaluate if categories from defaults can be updated and removed, and no information from exisiting transactions is lost and corrupted|High|Basic feature|15 mins|Accuracy
12|New categories|1 tester|To evaluate if new categories for income and expense can be added, updated and removed|Low|Pro feature|30 mins|Usability
13|Recurring records|1 tester|To evaluate if recurring transaction can be created at regular intervals and reminders are set ahead of time |Medium|Pro feature|30 mins|Reliability, Maintainability
14|Multi-currency function|1 tester|To evaluate if accounts with different currencies can be added, updated and removed, and if account balance is accurately included in the chart and transaction list|Medium|Pro feature|30 mins|Accuracy, Usability
15|Synchronization|2 testers|To evaluate if the data can be safely synchronized using Google Drive or Dropbox account|Medium|Pro feature|30 mins|Usability, Performance
16|Password protection|2 testers|To evaluate if access to the app and records can be password protected|High|Pro feature|30 mins|Security
17|Built-in calculator|1 tester|To evaluate if the built-in calculator is functional|High|Basic feature|15 mins|Reliability
18|Dark theme|1 tester|To evaluate if dark theme is correctly applied when selected|Low|Pro feature|15 mins|Usability
