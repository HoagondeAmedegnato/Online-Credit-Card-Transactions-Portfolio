# Online-Credit-Card-Transactions-Portfolio
***Over 90k credit card transactions marked as Fraudulent or Legitimate***

![image](https://user-images.githubusercontent.com/79173300/133983157-99cfbb3a-346f-4aab-9d7f-1cd539b5420d.png)

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
 ![image](https://user-images.githubusercontent.com/79173300/137671879-53e18141-327a-47ff-9b82-c16a75b77abf.png)

* Divided the dataset into two parts to count the parts that are marked fraudulent (2052), and the parts that are marked legitimate (87562)
 ![image](https://user-images.githubusercontent.com/79173300/137672419-235044d3-84d7-4607-984e-19026feb332c.png)

* Analyzed the 2052 Fraud Credit Cards 
 ![image](https://user-images.githubusercontent.com/79173300/137672621-d70a573d-7f65-456a-b9ac-c21a77e664e9.png)
 ![image](https://user-images.githubusercontent.com/79173300/137672698-54cc88c4-c0ba-4d55-a339-243bd0c1721c.png)


* Analyzed the 87562 Legit Credit Cards
 ![image](https://user-images.githubusercontent.com/79173300/137672880-172e3ec8-c0f4-4a1b-9782-6aa067f6b49b.png)
 ![image](https://user-images.githubusercontent.com/79173300/137672915-ba4b8c52-1506-4f44-9aab-615ce2f25927.png)

* Calculated the Correlation Matrix of the Credit Card dataset
 ![image](https://user-images.githubusercontent.com/79173300/137673056-dbc50a7d-fa77-4170-8fd3-a3f9ebd18177.png)

____
IV.	***Model Development***: 01.Model Development.ipynb

In order to develop this credit card fraud detection, I’ve used the unsupervised machine learning technique to improve the process efficiency. Machine learning models are able to learn from patterns of normal behavior. They are very fast to adapt to changes in that normal behavior and can quickly identify patterns of fraud transactions. This means that the model can identify suspicious customers even when there hasn't been a chargeback yet.

In order to train and evaluate the model:
* I’ve calculated the Accuracy Score and the Confusion Matrix of these Supervised Machine Learning:
			
 ![image](https://user-images.githubusercontent.com/79173300/137682138-0275ae76-01fa-4e0b-be9e-5b0921e2187f.png)

* I’ve created a dataframe with 2 Principal Component Analysis (PCA), and concatenated it to the cluster 

pca | pca | cluster
---- | ---- | ----
0.095292 | 0.390802 | 4
---- | ---- | ---- |
1.543063 | -1.024833 | 6
---- | ---- | ---- |
1.219094 | 3.171305 | 7
---- | ---- | ---- |
-0.946215 | -2.743648 | 0
---- | ---- | ---- | 
-1.258884 | 1.046530 | 7

 ![image](https://user-images.githubusercontent.com/79173300/137684721-bfcfc847-daac-436c-af96-9a5cc43c2ac6.png)

* I’ve been used the following steps for K-Means algorithm:

  - Choose number of clusters “K”

  - Select random K points that are going to be the centroids for each cluster

  - Assign each data point to the nearest centroid, doing so will enable me to create “K” number of clusters

  - Calculate a new centroid for each cluster 

  - Reassign each data point to the new closest centroid

  - Go to step 4 and repeat

  ![image](https://user-images.githubusercontent.com/79173300/137687477-6f5e7ef7-805d-4466-a2f2-f126bfb54691.png)

  ![image](https://user-images.githubusercontent.com/79173300/137687628-1ce1f2ed-fce2-4577-91d8-9b83da9ad7e6.png)

  ![image](https://user-images.githubusercontent.com/79173300/137687791-b51f43d6-0223-41be-8858-08de9eae54e4.png)

  ![image](https://user-images.githubusercontent.com/79173300/137687854-8b7250f1-dbe1-44cc-bb19-09baf669ec1c.png)

  ![image](https://user-images.githubusercontent.com/79173300/137687915-809bf039-3639-4438-a6a7-88284ff959a1.png)

  ![image](https://user-images.githubusercontent.com/79173300/137687975-0fea8057-3ec9-4ec6-b5f6-149f7c407c9b.png)

  ![image](https://user-images.githubusercontent.com/79173300/137688016-06e902e7-7385-42c5-9be3-a20bf23f7989.png)

  ![image](https://user-images.githubusercontent.com/79173300/137688084-3b31aa66-939c-41b9-8401-62dea18691e7.png)

  ![image](https://user-images.githubusercontent.com/79173300/137688140-dc709ea3-bf31-4442-8002-b75ee2a67b6d.png)

  ![image](https://user-images.githubusercontent.com/79173300/137688182-01a3bc88-ca4b-422e-8f2c-4c89de950338.png)

  ![image](https://user-images.githubusercontent.com/79173300/137688223-0016e388-efba-44ac-831b-b6048534fe4d.png)

  ![image](https://user-images.githubusercontent.com/79173300/137688269-bfc7c5e7-3a6b-4978-a018-d8bc74250598.png)

  ![image](https://user-images.githubusercontent.com/79173300/137688309-3c282ee9-a514-4e08-bd32-021f25a29bf5.png)

  ![image](https://user-images.githubusercontent.com/79173300/137688343-3a5c57e4-7035-4ced-849e-5b0a97f00d4e.png)

  ![image](https://user-images.githubusercontent.com/79173300/137688399-11bdeac3-3067-47a8-8145-d336f21a9d25.png)

  ![image](https://user-images.githubusercontent.com/79173300/137688441-a3f78d31-d503-4cda-a04e-e1c7e2e3b95a.png)

  ![image](https://user-images.githubusercontent.com/79173300/137688501-774286d8-b9dd-4d57-814c-7feea01d5ed3.png)

* I’ve trained the autoencoder to fit it to the dataset credit card, and applied the training to predict new features.

pca | pca | cluster
---- | ---- | ----
2.306092 | -1.540109 | 2
---- | ---- | ---- |
-0.711844 | 0.985546 | 3
---- | ---- | ---- |
3.832627 | -0.653523 | 2
---- | ---- | ---- |
-1.854407 | 0.168122 | 3
---- | ---- | ---- | 
-0.514209 | 0.474712 | 3

![image](https://user-images.githubusercontent.com/79173300/137686367-78e83741-df0d-4765-9363-1c7f98cc034c.png)


____
V.	***Findings and Takeaways***
