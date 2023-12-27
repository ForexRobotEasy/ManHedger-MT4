# ManHedger MT4 Expert Advisor

This is the code for the ManHedger MT4 Expert Advisor, developed by the Forex Robot Easy Team. This Expert Advisor aims to automate the trading process by opening buy or sell trades based on the current market state.

## How it works

1. The code includes the necessary libraries and functions for trading, mathematical calculations, and time series analysis.

2. Constants are defined to set the grid size, grid distance, hedge multiplier, stop loss and take profit percentages.

3. The global variables `Trade` and `Series` are initialized. `Trade` is an object of the `CTrade` class, used for executing trades, while `Series` is an object of the `CTimeSeries` class, used for accessing time series data.

4. A structure `STradeInfo` is defined to store trade information, including the open price, stop loss, and take profit levels.

5. An array `trades` is declared to store the trade information, and a variable `tradeCount` is initialized to keep track of the number of trades.

6. The `OnInit` function is called during the Expert Advisor initialization. The trade slippage and deviation are set using the `SetSlippage` and `SetDeviation` methods of the `Trade` object.

7. The `OnTick` function is called on every tick of the market. It checks if there are any existing trades. If there are no trades, it determines the current market state by calculating the difference between the current and previous closing prices.

8. If the market is trending upwards, it opens buy trades. It iterates over the specified grid size and calculates the entry price, stop loss, and take profit levels for each trade. If a buy order is successfully placed using the `Buy` method of the `Trade` object, the trade information is stored in the `trades` array.

9. If the market is trending downwards, it opens sell trades. Similar to the buy trades, it calculates the entry price, stop loss, and take profit levels for each trade. If a sell order is successfully placed using the `Sell` method of the `Trade` object, the trade information is stored in the `trades` array.

10. After opening trades, the code checks for existing trades. It iterates over the `trades` array and checks if any trade has reached the stop loss or take profit levels. If so, it modifies the stop loss and take profit levels using the `PositionModify` method of the `Trade` object.

11. The `OnDeinit` function is called when the Expert Advisor is stopped. It closes all open trades using the `PositionCloseAll` method of the `Trade` object. It also resets the `trades` array and `tradeCount` variable.

## Product Description

ManHedger MT4 Expert Advisor is an automated trading tool developed by the Forex Robot Easy Team. This Expert Advisor is designed to elevate your forex trading strategy by opening buy or sell trades based on the current market state.

The Expert Advisor uses a grid trading strategy, where it opens a series of trades at specific price levels. It takes into account the current market trend and calculates the entry price, stop loss, and take profit levels for each trade.

Key Features:
- Automated trading: The Expert Advisor executes trades automatically based on predefined rules.
- Grid trading strategy: It opens a series of trades at specific price levels, allowing for potential profit in both bullish and bearish market conditions.
- Customizable parameters: You can adjust the grid size, grid distance, hedge multiplier, stop loss, and take profit percentages to suit your trading preferences.
- Risk management: The Expert Advisor includes stop loss and take profit levels to manage risk and protect your account balance.
- Trade modification: It monitors existing trades and adjusts the stop loss and take profit levels if necessary.

Please note that ForexRobotEasy is not the official developer of this product. We are only showcasing a sample code that can work as described in this product. For detailed reviews and trading results of this product, please visit the official developer's site [here](https://forexroboteasy.com/forex-robot-review/manhedger-mt4-review-elevate-your-forex-trading-strategy/). To find the official developer of this product, use MQL5.
