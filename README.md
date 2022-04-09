# Unit 5-Assignment

## Introduction
In Part 1 of this assignment, we create a "Personal Financial Planner" that allows users to determine if they have enough savings in their Emergency Fund, by comparing their portfolio (comprised of shares and cryptocurrency) to a set benchmark, using an IF statement. In Part 2, we run 3  Monte Carlo Simulations to project retirement portfolio returns over a 30-, 10- and 5- year period, by applying different portfolio weights for stocks and bonds.  Finally, we illustrate our findings for parts 1 and 2 using charts from the matplotlib library. 

## Part 1 (Ln 1-13)
* Ln 1-2: We import the libraries and API we'll need, and load our environment. 
* Ln 3-5: We set our cryptocurrency asset weights, fetch our cryptocurrency pricing data using the required APIs, and display the value of our holdings in BTC and ETH. 
* Ln 6-8: We set the current amount of shares, set Alpaca API and Secret Keys, and create a dataframe of tickers comprised of S&P 500 (SPY) and Bonds (AGG). 
* Ln 9-11: We select and display AGG and SPY close prices, using those to compute the current value of our shares and bonds, set monthly household income and create a dataframe comprised of our Cryptocurrency and Shares (including bonds) holdings. 
* Ln 12-13: We visualize our Cryptocurrency and Shares (including bonds) holdings, using a pie chart from matplotlib. In Ln 13, we create two variables namely (1)emergency_fund and (2)  total_savings , comprised of both holdings. Finally, we create an IF statement (using variables 1 and 2), to print one of 3 comments advising the investor whether or not they have enough saved up in their emergency fund. 

## Part 2 (Ln 14-35)
* Ln 14-18: We set start and end dates of five years back from today, obtain 5 years' worth of historical data for SPY and AGG, and create a new dataframe by concatenating SPY and AGG data. We then configure a 30yr Monte Carlo ('MC') simulation, using portfolio weights of 40% bonds(AGG) and 60% stocks (SPY), over 500 simulations. 
* Ln 19-22  : We plot the results of our 30yr MC simulation in a line chart and Gaussian distribution plot, while displaying our confidence interval (under summary statistics). We end the 30yr simulation by displaying in writing the range of savings that a $20,000 investment would grow to over 30 years using the upper and lower limits of our 95% confidence interval. 
* Ln 23: Using the confidence interval above, we calculate and display the range of savings that a $30,000 investment would grow to over the same period.
* Ln 24-29: We repeat the steps in lines 19-22, but do this over for a 5yr forecast period, with a larger initial investment of $60,000 and a more aggressive weight for stocks (SPY) of 80%. 
* Ln 30-35: We repeat the steps from Ln 24-29, but set a 10yr forecast period, with a $60,000 initial investment and a slightly lower portfolio weight for stocks (SPY) of 70%. 
