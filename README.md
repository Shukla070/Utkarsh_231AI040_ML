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

##DATA GATHERING
type of transaction (bought or sold),
security title (common stock, warrant, etc.),
transaction code,
number of shares acquired/disposed,
share price,
total $ amount of transaction, and
shares owned following the transaction.

### My colab was not working properly after this But these are the processes which I wanted to do after this:
##Data Cleaning
In the next step, we focus on cleaning the transactions.

 In particular, we remove transactions that meet any of the following criteria:

Number of shares = share price
Share price > $6,000 and number of shares is not 1
Total amount per transaction < $1
Transaction code is M representing the exercise or conversion of derivative security exempted pursuant to Rule 16b-3
Incorrect ticker, e.g. “NONE”, “N/A”
Incorrect reporter with CIK matching 810893, 1454510, etc.

##Analysis
Finally, we’re ready to start analyzing the data. First, we set some basic styling props for our charts and define a millions_formatter() helper function to format the axis of charts. The helper transforms general numbers into a financial format, for example 20000000 becomes $ 20 M.

 we start with plotting the total amount of all purchase and sale transactions per year from 2012 to 2022.

 The following code calculates the total number of securities acquired and disposed per day. It first creates two separate dataframes, one containing the total number of securities acquired, and another containing the total number of securities disposed.


 
