# README
## Ibovespa Index Comparison

This script compares the performance of an equal-weighted Ibovespa index with the traditional market-cap weighted Ibovespa index. It retrieves the list of Ibovespa stocks from the Status Invest website, calculates their daily returns, and plots the cumulative returns for both indices over a specified period, highlighting the performance differences through sectoral comparisons of returns.

### Requirements
- Python 3.x
- cloudscraper library
- beautifulsoup4 library
- yfinance library
- pandas library
- matplotlib library

### Functionality
1. Disable Logging for yfinance:
The script disables logging for the yfinance library to avoid cluttered output.

2. Retrieve Ibovespa Stocks:
The "obter_ativos_ibovespa" function scrapes the Status Invest website to retrieve the current list of stocks in the Ibovespa index. The ticker symbols are adjusted to be compatible with Yahoo Finance by appending .SA.

3. Download Stock Data:
The script downloads the adjusted closing prices for the Ibovespa stocks over a specified period using yfinance.

4. Calculate Daily Returns:
It computes the daily returns for each stock and handles missing values by replacing them with the mean of the respective row.

5. Equal-Weighted Index Calculation:
The script calculates the daily returns of an equal-weighted index by averaging the daily returns of all stocks.

6. Download Traditional Ibovespa Data:
The script also downloads the adjusted closing prices for the traditional Ibovespa index and calculates its daily returns.

7. Plot Cumulative Returns:
Both the equal-weighted and traditional Ibovespa indices' cumulative returns are plotted on the same graph for comparison.

### Customization
Period for Data Download:
Change the "periodo" variable to adjust the time frame for which stock data is downloaded (e.g., "1y" for one year, "6mo" for six months).
Modify the script to include any additional tickers or sectors of interest.
Run the script to generate cumulative return plots and sectoral contribution analysis.

### Description
The script performs the following tasks:

- Retrieves ticker symbols of companies listed in the Ibovespa index.
- Fetches sector-specific ticker symbols from Status Invest.
- Calculates cumulative returns for Ibovespa Equal Weighted and Traditional indices.
- Analyzes contributions to the return differential by specific sectors (Energy & Utility, Consumption, Housing & Materials, Financial, Industrial, and Tech).

### Example Output
The script generates plots illustrating the cumulative returns of Ibovespa Equal Weighted and Traditional indices. It also provides insights into how specific sectors and individual stocks contribute to the return differences between the two indices.

### Notes
Ensure you have a stable internet connection, as the script fetches data from online sources.
Be aware of the API rate limits imposed by Yahoo Finance.

### Author
Carlos Peixer

Feel free to contribute or report issues via the project's repository.
