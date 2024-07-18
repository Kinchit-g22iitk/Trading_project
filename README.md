# Forex Trading Strategy using FXCM API

## Overview

This project implements an automated Forex trading strategy using the FXCM API. The strategy utilizes the Moving Average Convergence Divergence (MACD), Average True Range (ATR), and Renko charts to generate trade signals and manage positions in various currency pairs.

## Features

- **Currency Pairs:** The strategy can trade multiple currency pairs including EUR/USD, GBP/USD, USD/CHF, AUD/USD, and USD/CAD.
- **Technical Indicators:**
  - **MACD:** Used to identify potential buy or sell signals based on the convergence and divergence of moving averages.
  - **ATR:** Used to calculate the True Range and Average True Range, which are essential for determining the volatility of the market.
  - **Renko Charts:** Used to filter out noise and identify the overall trend of the market.
- **Trade Signals:**
  - **Buy Signal:** Initiated when specific conditions in MACD and Renko charts are met.
  - **Sell Signal:** Initiated when specific conditions in MACD and Renko charts are met.
  - **Close Positions:** The strategy can close existing positions based on the signals generated.
- **Automated Execution:** The strategy continuously monitors the market and executes trades at regular intervals (every 5 minutes).

## Requirements

- FXCM API token
- Python libraries: fxcmpy, numpy, stocktrends, statsmodels

## Setup

1. Install the required Python libraries.
2. Obtain an FXCM API token and save it in a text file.
3. Modify the token path in the script to point to your token file.

## How It Works

1. **Initialize API Connection:** Connect to the FXCM API using the provided token.
2. **Fetch Market Data:** Retrieve historical market data for the specified currency pairs.
3. **Calculate Indicators:** Compute MACD, ATR, and Renko charts for the market data.
4. **Generate Trade Signals:** Based on the calculated indicators, generate buy, sell, or close signals.
5. **Execute Trades:** Place or close trades according to the generated signals.
6. **Continuous Monitoring:** The script runs continuously, fetching new market data and making trade decisions at regular intervals.
