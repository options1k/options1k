---
title: 90 DTE Microsoft Bull Put Spreads (MSFT Strategy)
description: Option Selling Strategy 2
date: 2023-08-08
tags:
  - strategy
permalink: "/90dte-msft-strategy/"
---
This is an option selling strategy of Microsoft (`MSFT`) I found via backtests on <a href="https://optionalpha.com">optionalpha.com</a>. 

Based on the backtests (approx 10 years), returns easily outperforms `S&P500`, as well as underlying `MSFT` stock (depending on allocation amount).

Best of all, it has extremely high win rate (> 95%).  

There are a many variations of the strategy based on frequency, allocation amount, spread size, profit taking etc.  I'm going to try a couple variations for now:

## Basic overview
1. *Every week* sell a 90 day to expiry (DTE) put credit spread on `MSFT` at .15/.10 delta.

2. *Every month* sell 90 DTE put credit spread on `MSFT` at .15/.05 delta

## Detailed Overview
There's not much more to it than that, other than how much money I want to allocate to this, and when to exit the position.  

Basically, I have to be a robot and sell put spreads every week and month.  I would just use Option Alpha's autotrading bots, but it doesn't work with Interactive Brokers yet.

### Entry rules
1. Every Monday or Tuesday, sell a 90DTE put spread (0.15 / 0.10 delta).
2. Every 15th to 20th of the month, sell a 90DTE put spread (0.15 / 0.05 delta)

- Note:  Doesn't have to be exactly 90 days.  Can be a bit less or more (i.e. 80 to 100+).

### Exit rules
1. Take profit at 50% of initial collected premium.

- Note: May experiment with percentage a bit


### Allocation amount
For now, I'm going to allocate just around $5,000 towards this strategy.

There is no cut/stop loss target for this strategy, so the total risk is the width of the spread.

Example:  Sell one 300/290 put spread.  Width of $10, so total risk is $1000.

So, if I already have five $10 put spreads, I won't enter any more positions.


## Summary / Notes

Will this shit actually work?

Based on the backtests, it has like 98% win rate, and over 300% return (over 10 years).  If you increase allocation amount to like $20k, you get like 900% return??

Seems a bit crazy, so always need to keep in mind:

>> *"Past results are no guarantee of future performance."*

Microsoft could always tank for whatever reason, and I will lose all my money.  I think $5k is OK for testing this strategy out for awhile.  I've lost much more than $5k in the past 😅

