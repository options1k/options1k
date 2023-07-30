---
title: Stochastics + Support/Resistance (Gin Lim Strategy)
description: Strategy 1
# date: 2023-04-25
tags:
  - strategy
permalink: "/gin-lim-strategy/"
---
This is an option selling strategy I adapted from Gin Lim over at <a href="https://passiveseeds.com/">passiveseeds.com</a>

## Basic overview
Sell bull put spreads when stock is oversold and near support.  
Sell bear call spreads when stock is overbought and near resistance.

## Detailed Overview
There's a lot more to it than that.  Here are the detailed entry, exit, and sizing rules:

### Entry rules
1. Probability of profit (i.e. Probability out of the money) > 75%
1. High liquidity (Open interest > 300)
1. Tight Bid Ask Spread (< $1)
1. Expiry in 40-60 days
1. No earnings in next 3 weeks
1. Initial profit target (premium / spread-premium) > 15% 
1. Stochastics oversold (< 20) for puts; overbought (>80) for calls
1. Strike is below support for puts; above resistance for calls
1. Price is in uptrend for puts; downtrend for calls; or flat/sideways range
1. Other: When overall stock market is volatile, look for Implied Volatility Percentile > 30%

### Exit rules
1. Take profit at 50% of initial collected premium 
2. Take loss at 200% of initial collected premium (or 4:1 profit target)
3. Take loss if support/resistance is broken (full candle below support/resistance)


### Risk level + trade sizing
1% risk per trade based on exit plan.  

My current capital is about 30k, so my **max risk per trade is about $300**.

I must exit the trade when my net loss is at 200% of collected premium, and take profits at 50% (i.e. 4:1 risk/profit)

Since my max risk/loss is $300, my target take profit is $75, so **my target for initial premium collected is $150**. 

Based on my rules, I need to win over 80% of my trades to be profitable.  It's not exact, as I may take wins/losses early, but it's a general target to aim for.

**Example**

If the premium collected per option sold is $50, then I should sell 3 options (i.e. $150 collected).  
I would take profits when I can buy back the position at $25 per spread (i.e. 50% profit target = $75 profit).  
I would cut my losses when the price of the option reaches $150 per spread (i.e. $450 cost - $150 collected premium = $300 net loss).

## Summary / Pros / Cons
The most important thing when using this strategy is to cut your losses.  Everything falls apart if you don't, as I <a href="/how-i-lost-2-986-in-july-2023-trading-options/">experienced</a>.

You won't win every trade, so just take your losses and move on.

When sticking to the rules, I have been mildly profitable.  Gin seems to do really well with this basic strategy.

The thing I don't like about this strategy is you have to look at your positions everyday to check if you need to exit or not.  Not a huge deal, but you can't completely set-it-and-forget-it. 

Also, scanning and picking trades based on support/resisntance levels can be pretty subjective.
