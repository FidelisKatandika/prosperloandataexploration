# Features that Affect Borrower's Annual Percentage Rate
## by (Fidelis Katandika)


## Dataset
The data consists 113,937 loans from prosper with 81 variables on each loan. 
The dataset can be found [here](https://www.google.com/url?q=https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv&sa=D&ust=1581581520570000)
with feature documentation available [here](https://www.google.com/url?q=https://docs.google.com/spreadsheet/ccc?key%3D0AllIqIyvWZdadDd5NTlqZ1pBMHlsUjdrOTZHaVBuSlE%26usp%3Dsharing&sa=D&ust=1554486256024000)


## Summary of Findings

This exploration focused on the borrowers in the dataset that had loans with prosper in the dataset, which came to around 19000+ records. The exploration focused on identifying what features affected Borrower's Annual Percentage Rate.  The results of the exploration have shown a strong correlation between Borrower Annual Percentage Rate, Prosper Rating and Credit Score. Additionally, the loan term revealed loans with a length of 12 months are cheaper, followed by 60 month-long loans. 12 month loans overrode the credit score rating. 36 month loans were on average more costly than the other 2 categories but has cheaper and more costly extremes over the Credit Score range. The Credit Score/Prosper Rating influences the BAPR for loans with length larger than 12 months, however, the loans with the longest term have better Borrower Average with significant influence from the credit score.

The investigation started with univariate exploration. All the features were visualized to gain an understanding of the distribution and identified unusual data points and outliers. The main variable of interest was BorrowerAPR, which is the Borrower's Annual Percentage Rate (BAPR) , the percentage of the annual cost of borrowing to the borrower. The graph of BAPR was unimodal and highlighted that there are few results that are above 40%. The data above 40% all had a poor Prosper Rating and a below-average Credit Score Range Upper and Lower score. Similarly, the rest of the features were explored. The Current Credit Lines (CurrentCreditLines) required a log-transformed histogram for the readability of the graph. The Credit Score Lower & Upper were averaged to create a new feature CreditScoreAvg. Occupation required transformation to eliminate job subgroups. The majority of the plots produced were unimodal. This factored in the reason for picking variables for focus in the bivariate plots.

Bivariate plots strongly indicated the Credit Score Average (CreditScoreAvg) and Prosper Rating (ProsperRating - Prosper's internal rating) were negatively correlated. Using Box & Violin plots made this relationship, after an initial scatter plot of CreditScore against BAPR. Bank Card Utilization (BankCardUtilization) heat map showed a high card utilization matched with a high BAPR but this was not very strong. Interestingly,  the tenure of a loan given by the attribute term in months 12, 36, and 60 reflected on average the shortest loan duration had the lowest BAPR. Followed by 60-month-long loans. The loan tenure, Credit Score and BAPR formed the investigation for the multivariate exploration phase.

The multivariate exploration strengthened the fact that loans of 12-month tenure are the least expensive but in addition to this these loans were not affected by a poor credit score. On average the multivariate plot showed that 36-month tenure had the highest BAPR. On average the 60 months have more favorable rates as compared to loans that are 36 months long.


## Key Insights for Presentation
The presentation focuses on providing insights on the distribution of Borrower's Annual Percentage Rate, which is a unimodal graph. Followed by the distribution of Credit Score, which shows the vast majority of borrowers lie in a particular range 680 to 730, with the extreme ends having fewer numbers. 

The Prosper Rating affects the BAPR in the same way as Credit Score does, therefore there is a box plot showing how these two variables behave. 

The term of the loans has an interesting behaviour against BAPR, a Box Plot of durations by BAPR was added to show loans with a duration of 36 months have the highest average BAPR, followed by the 60 month-long loan. The 12 month loan has the lower average BAPR. 

This is followed by a scatter plot of CreditScoreAvg and BorrowerAPR, there is negative correlation between the attributes. The better score the more likely the BAPR will be lower.

Finally, we have the final plot that shows the Credit Score/Prosper Rating does influence the BAPR for loans with length larger than 12 months, however, the loans with the longest term have better Borrower Average with significant influence from the credit score.
