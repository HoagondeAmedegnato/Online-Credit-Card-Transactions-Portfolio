# Online-Credit-Card-Transactions-Portfolio
***Over 90k credit card transactions marked as Fraudulent or Legitimate***



____

**Note**: This readme will guide you through the steps I took to complete this project
____
**Table of Contents**
____
I.	***Introduction***

II.	***Data Collection and Data Preprocessing***

III.	***Exploratory Data Analysis***: 00.EDA.ipynb

IV.	***Model Development***: 01.Model Development.ipynb

V.	***Findings and Takeaways***
____
I.	***Introduction***

Credit card fraud is an inclusive term for fraud committed using a payment card, such as a credit card or debit card. The purpose may be to obtain goods or services, or to make payment to another account which is controlled by a criminal. Credit card fraud happens when someone, a fraudster or a thief uses a stolen credit card or the information from that card to make unauthorized purchases in another name or take out cash advances using that account.

It is important for me to analyze and visualize the Online Credit Card Transactions datasets, because in most companies, fraud is identified only after it occurs. In the event that they are unable to prevent it in a timely fashion, however, fraud detection is the best bet for eradicating it from the environment and preventing a recurrence.

Again, my goal for this project is to *help prevent, reduce or avoid the credit card fraud*.
____
II.	***Data Collection and Data Preprocessing***

The datasets I use, is from Kaggle website (Data Source: https://www.kaggle.com/adityakadiwal/credit-card-fraudulent-transactions), where the file CC_FRAUD.csv has been provided with a detail of 94682 transactions: 2094 that are marked as fraudulent and 92588 are marked as legitimate transactions. The description of the 20 columns of the dataset is as follow:

* *DOMAIN*: The domain name of the customer's email address that was used for the transaction (Masked)

* *STATE*: The state code of the customer's location.

* *ZIPCODE*: The zip code of the customer's location.

* *TIME1*: Hour feature #1 of the transaction.

* *TIME2*: Hour feature #2 of the transaction.

* *VIS1*: Anonymized feature #1 for feature VIS.

* *VIS2*: Anonymized feature #2 for feature VIS.

* *XRN1*: Anonymized feature #1 for feature XRN.

* *XRN2*: Anonymized feature #2 for feature XRN.

* *XRN3*: Anonymized feature #3 for feature XRN.

* *XRN4*: Anonymized feature #4 for feature XRN.

* *XRN5*: Anonymized feature #5 for feature XRN.

* *VAR1*: Anonymized feature #1 for feature VAR.

* *VAR2*: Anonymized feature #2 for feature VAR.

* *VAR3*: Anonymized feature #3 for feature VAR.

* *VAR4*: Anonymized feature #4 for feature VAR.

* *VAR5*: Anonymized feature #5 for feature VAR.

* *TRN_AMT*: The transaction amount.

* *TOTAL_TRN_AMT*: The total transaction amount.

* *TRN_TYPE*: The type of transaction whether FRAUD or LEGIT.

I’ve downloaded the CC_FRAUD.csv file from the Kaggle website and save them into my Google Drive, created a Google Colaboratory for the notebooks.

I’ve created two (2) Google Colaboratory, because my project is subdivided into two (2) parts:

* Exploratory Data Analysis (EDA), where I’ve explored the analysis for the overall dataset
* Model Development, where I’ve performed the market segmentation using supervised and unsupervised machine learning techniques.
____
III.	***Exploratory Data Analysis***: 00.EDA.ipynb

As part of this, several plots have been made:
* Analyzed the whole dataset by examining them
* ![image](https://user-images.githubusercontent.com/79173300/137671879-53e18141-327a-47ff-9b82-c16a75b77abf.png)

* Divided the dataset into two parts to count the parts that are marked fraudulent (2052), and the parts that are marked legitimate (87562)
* ![image](https://user-images.githubusercontent.com/79173300/137672419-235044d3-84d7-4607-984e-19026feb332c.png)

* Analyzed the 2052 Fraud Credit Cards 
* ![image](https://user-images.githubusercontent.com/79173300/137672621-d70a573d-7f65-456a-b9ac-c21a77e664e9.png)
* ![image](https://user-images.githubusercontent.com/79173300/137672698-54cc88c4-c0ba-4d55-a339-243bd0c1721c.png)


* Analyzed the 87562 Legit Credit Cards
* ![image](https://user-images.githubusercontent.com/79173300/137672880-172e3ec8-c0f4-4a1b-9782-6aa067f6b49b.png)
* ![image](https://user-images.githubusercontent.com/79173300/137672915-ba4b8c52-1506-4f44-9aab-615ce2f25927.png)

* Calculated the Correlation Matrix of the Credit Card dataset
* ![image](https://user-images.githubusercontent.com/79173300/137673056-dbc50a7d-fa77-4170-8fd3-a3f9ebd18177.png)

____
IV.	***Model Development***: 01.Model Development.ipynb

In order to develop this credit card fraud detection, I’ve used the unsupervised machine learning technique to improve the process efficiency. Machine learning models are able to learn from patterns of normal behavior. They are very fast to adapt to changes in that normal behavior and can quickly identify patterns of fraud transactions. This means that the model can identify suspicious customers even when there hasn't been a chargeback yet.

As part of this, I’ve implemented the following steps:
