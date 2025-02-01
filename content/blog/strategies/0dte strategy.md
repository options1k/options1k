---
title: 0DTE Strategy
description: Strategy 7
date: 2025-01-27
tags:
  - strategy
  - active
permalink: "/0dte-strategy/"
draft: true
---

On this page is a collection of 0DTE strategies I currently use.  
There is only one right now:

## SPX EMA Strategy / METF Strategy

This is a strategy I first read about on [thetaprofits blog](https://www.thetaprofits.com/how-to-trade-the-metf-0dte-options-strategy/) -- called the METF (Multiple Entry Trend Following) 0DTE Options Strategy.

At certain/multiple times during the day, you compare two EMA lines (exponential moving average) on the `SPX`.  If the shorter EMA (i.e. 20) is above the longer EMA (i.e. 50), then it indicates an uptrend.  

In an uptrend, you sell a bull put spread (i.e. put credit spread).

In a downtrend, you would sell a bear call spread.

That's it.

The exact EMAs to use (i.e. 5, 20, 40, etc.), time of day, chart time frame (i.e. 1min, 5min), strike prices, target credit/premium, stop loss, etc., depends on individual preferences.  

Here are the parameters I currently use:

### Entry Parameters

- Ticker: `SPX` 
- 20/40 EMAs on a 1min chart;  if 20 is above 40 on specified entry time, then enter a Bull Put Spread; if 20 is below 40, then enter a Bear Call Spread.
- Target credit: 0.85 - 1.25 (i.e. minimum premium received is $0.85 per spread, max $1.25)
- Strike spread width:  Min spread of 25 points; Max spread of 60 points (e.g. Sell put is 5000; buy put is 4940)
- Delta target:  No specific delta, but as far away from the current (i.e. at the money) price  as possible
- Multiple entry times based on backtest:

#### Entry Times:

The entry times I use are based on backtests from the wonderful (and free) [BYOB tool](https://tradeautomationtoolbox.com/byob-ticks/).  I use the above listed entry parameters.

I export all the trades from the backtest, and see which times on which days have the most positive return.  I compare the past 3 months, 6 months, and 12 months. 

For example, at time of writing this, 2:30pm on Mondays has good returns recently, so I would enter a trade at that time.

Will share my spreadsheet of best times later on.

### Exit

- **Stop loss**: 100% of credit received.  
  - E.g:  If I receive $1 credit from selling my initial bull or bear credit spread, then I will exit the trade if the price to buy back the spread is $2 (i.e. net loss of $1).
  - Will experiment with putting stop loss on entire spread, or just the short leg.

<p></p>

- **Profit Target**: 50% - 100% of credit received
  - Will experiment with taking profits early (i.e. 50+%), or letting everything go to expiry (i.e. 100%).  Backtests typically show that letting positions go to expiry have better returns overall, but also have bigger drawdowns / more volatility.

### Allocation

Maximum 1% loss per day (of portfolio size).  

If my portfolio is around $30k, then my max loss is about $300 per day.  

Since my target credit is around $1, and my stop loss is 100% of credit, then my maximum loss per trade is also $1.

That means I can take a maximum three positions per day (3 max losses = $300)

If I exit a position early for profit, then technically I can enter more trades afterwards.

May experiment with looking at max 5% loss per week instead of 1% per day, so I can risk more capital on good days.  E.g: If Mondays have been historically much better than Wednesdays, I may risk more on Mondays and trade less on Wednesdays.

## Automation

I am currently using [Trade Automation Toolbox](https://tradeautomationtoolbox.com/) (i.e. TAT) to automate my 0DTE trades.  

It is a bit pricey for beginners ($50/month subscription + $40/month Windows VPS cost), but has worked well so far.  

Hopefully I can make enough to cover the subscription costs. 😅


## Notes / Thoughts on EMA/METF Strategy

The METF strategy has been profitable the first couple months of testing it.  Hopefully, I can scale it up over time.  

It can be pretty hard to look at the losing days.  The automation software helps a lot with this, as you can just ignore it for a day and let everything run.  I did trade manually at first as I thought the automation software was a bit expensive.  I thought about coding my own basic version, but I am pretty satisfied with TAT right now.

I chose the 20/40 EMA sort of arbitrarly.  I see many traders using 5/40 or 5/20 EMAs instead, which is a lot more choppy.  I guess I like the slighlty smoother 20/40 lines.

Perhaps will do some more of my own backtesting with different EMAs or trendlines later on.

## Other potential ideas / strategies

Some future 0DTE strategies/research to consider:
- SPX "pegging" data: https://optionalpha.com/blog/0dte-intraday-spx-historical-prices
- 0DTE time decay: https://optionalpha.com/blog/0dte-options-time-decay
- https://optionalpha.com/learn/top-0dte-options-strategies
- Breakeven Iron Condor: https://www.thetaprofits.com/my-most-profitable-options-trading-strategy-0dte-breakeven-iron-condor/
- MEIC:  Multiple Entry iron condor strategy: https://www.youtube.com/watch?v=cqnL6-44ZOk / https://optionalpha.com/bots/0dte-credit-targeting-multiple-entry-synthetic-iron-condor