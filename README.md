#  Loan Prosper Data Exploration 
                      
##              By    Purity Borois


## Dataset
This data  contains information on 113,937 loans with 81 variables on each loan. These variables include the loanstatus, borrower apr,loan original amount,interest rates,prosper ratings, prosper score,occupation,employment status,totaltrades,ontimeprosperpayments,debt to income ratio,investors among others.

On Data Wrangling, I decided to first inspect on my dataset randomly, that is by using (.sample),(.head),(.tail) and also by looking at the shape .I programmatically assessed my dataset using (.info) to get to know the datatype of each variable and the number of rows that have values corresponding to each variable.Performed descriptive statistics on numerical variables to identify the mean,median,quartiles,minimum and maximum amount.Converted prosperscore  and prosperrating(alpha) into ordered categorical variables.I dropped the columns which had a higher number of missing values.

## Summary of Findings
In the exploration phase, I performed univariate,bivariate and multivariate analysis on my chosen features and found various interesting relationships between them.My analysis focused on the best features to determine the ProsperRating (Alpha) of the loans.

- The distribution of ProsperRating (Alpha) appears to follow a normal distribution with most loans rated at C.Few loans are rated at AA which is the best rating.
- The DebtToIncomeRatio distribution appears to follow a right-skewed pattern, with most of the loans having a debt to income ratio less than 0.25.There is a sharp peak at 0.195, this means most loans have a debt to income ratio of 0.195.
- Most loans are borrowed by people who are employed then followed by those who are full-time. Few Retired people borrow loans maybe because they receive enough pensions to help in their needs,plus they have less responsibilities thus no need to borrow alot of money.
- Under occupation distribution,I saw that most loans were from borrowers who had other jobs then followed by professional jobs.Students in technical school,community college,college freshman borrow less to no loan,this may be caused by the fact they do not recieve an income or do not have a job to help in paying a loan.Judges also borrow less.This is because maybe they receive a handsome amount of money as their income, thus would not see a reason to loan if they can be able to meet their needs using their incomes. 
- The loan status distribution,tells us that most loans are completed, with a number still on current stage.A few loans are in their finalpaymentprogress and others are pastdue by more than 120 days.
- In our dataset, 88.84 borrowers listed that they are not in any group while 11.16 listed that they are currently in groups.
- StatedMonthlyIncome variable depicts an interesing distribution, because as the income increase from 0 to 2500 to 5000, the amount of loans also increases, but from 5000 onwards the loan amount starts to decrease. This shows that borrowers who receive higher incomes borrow less.
- For TotalTrades distribution, most loans were borrowed by people who had 20 and 30 trades.Trades never delinquent follows a left-skewed distribution with most of the trades having able to pay their debts on time. This is a good thing because it will increase your loan limit and also improve your rating.
- OpenRevolvingMonthlyPayments follow a right-skewed distributio,as most of the loans have a revolvingmonthlypayment of 0 to 300.For ontimeprosperpayments,as it increases from 0 to 10, the loan count also increases.But from 10 onwards the loan counts starts to decrease,though there is an exception at 35, where the loan count increased slightly.
- For ListingCategory (numeric), we see that most people borrow loans so as they can repay other debts.A few borrow for the purposes of boat,cosmetic procedure,green loans and RV.
- In the borrower state distribution, most loans are borrowed by people from CA-California.Followed by borrowers from Texas,Florida,New York,Illinois and Georgia.
- DebtToIncomeRatio vs StatedMonthlyIncome depicts a negative relationship because as the income increase the debt to income ratio decreases.Debt to income ratio has a positive relationship with totaltrades and ontimeprosperpayments.
- Debt to income ratio depicts a negative association with prosperrating (alpha),this means that as the debt to income ratio decreases,the ratings becomes better.
- There is a positive relationship between statedmonthlyincomes vs totaltrades and statedmonthlyincomes vs ontimeprosperpayments.
- For prosperrating (alpha) vs statedmonthlyincomes shows that as the incomes increase the prosperrating gets better. This shoes a positive relationship.For prosperrating (alpha) vs totaltrades,we see that as the total trades remain constant at 20,the ratings improve from HR to D,but then at rating C the number of trades starts to increase with increase in rating.
- From prosperrating vs loanstatus, i found that most loans that were rated were on current status.For prosperrating vs currentlyingroup,we see that most borrowers rated were not in any group.
- On multivariate analysis, I explored the effects of loan status on prosperrating and debttoincomeratio.I found out that,For completed and current loans, as the debttoincomeratio decreases, the ratings get better.This pattern is also seen when the loan is pastdue by 91-120 days.For past due(31-60) and (61-90) the debt to income ratio keeps on fluctuating as the ratings get better. Interestingly, for finalpaymentinprogress, as the debttoincomeratio increases the ratings increase from HR to E to D,as from rating  (C) the debttoincome ratio decreases with increase in ratings.For loans past due(>120days), there are no best ratings that is A and AA.
- I also investigated the effect of currentlyingroup on the relationship between prosperrating and statedmonthlyincomes.An increase in the statedmonthlyincomes for borrowers in groups and those not in groups leads to an increase in the rating.Borrowers not in groups received a higher income than those in group from rating HR to A.But at rating AA, borrowers in groups had a higher income than those not in groups.
- Lastly,  the distribution of debttoincomeratio vs logtransformedstatedmonthlyincome  at different levels of prosperrating (alpha), showed that when the most datapoints clustered at higherincome and lower debttoincomeratio, we get a better rating but as the most datapoints cluster at high debttoincomeratio , the ratings goes down.



## Key Insights For Presentation.
- The distribution of ProsperRating (Alpha) appears to follow a normal distribution with most loans rated at C.Few loans are rated at AA which is the best rating.
- The DebtToIncomeRatio distribution appears to follow a right-skewed pattern, with most of the loans having a debt to income ratio lees than 0.25.There is a sharp peak at 0.195, this means most loans have a debt to income ratio of 0.195.
- StatedMonthlyIncome distribution shows that as the income increase from 0 to 2500 to 5000, the amount of loans also increases, but from 5000 onwards the loan amount starts to decrease. This shows that borrowers who receive higher incomes borrow less.
- A negative relationship between prosperrating (alpha) and debt to income ratio.
- An increase in the statedmonthlyincome leads to a better rating. a positive relationship.
- Effects of loan status on the relationship between prosperrating (alpha) and debttoincome ratio.There are those statuses that follow the overall relationship, but a few are rated with fluctuating debttoincome ratio.
- The effect of currentlyingroup on prosperrating and statedmonthly, shows a positive relationship allthrough, but with a slight competition between incomes of those in groups and those not in groups.
- The increase in statedmonthlyincomes leads to a lower debt to income ratio thus giving the loan a better prosper rating.
 


```python
! jupyter nbconvert README.ipynb --to markdown
```


```python

```
