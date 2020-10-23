# Zee-Entertainment-Enterprises-TimeSeries

## Overview

I wanted to take a closer at **Zee Entertainment Enterprises Limited (ZEEL)**, a media and entertainment broadcasting company of the Essel Group. It owns a large group of entertainemnt channels under the brande name of __Zee__. Being as it is the primary profit generating company of the Essel Group I wanted to see if we would be able to forecast the opening and closing stock price of for ZEEL. The stock is currently valued in the $170-$180 range whcih I thought was a good place to work from to be able to see decent flucuation in the price.

## Goals:

- To build a Time Series forecasting model to predict opening and closing price for ZEEL.

- By predicting opening and closing price of the stock we should be able to see when we should buy and when we should sell.

- If we predict a week will have a lower open price than closing price we would buy more shares at the predicted low point, and sell before the market closes at weeks end.

- With small tweaks the model can be adjusted to work on a day to day scale.

- The days that we predict an open price that is lower than that day's closing price we would buy at open and sell just before close.


## The Approach
- Used the **nsepy** library to pull the ZEEL stock data from Jan 1, 2015 to October 22, 2020

- Engineer features to give model deeper insight

- Perform Exploratory Data Analysis on the data and create visualizations.

- Build and test ARIMA model to predict open and close stock prices


## Summary of Findings

- Our model performed quite well with an RMSE between 9.37 and 9.53. As you can see in the figure our predictions were quite close to the actual values.
![](https://github.com/mdetiberiis01/Zee-Entertainment-Enterprises-TimeSeries/blob/main/forecasted_price.png)

- In recent times, on average more days have had a higher open than close price which can be seen in the steady decline in share value since 2018.

- We predicted an opening price of $174.62 and a closing price of $181.96 for the week of 10/19/2020 and 10/23/2020, which is a good indication we should buy this week and sell before market close at weeks end.

-ME and AR

## Business Insight

- The week of October 19, 2020 to October 23, 2020 is a good week buy shares early in the week and sell before market close on Friday.

- ZEEL has been having more days with a lower closing price than opening price since  which would make us suggest looking for a new company to invest in in order to have higher returns at a faster rate.
![](https://github.com/mdetiberiis01/Zee-Entertainment-Enterprises-TimeSeries/blob/main/30day_average.png)

## Limitations and Future Work

- One main limitation would be regarding the nsepy library. The library only has a select few number of stock that allow historic data access. Because of this our model will not scale for all stocks.

- I would like to find an alternative data source so the model will be usable for more than the select few stocks.
