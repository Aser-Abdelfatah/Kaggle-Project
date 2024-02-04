This is a group project for MATH154: Computatioanl Statistics in the fall of my sophomore year in 2022. The code and the full write-up are in the repo. This group project was solving the [Kaggle competition Give Me Some Credit
](https://www.kaggle.com/competitions/GiveMeSomeCredit).
## Introduction
In this write up we are analyzing the likelihood someone experiences financial distress over the next two years given certain parameters. With the data, there are a total of 11 parameters which include:
1. SeriousDlqin2yrs: Person experienced 90 days past due delinquency or worse after 2 years
2. RevolvingUtilizationOfUnsecuredLines: Total balance on credit cards and personal lines of credit except real estate and no installment debt like car loans divided by the sum of credit limits
3. Age: Age of borrower in years
4. NumberOfTime30-59DaysPastDueNotWorse: Number of times borrower has been 30-59 days past due but no worse in the last 2 years.
5. DebtRatio: Monthly debt payments, alimony,living costs divided by monthly gross income
6. MonthlyIncome: Monthly income
7. NumberOfOpenCreditLinesAndLoans: Number of Open loans (installment like car loan or mortgage) and Lines of credit (e.g. credit cards)
8. NumberOfTimes90DaysLate: Number of times borrower has been 90 days or more past due.
9. NumberRealEstateLoansOrLines: Number of mortgage and real estate loans including home equity lines of credit
10. NumberOfTime60-89DaysPastDueNotWorse: Number of times borrower has been 60-89 days past due but no worse in the last 2 years.
11. NumberOfDependents: Number of dependents in family excluding themselves (spouse, children etc.)

<br> Using these different parameters, our goal is to create the best learner we can using the evaluation metric of area under the curve (AUC) of the receiver operating characteristic (ROC) curve.
A couple of early issues arise even from a quick look of the data set. We see that there are missing/NA values in the MonthlyIncome and number of NumberOfDependents columns. We also want to make sure that we remove any outliers that might heavily screw the data. What we decide to do is use Outlier Analysis to determine which values to remove from our data set and the imputation method SMOTE to fill in our missing values.
