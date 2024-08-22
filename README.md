# Utkarsh_231AI040_ML

Pls read after line 21 also

We’ll start by talking about what Form 4 filings and insiders are, then move on to discussing how you can use Python to gather the data from SEC EDGAR filings. After that, we will use various Python libraries to perform some basic analysis on the gathered data to generate potential buy and sell indicators to copy and follow insider trading activity.

Our objective is to discover trading patterns that forecast stock price shifts.

We begin by constructing our local database of insider trades for the years 2012 to 2022.

1.) Downloading Form 3, 4 and 5 filings which have been converted from XML to JSON
2.) Extracting all insider transactions from the JSON filings
3. Cleaning transactions (e.g. removing incorrectly reported trades)

4. Augmenting transactions with sector and industry information

5. Analyzing the data

The get_data() method provides a search interface that accepts a JSON formatted search query and returns all Form 3, 4 and 5 filings that match our query. The return value represents a JSON object (Python dictionary) that holds matching filings in a list behind the transactions key.

### My colab was not working properly after this But these are the processes which I wanted to do after this:
Data Cleaning
In the next step, we focus on cleaning the transactions.


