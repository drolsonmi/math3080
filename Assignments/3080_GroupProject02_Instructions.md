# Math 3080 - Group Project 2

[(Downloadable Jupyter Notebook of this project): https://github.com/drolsonmi/math3080/Assignments/3080_GroupProject02.ipynb](https://github.com/drolsonmi/math3080/Assignments/3080_GroupProject02.ipynb)


In this project, we are going to do an analysis of stock data. In this project, we will practice the following:
* Loading API data
* Manipulating DataFrames
* Joins
* Datetime objects
* Graphing

We are going to obtain stock data from the Alpha Vantage service API service. Here are a couple of helps:
* [Alpha Vantage FAQs](https://www.alphavantage.co/support/#api-key)
* [Alpha Vantage Documentation](https://www.alphavantage.co/documentation/)
  * We will focus on the __DAILY_ADJUSTED__ dataset. You are welcome to experiment and play with the other datasets.

API keys will be emailed to you before this project begins.

You may also want to look back at the *05 Obtaining Data.ipynb* notes to remind yourself of how APIs work.

-----
For this project, we will work with 5 datasets: 
* Google / Alphabet Inc (GOOGL)
* Tesla (TSLA)
* Amazon (AMZN)
* AT&T (T)
* Ford (F)

1. Load the Google dataset
2. Wrangle the data so that,
    * there are two columns for the date and closing values
    * the dates are in datetime format and closing values are floats (You may need to use a .apply() method to turn values into a float)
3. Load the other 4 datasets the same way
4. Join the 5 DataFrames on the dates
5. Show the final DataFrame
6. Plot the 5 stocks over
    * The past month
    * The past 6 months
    * The past year
    * The past 5 years
    * Make sure that each plot has an appropriate title and x- and y-axis labels.

> Notice that there is a sudden drop in the values of Google, Amazon, and Tesla stocks. This happens when the company changes the value of the stocks.
> * If you have 10 stocks at \$100 each, then you'll have 20 stocks at \$50 each after the change
> 
> Also, notice how these stocks are at such different values. We need to scale them so we can compare them.

7. Standardize the stocks and replot them for the last year
8. Show the 15-point rolling average for all standardized stocks for the past year. 
9. What observations can you make from this graph?
10. Find the correlation between all stocks.
    * Experiment to find the best way to find the clearest correlation - correlation between averages, percent changes (stock returns), rolling averages,...
11. How would you describe the relationship between each pair of stocks?