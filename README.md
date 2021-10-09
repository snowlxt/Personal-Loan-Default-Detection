# Personal-Loan-Default-Detection
![0_lAkevA6upQBq-NCk](https://user-images.githubusercontent.com/62194058/136675162-74e514ec-f6d2-4972-9110-74737937a999.jpeg)


## Overview
This project will explore the types of customers that default on loans in peer-to-peer lending. This is relevant because on such platforms, lenders are normally at a disadvantage due to information asymmetry: usually, borrowers are more knowledgeable about the risks of the platform than lenders. If borrowers default, lenders, as an individual, bear the consequence and the financial loss themselves, unlike financial institutions, which have procedures and operations in place to mitigate loss. When lenders screen applicants for loan bidding, it is important that they consider factors that affect default rate to make a meaningful and reliable investment. The purpose of this research is to determine the relationships between the default rate of a loan and several customer factors, such as credit score, employment, income, home ownership, and indebtedness. The study will also consider the loan purpose, loan grade and various other pertinent factors.

## Dataset
* Data source: LendingClub
* Time span: 2013 - 2017
* Shape: 74 columns, 887,379 rows
* Link: https://www.kaggle.com/husainsb/lendingclub-issued-loans

## Data Preprocessing
The dataset from Lending Club contained information pertaining to joint applicant borrowers. Since less than .001% of loans belonged to joint borrowers, the 4 columns of data describing these borrowers (including the joint dti, joint income, and the verification status of secondary applicant’s employment) contained mostly missing data and were thus removed. Next, we removed 14 columns that contained all missing data.  These included the number of revolving trades opened in the last 24 months, the number of personal financial inquiries, and the total current balance of all installment accounts. After columns of missing data were removed, we were left with 55 columns.  
Other data was simply removed due to their non-predictive power. Attributes like the webpage url of the loan listing, the title of the loan’s web listing, the description of the loan, zip code (where last two digits are censored), member id, loan id, and, lastly, policy code, as it contained the same value for all rows. After removing useless variables, we were left with 48 columns to work with.

Interestingly, the dataset contained a lot of leakage data that described either customer payment behavior after the loan was issued or data describing various actions of Lending Club itself. Since we want to predict loan default before the loan was issued, these variables should not be used in the prediction. For example, variables like the total late fees received to date, the total principal received to date, the total amount of interest received to date, the amount of the last payment, and the amount of recoveries were excluded from analysis as these describe customer payment behavior and would have impacted our prediction of customer solvency/default.  The variable describing the date of Lending Club’s last credit pull was also removed as it is again not an event in our desired timeframe. After all leaky data was removed, the final set of attributes for analysis was reduced to 30 variables, which is still a substantial amount of data to work with. The training data consisted of 107,391 rows, and the testing data consisted of 60,408 rows. Lastly, rows in which any variable had a value that was less than Q1-1.5*IQR or greater than  Q3+1.5*IQR was removed from the dataset.

## Mapping Raw Data to Features



## Feature Engioneering


## EDA


## Modeling
