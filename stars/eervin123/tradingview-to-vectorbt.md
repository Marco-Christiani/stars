---
repo: eervin123/tradingview-to-vectorbt
url: 'https://github.com/eervin123/tradingview-to-vectorbt'
homepage: null
starredAt: '2023-03-31T21:31:06Z'
createdAt: '2022-02-07T18:08:15Z'
updatedAt: '2025-11-25T02:05:30Z'
language: Jupyter Notebook
license: NA
branch: master
stars: 23
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:35:00.136Z'
description: null
tags: []
---

# Converting Tradingview Trade Files to VectorBT strategies

Run a backtested strategy in pinescript in tradingview. Then download the trades from tradingview into a csv.

![TV Strategy Backtest View](images/tv_strategy_screenshot_1.jpg)
![TV Strategy Trades View](images/tv_strategy_screenshot_2.jpg)

Drop that csv into the `data` folder and import the trades into a vectorbt backtested portfolio. Note, you will also need to download data of the actual series you are running. eg. In this case I am using `ETHUSDT` 2 hour data from Binance and my start date is 2018-01-01.

Once you run the trades through into a strategy and portfolio, you can see the following preview of the output.

![Strategy Output](images/strategy_results.png)
