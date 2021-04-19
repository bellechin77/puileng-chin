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
|Test Charter|Target|Resource|Information|Priority|Comment|Duration|Quality Attribute|
:----------|:-----|:-------|:---------|:-------|:-----|:-------|:---------------
|1|Language settings|1 tester|To evaluate if language is correctly set based on user selection|High|Basic feature|15 mins|Reliability|
|2|Currency settings|1 tester|To evaluate if main currency is set based on user selection and correctly applied to all accounts and transactions (expense and income)|High|Basic feature|15 mins|Reliability|
|3|Balance settings|1 tester|To evaluate if settings (budget mode, carry over, future recurring records) are correctly applied based on user selection.|High|Basic feature|10 mins|Reliability|
|4|Account|1 tester|To evaluate if account i.e cash, payment card, paypal etc can be added, updated and removed|High|Basic feature|15 mins|Accuracy|
|5|Income|2 testers|To evaluate if income can be added, updated and removed|High|Basic feature|30 mins|Accuracy|
|6|Expense|2 testers|To evaluate if expense can be added, updated and removed|High|Basic and key feature|30 mins|Accuracy|
|7|Transaction list|1 tester|To evaluate if the Transaction list accurately show all income and expense transactions|High|Basic and key feature|30 mins|Accuracy|
|8|Chart|2 testers|To evaluate if Spending distribution is accurately displayed on the chart based on the expense transactions|High|Basic and key feature|30 mins|Accuracy|
|9|Balance|2 testers|To evaluate if the Balance accurately shows the correct value taking into account: <ol><li>all income and expense transactions,</li><li>account settings, and </li><li>balance settings</li></ol>|High|Basic and key feature|60 mins|Accuracy|
|10|Exception handling|2 testers|To evaluate if the app is capable of handling exceptions for invalid user input and/or user navigations|High|Basic feature|90 mins|Reliability|
|11|Categories from default|1 tester|To evaluate if categories from defaults can be updated and removed, and no information from exisiting transactions is lost and corrupted|High|Basic feature|15 mins|Accuracy|
|12|New categories|1 tester|To evaluate if new categories for income and expense can be added, updated and removed|Low|Pro feature|30 mins|Usability
|13|Recurring records|1 tester|To evaluate if recurring transaction can be created at regular intervals and reminders are set ahead of time |Medium|Pro feature|30 mins|Reliability, Maintainability|
|14|Multi-currency function|1 tester|To evaluate if accounts with different currencies can be added, updated and removed, and if account balance is accurately included in the chart and transaction list|Medium|Pro feature|30 mins|Accuracy, Usability|
|15|Synchronization|2 testers|To evaluate if the data can be safely synchronized using Google Drive or Dropbox account|Medium|Pro feature|30 mins|Usability, Performance|
|16|Password protection|2 testers|To evaluate if access to the app and records can be password protected|High|Pro feature|30 mins|Security|
|17|Built-in calculator|1 tester|To evaluate if the built-in calculator is functional|High|Basic feature|15 mins|Reliability|
|18|Dark theme|1 tester|To evaluate if dark theme is correctly applied when selected|Low|Pro feature|10 mins|Usability|

