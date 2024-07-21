# A Cryptocurrency Bot with GDAX API

This script interfaces with the GDAX api to make trades on the same exchange. Currently in ETHUSD pairs. The "buy" signal initiates a limit order at te current bid, and iterates until the order is filled. The buy signal is a combination of EMA and RSI indicators which signal that ETH is oversold. The sell signal is the opposite with overbought being the prime mover. This script is scheduled to run every 5-10 minutes using a tool such as Windows Task Scheduler.

# How It Works
- Buy Signal: The bot initiates a limit order at the current bid price when it detects that ETH is oversold based on the EMA and RSI indicators. The order is placed iteratively until it is filled.

- Sell Signal: Conversely, the bot places a sell order when the indicators signal that ETH is overbought.

- Order Execution: The bot splits the sell orders into tiered profit targets, ensuring optimal returns.

# Features
- Automated Trading: The script is designed to run automatically every 5-10 minutes using tools like Windows Task Scheduler.

- Logging: Detailed logs are maintained for every trade, including timestamps and execution details.

- Email Notifications: Users receive email alerts for buy and sell orders to stay informed about the bot's activities.

- GDAX API Integration: Seamlessly interfaces with the GDAX API to execute trades and retrieve market data.

# Prerequisites
- R and the necessary libraries (rgdax, mailR, stringi, curl, xts, TTR)
- GDAX (Coinbase Pro) account with API key, secret, and passphrase
- Configured email account for notifications

# Setup
- Clone the repository.
- Install the required R libraries.
- Update the script with your GDAX API credentials and email settings.
- Schedule the script to run at desired intervals using Windows Task Scheduler or any other task scheduling tool.
