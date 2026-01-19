#Market Risk Regime Detection with Market & Macroeconomic Signals
##Overview

This project explores market behaviour under changing economic conditions by modelling and anticipating high-volatility market regimes using a combination of market data and macroeconomic indicators.

Rather than attempting to predict prices or returns, the focus is on risk monitoring:
detecting and anticipating transitions into stressed market conditions that matter for risk management and decision-making.

The work is framed as a decision support system, not a trading strategy.

Motivation

In practice, financial institutions do not ask “What will the market price be tomorrow?”
They ask:

Are market conditions becoming unstable?

Is risk increasing beyond normal levels?

Should exposure or hedging policies be reviewed?

Volatility regimes provide a natural and interpretable way to formalise these questions.
This project therefore models future high-volatility regimes, using information that would realistically be available at the time of prediction.

User of Interest

The intended users are:

Market risk managers

Portfolio managers

Risk or investment committees

The outputs are designed to support:

Risk monitoring

Early warning alerts

Contextual analysis during macroeconomic stress

Data Sources
Market Data

Asset: S&P 500 Index (^GSPC)

Frequency: Daily

Period: 2005 – present

Fields: Open, High, Low, Close, Volume (OHLCV)

This period intentionally spans multiple market regimes, including:

The 2008 financial crisis

The COVID-19 shock

The post-2021 inflation and rate-hike environment

Macroeconomic Data (FRED)

Federal Funds Rate (monetary policy)

CPI (inflation)

Unemployment rate

VIX (market-implied fear)

Macroeconomic variables are aligned to daily frequency via forward-fill and lagged conservatively to respect information availability and avoid data leakage.

Feature Engineering
Market Features

The following features capture short- and medium-term market behaviour:

Daily returns

Rolling volatility (5, 10, 20 days)

Rolling trading volume

Intraday high–low range

Momentum over 5 and 10 days

These features describe movement, risk, liquidity, and trend strength.

Macro Features

Macroeconomic indicators provide context, rather than short-term signals:

Interest rates (cost of capital)

Inflation (economic pressure)

Unemployment (business cycle health)

VIX (forward-looking market fear)
