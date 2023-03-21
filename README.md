# Time Series
Presents portfolio optimization of stocks with TimeSeries. Libraries used: Riskfolio, Darts, Prophet, Statsmodels.api 

## Introduction
The changes in the stock prices is an exciting topic, someone likes to invest a certain budget, others like to follow the development of a company or sector.
On many websites one can build one's own portfolio. The idea is to see the desired stocks in one space. By comparing their values one can eventually decide where is better to invest.
Example: [My Portfolio](https://finance.yahoo.com/portfolios/)

Portfolio optimisation methods are used from the Riskfolio library. With this library one can easily build a portfolio optimizer to measure the risks, when investing in a group of stocks.

In this repository one can find several ways to compute preditions using machine learning models. The old way is with statsmodels. This library has ARIMA, ArmaProcess, OLS ... models which can give some predictions.
More advanced models one can find using the Darts and Prophet libraries. 
The neural network model NBEATSModel from the Darts library shows good accuracy when predicting future stock values.

## Overview Libraries

### Data Analysis
When time series data is analysed there is special attention given to the index of the data. The index becomes the Date field of the dataset. When splitting the data different technologies can be used.<br>
[analysis](https://github.com/EmiliaGenadieva/time-series/blob/main/notebooks/analysis_data.ipynb)<br>
In this notebook one can find code to download a single ticker as well as multiple tickers from the Yahoo finance website. Preview Time Series Data and perform comparisons of simple calculations.

### Portfolio Optimisation
Library used with documentation: [riskfolio-lib](https://riskfolio-lib.readthedocs.io/en/latest/portfolio.html)</br>
Data is analysed with different module functions: The portfolio is analysed with risk measures like : Semi Standard Deviation,  Conditional Value at Risk, Entropic Value at Risk, Conditional Drawdown at Risk, Worst Realisation..
Example: obj = 'MinRisk' # Objective function, could be MinRisk, MaxRet, Utility or Sharpe<br>
Notebook developed by using this library with several use cases how to display charts and calculations.<br>
[portfolio_optimisation](https://github.com/EmiliaGenadieva/time-series/blob/main/notebooks/portfolio_optimisation.ipynb)

### Darts ML Models
The developers of this library wrote it specially for time series data. Defined functions for well known models like ARIMA and ExponentialSmoothing are also included as part of their library. <br>
Backtesting of is also available: one measures the performance obtained when this model is used historically.<br>
Average error (MAPE) over forecasts is provided as part of the calculations.<br>
Exploring the data analysis and ML models from this library:<br>
[Darts with ABT PFE Stocks](https://github.com/EmiliaGenadieva/time-series/blob/main/notebooks/Darts_ABT_PFE.ipynb)<br>
[Darts with JNJ Stocks](https://github.com/EmiliaGenadieva/time-series/blob/main/notebooks/Darts-JNJ.ipynb)

### Prophet ML Models
[Library in R & Python](https://facebook.github.io/prophet/)<br>
Similar to Darts, in the Prophet python library one can find predefined models for time-series data, have predictions, test for seasonality of the data... One receives an output by using functions of this library 'The forecast object here is a new dataframe that includes a column yhat with the forecast, as well as columns for components and uncertainty intervals'<br>
Implementation of models from the Prophet library: 
[notebook_prophet](https://github.com/EmiliaGenadieva/time-series/blob/main/notebooks/prophet.ipynb)

### Statsmodels Models
In Statsmodels there are Linear Regression Models.<br>
After a model is defined and trained, one can have a summary report like (OLS Regression) Results with a detailed outcome values like Log-Likelihood(value of a regression model is a way to measure the goodness of fit for a model), R-squared, AIC(Akaike information criterion - lower AIC value, better fitting model) BIC:(Bayesian Information Criterion - lower BIC value, better fitting model)<br>
2 notebooks are included for code when predicting and analysing data:<br>
[statsmodels_notebook_1](https://github.com/EmiliaGenadieva/time-series/blob/main/notebooks/statsmodels-1.ipynb)<br>
[statsmodels_notebook_2](https://github.com/EmiliaGenadieva/time-series/blob/main/notebooks/statsmodels-2.ipynb)

## Further Improvements
There is still a lot one can improve to give a more accurate predictions for future values in the stock market.<br>
- From the Google Trends API one could get data for the relevant searches worldwide and/or for a specific country. There could be a model which takes this data into consideration and includes it by coupling the dates from Trends with the stocks dates. If there are breaking news about a company, people tend to search online with the most used search engine Google.
- One could compare the predictions from the different models and the different libraries to choose the more accurate model.
- Data used in these examples explores only Yahoo finance stock prices. One can find other sources of stock markets which give access to their stock prices in real time.