### Findings / Potential Defects
|Test Charter|Target|Findings|Type of Risks|Risk Mitigation|
|:----------|:-----|:-------|:------------|:--------------|
|1|Language settings|Language is partially updated in the app if user does not exit and restart the app. This may cause some confusion and may impact the usuablity if users experience difficulty in navigating the functions due to problem in interpretatng the language in sections that have not been updated before the app is restarted|Usability|Force restart of app after language is changed in settings|
|2|Currency settings|Currency is sorted by currency description instead of currency code. Most popular currencies i..e USD, GBP, EUR are not displayed on top for easy navigation|Usability|Enhance the presentation of currency list to faciliate quick search i.e. most populate currencies are listed on top of the list, followed by other currencies sorted by currency code|
|3|Balance settings|There is no Info or Help to briefly describe the purpose of the individual settings (Budget mode, Carry over, Future recurring records). The red message pops up from time to time (triggered with some hidden rule) but not self-intuitive and viewable as and when user wants|Usability|Enhance GUI with quick info or help when users tap on a specific function/feature|
|4|Account|<ol><li>"Add" label in the Accounts menu appears confusing. Tapping on "Add" is not functional. New account can be added only by tapping "+".</li><li>Account with same name, currency and icon can be added (duplicate accounts can appear confusing when managing transactions)</li><li>Only the initial account balance of the cash account from default is included in the Balance, Transaction list and Chart. The initial account balance for all other accounts (payment card from default and all other new accounts added)are not included even though the switcher "Included in the balance" is turned on</li></ol>|Usability (1, 2), Reliability (3)|<ol><li>Make the "Add" label functional as the "+" symbol or remove the "Add" label from the menu</li><li>Add quick user guide on unique account creation i.e. by name and currency, icon and currency, etc. Impose validation on duplicate accounts</li><li>Review the criteria to include the account balance in the Balance, Chart and Transaction list, and rectify the solutions where appropriate</li></ol>|
|5|Income|<ol><li>Income added to accounts (other than cash account from defaults) is not updated to the Balance, Transaction list and Chart even though the switcher "Included in the balance" is turned on</li><li>When an income record is edited, there is no option to cancel Edit. User could have made some mistakes in the edit and wants to undo changes, but option to cancel changes is not available. User only has the option to undo changes after the changes are saved (Done)</li></ol>|Reliability (1), Usability (2)|<ol><li>Review the criteria to include the Income transaction in the Balance, Chart and Transaction list, and rectify the solutions where appropriate.</li><li>Add a cancel option for Edit.</li></ol>|
|6|Expense|<ol><li> Expense added to accounts (other than cash account from defaults) is not updated to the Balance, Transaction list and Chart even though the switcher "Included in the balance" is turned on</li><li>When an expense record is edited, there is no option to cancel Edit. User could have made some mistakes in the edit and wants to undo changes, but option to cancel changes is not available. User only has the option to undo changes after the changes are saved (Done).</li></ol>|Reliability (1), Usability (2)|<ol><li>Review the criteria to include the Expense transaction in the Balance, Chart and Transaction list, and rectify the solutions where appropriate.</li><li>Add a cancel option for Edit.</li></ol>|
|7|Transaction list|Only account balance and transactions of the cash account from defaults are reflected in the Transaction list. Account balances and transactions of all other accounts are not reflected in the Transaction list|Reliability|Review the criteria to include the account balance, income and expense transactions in the Transaction list, and rectify the solutions where appropriate|
|8|Chart|<ol><li>Only expense transactions of the cash account from defaults are reflected in the Chart. Expense transactions of all other accounts are not reflected in the Chart.</li><li>Total spending distribution exceeeds 100%</li></ol>|Reliability (1, 2)|<ol><li>Review the criteria to include the expense transactions in the Chart, and rectify the solutions where appropriate.</li><li>Rectify the rounding precision of the spending distribution</li></ol>|
|9|Balance|<ol><li>Only account balance and transactions of the cash account from defaults are reflected in the Balance. Account balances and transactions of all other accounts are not reflected in the Balance.</li><li>Monthly budget amount is not reflected in the Chart when Budget mode is turned on. The features on Budget mode cannot be fully tested (feature is not usable from end user's perspective)</li></ol>|Reliability (1), Usability (2)|<ol><li>Review the criteria to include the account balance, income and expense transactions in the Balance, and rectify the solutions where appropriate.</li><li>Quick user guide as to how budget mode can be used i.e. monthly budget amount vs income and carry over, and review solutions for variations of balance settings</li></ol>|
|10|Exception handling|Negative test not explored|||
|11|Categories from default|Category from defaults can be deleted resulting in all associated transaction records removed/lost even though user is warned in the Deletion confirmation dialog|Accuracy|Category that has been in use in any transactions should not be deleted| 
|12|New categories|Pro feature not explored|||
|13|Recurring records|Pro feature not explored|||
|14|Multi-currency function|Pro feature not explored|||
|15|Synchronization|Pro feature not explored|||
|16|Password protection|Pro feature not explored|||
|17|Built-in calculator|Calculator does not return correct result for certain formula i.e. 9999999999.99*2, which returned a value 0|Reliability|Review the capacility of the fields used in calculation, and identify root cause of the calculation error|
|18|Dark theme|Pro feature not explored|||


### Test Approach
1. The Exploratory test starts with Basic features of the app following the priority assigned to each charter.
   - Settings (Language, Currency, Balance)
   - Accounts
   - Expenses
   - Income
   - Transaction list
   - Spending distribution chart
   - Balance
2. When testing the Basic features, black-box testing is used following the logical flow of a typical end user.
3. Exhaustive negative testing is subsequently done with variations of invalid data input and user navigations to discover if the app is capable of handling exceptions.
4. Test scenarios used in the black-box testing are documented and the test observations/results are logged. 
5. Test scenarios and test data used in the negative tetsting are also documented, and system behaviors are logged.
6. The information gathered from the Exploratory tests on Basic features will be used for the test design in subsequent tests.
7. Exploratory tests on Pro features are carried out after the Basic features are tested satisfactorily.
   - Password protection
   - Synchronization
   - Recurring records
   - Multi-currency
   - New categories
   - Dark theme
