---
title: Long-term Trend Strategy
description: Option Selling Strategy 5
date: 2023-11-12
tags:
  - strategy
  - active
permalink: "/long-term-trend-strategy/"
---


## Basic overview

Sell 90+ days to expiry (DTE) bull put credit spreads on highly priced, fundamentally solid companies that are in long term up trends.
 
## Detailed Overview 

I screened for companies that are fundamentally (financially) solid; with a price chart that is in a long term uptrend; and currently undervalued.  

Selection of companies is similar to that of the <a href="https://options1k.com/naked-put-strategy/">Naked Put Strategy</a>. 

The main difference is that these companies are around (or over) $200 per share, which means I would need around $20k of capital/margin to sell naked puts on them.

Basically, I would like to own these companies outright, but I can't afford to.  

So, I am selling bull put spreads on them instead.

I also used backtester on optionalpha to see how well they performed over the last 5 years or so.

### Companies
For now, here are the companies I will be using this strategy with:
- **`V` (Visa)**
- <s> **`MCD` (McDonald's)**</s>  *(removed because low volume)*
- **`PG` (Procter & Gamble)**
- **`COST` (Costco)**

I may add more in the future, but three is enough for now.  I also tried to select companies in different industries, although they're all kind of related.  Aren't we all?

### Entry rules
Around the middle of each month, sell a 90 DTE bull put spread on the selected companies.  Here are the spreads for each:

- `V` : Sell put @ 0.15 delta; Buy put @ 0.10 delta
- <s> `MCD`: Sell put @ 0.15 delta; Buy put @ 0.10 delta </s>
- `PG`: Sell put @ 0.15 delta; Buy put @ 0.05 delta
- `COST`: Sell put @ 0.15 delta; Buy put @ 0.10 delta


### Exit rules
No stop loss on any of the companies.

Slightly different profit take target on each:
- `V` : 50% profit take
- <s> `MCD`: 75% profit take </s>
- `PG`: 50-75% profit take
- `COST`: 50-100% profit take

*Note: May experiment with percentages a bit*

### Allocation/Risk amount
Will start with selling 1 spread per month, per company, and work my way up (or down) from there.

This should work out to a bit under $5k of risk.  

Since there is no stop loss, I put the risk at the total of the spread.  For example, selling a 230/220 spread on `MCD` is $1000 of risk.

## Summary / Notes
This trading strategy is basically an alternative to actually investing (i.e. buying shares) in solid, profitable companies.

i.e. If I had a lot of money, I would probably just buy 100 shares of Visa.  At time of writing, it's around $245/share, so I would need $24,500 cash to do that.

I *could* just buy a few shares, but then I would not be able to sell covered calls on it.

Optimally, this strategy will provide a steady source of income each month.  Almost like dividend payments.

The main downside, of course, is that any of these companies could tank suddenly for whatever reason, and I would lose the entire cost of the spread.

I tried to be meticulous choosing financially strong companies that have exhibited years of stable price growth.  Anything can happen though.


