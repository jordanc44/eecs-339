# EECS 339 - Portfolio

Will Parsons, Jordan Clark, Kyle Pickard

EECS 339 Databases Lab 2: Portfolio Manager

[Storyboard / flowchart](FlowchartPortfolio.pdf) 

[ER diagram](ER.pdf)

[Relational design](Relational%20Diagram%20&%20All%20SQL%20Queries.pdf)

[SQL DDL](SQL%20DDL.pdf)

[SQL DML and DQL](SQL%20DML.pdf)

Link to application: https://murphy.wot.eecs.northwestern.edu/~jlc229/portfolio/portfolio.pl

A valid user with pre-existing portfolios is: will
The password for that user is: password

This lab completes all the specifications as laid out in the prompt for the assignment. Starting at the top, a user can either sign up or log in, and from there has access to the list of portfolios their account has created. A user can create a new portfolio, or click on a preexisting one. The portfolio view page contains many important features, including the current amount of money in the portfolio, a list of all the holdings and the quantities of stocks in the holdings, various statistics on the portfolio including the coefficients of variation and the beta values, the current value of the portfolio (stock values + cash) and many links to other features. By clicking on a stock, a user can query the historic and daily entered data to see a table of all the important values within the time range & a graph of the stocks value over that range. Additionally, the user can run an automated trading strategy over various configurable parameters for the stock or get the future predicted value of the stock over a configurable number of steps. All graphs for the stocks get properly generated and all important information is returned. Back at the portfolio level, the user can either manually enter daily stock data or can pull the most recent stock data for a proper ticker, any attempts to use an invalid ticker will not succeed at any point in this portfolio manager. At the portfolio level a user can deposit money into the portfolio or withdraw money from the portfolio. Additionally, the user can buy or sell stocks with valid tickers, which the buy and sell page displays alongside the most recent prices of the stocks. All transactions will update the cash amount in the portfolio, and all stock values are the most recent fetched data available.


EXTRA CREDIT:
BETTER HISTORICAL DATA:
./history_fill.pl
        history_fill.pl loops through all possible symbols using get_symbols.pl
        for each symbol, history_fill.pl pulls daily information from investopedia.com's historical database
        history_fill.pl scrapes daily information from 07/01/06, the day after the end of the original dataset to 2/26/19
        history_fill.pl adds the stock data to our daily_stocks table (our equivalent to cs339.StocksDaily)
        after running once, our lab has full historical data through 2/26/19 instead of 6/30/06
