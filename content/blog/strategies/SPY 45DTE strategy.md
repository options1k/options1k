---
title: SPY 45+ DTE Bull Put Spread
description: Option Selling Strategy
date: 2025-01-24
tags:
  - strategy
  - active
permalink: "/spy-45dte-strategy/"
---

## Basic overview

Sell 45+ days to expiry (DTE) bull put spreads on `SPY` every week.  Close at 60% profit target, or at 21 DTE (win or lose).
 
## Detailed Overview 

This is a strategy that I have cobbled together from various sources - [Options with Davis](https://optionswithdavis.com/), [Data Driven Options](https://datadrivenoptions.com/strategies-for-option-trading/favorite-strategies/credit-put-spread/), and The Trade Busters (a little bit).  They all seem to be originally based on research from Tasty Trade.


### Entry 

Every week, I will enter a bull put spread (i.e. credit put spread) on `SPY`.  

Will start with selling one spread every Monday, which is sort of an arbitrary choice.  Perhaps will add more positions on other days of the week to scale this strategy up.

The average delta of the spread will be around 16.  This is because Theta decay is supposed to be highest at this level (based on research from [Data Driven Options](https://datadrivenoptions.com/strategies-for-option-trading/favorite-strategies/credit-put-spread/)).

So, if the short put has delta of 20, then the long put will have delta of 13~.

Risk of each trade will be around 1% risk of my portfolio. 

So, if my portfolio is around $40k+, then I will risk around $400-$500 per trade (e.g. 450/445 spread = sell put at 450, buy put at 445).

Days to expiry will be a minimum of 45 days.  Prefer slightly longer if possible, i.e. 50-60 days


### Exit rules

- Profit take at 60% of premium received.  E.g. if I collect $100 credit initially, I will close the trade when I can buy the position back for $40.
- Exit at 21DTE regardless if the position is winning or losing.


### Allocation/Risk amount

Starting with just one trade per week on `SPY`.  Spread width around $5.

If profitable, can start scaling up by increasing width of the credit spread, or by selling more positions on other days of the week.

If not profitable, then I will just stop tading it.  But, I need a lot more trades before I decide that.

## Summary / Notes

This strategy replaces my old [10DTE SPY strategy](/spy-10day-strategy/), which I felt was taking too much risk despite being very profitable in 2024.

Based on research from people much smarter than me, there is advantage of selling 45+ DTE, as the volatility is generally overstated over that time length (or longer).  Backtesting also shows that consistently selling puts at 45+ DTE outperforms the actual index.

I should probably do my own backtesting to better understand this all.

This strategy will probably work very well in strong bull markets like 2024.  Curious to see how it does if the market goes flat or down. 