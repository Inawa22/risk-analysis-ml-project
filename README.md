# Market Risk Regime Detection

## Overview

This project looks at whether the S&P 500 is moving towards a high-volatility period.

Instead of predicting prices or returns, it answers a simpler question: **Is the market becoming riskier?**

It is a risk-monitoring tool, not a trading strategy.

## Who Is It For?

It could help market risk managers, portfolio managers and investment teams:

* Monitor rising risk
* Spot possible warning signs
* Review exposure or hedging decisions

## Data

The project uses daily S&P 500 data from 2005 onwards, including prices and trading volume.

It also uses:

* Interest rates
* Inflation
* Unemployment
* VIX

This period covers major events such as the 2008 financial crisis, COVID-19 and the recent rise in inflation and interest rates.

## Features

The model looks at:

* Daily returns
* Volatility over 5, 10 and 20 days
* Trading volume
* Daily price range
* Market momentum
* Interest rates, inflation, unemployment and VIX

The macroeconomic data is carefully lagged so the model only uses information that would have been available at the time. This avoids data leakage.
