---
title: 0DTE Strategy (draft)
description: Strategy 7
date: 2024-09-04
tags:
  - strategy
permalink: "/0dte-strategy/"
---
DRAFT:

Working on a 0dte strategy. 

## Research sources

- SPX "pegging" data: https://optionalpha.com/blog/0dte-intraday-spx-historical-prices
- 0DTE time decay: https://optionalpha.com/blog/0dte-options-time-decay
- https://optionalpha.com/learn/top-0dte-options-strategies

## Notes / Thoughts

- use option alpha's 0dte oracle system to find trades with high enough reward/risk based on probability
- look at time of day entering, and choose OTM% that has a better than 50% probability of still being OTM by end of day
  - e.g. at 12pm, .03% OTM has a 61% chance of staying OTM
    - based on 60% win probability, need about 67% return on risk to make it advantageous.  Aim for higher because of commissions

- based on time decay research, exponential decay after 3:30pm.  But, it doesnt seem practical to enter a trade taht late, so just enter as late as possible?

- not sure how to close these trades automatically.  IBKR has liquidating risk because my account isnt big enough to manage assignment on SPY or QQQ.
- maybe can just trade XSP or SPX, but volume is not very good, and spreads are super wide sometimes


- maybe try to enter early in the day on a trade that's .3% OTM or more
  - .3% is always about 50% win rate, so aim for over 100% return on risk

- should i trade iron condors/butterfly or stick to one sided trades, i.e. put or call spreads
  - or should I leg into an iron condor, i.e. first open a call spread, then later open a put spread?

## Entry
- what time should I enter at?  Time decay accelerates after 3:30pm, but that is a bit late to enter a trade. So, I guess enter as late as possible?  Maybe 3pm, or 2pm. 
- Or should I have multiple entries per day?  For example, enter once at 2pm and again at 3pm?  Or 12, 1, and 2 or something.


## Other ideas / strategies
- https://www.thetaprofits.com/my-most-profitable-options-trading-strategy-0dte-breakeven-iron-condor/
- MEIC:  Multiple Entry iron condor strategy: https://www.youtube.com/watch?v=cqnL6-44ZOk / https://optionalpha.com/bots/0dte-credit-targeting-multiple-entry-synthetic-iron-condor