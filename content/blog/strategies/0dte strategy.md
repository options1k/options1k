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

Some notes and stuff:

- SPX "pegging" data: https://optionalpha.com/blog/0dte-intraday-spx-historical-prices
- 0DTE time decay: https://optionalpha.com/blog/0dte-options-time-decay


- use option alpha's 0dte oracle system to find trades with high enough reward/risk based on probability
- look at time of day entering, and choose OTM% that has a better than 50% probability of still being OTM by end of day
  - e.g. at 12pm, .03% OTM has a 61% chance of staying OTM
    - based on 60% win probability, need about 67% return on risk to make it advantageous.  Aim for higher because of commissions

- based on time decay research, exponential decay after 3:30pm.  But, it doesnt seem practical to enter a trade taht late, so just enter as late as possible?

- not sure how to close these trades automatically.  IBKR has liquidating risk because my account isnt big enough to manage assignment on SPY or QQQ.
- maybe can just trade XSP, but volume is not very good, and spreads are super wide sometimes


- maybe try to enter early in the day on a trade that's .3% OTM or more
  - .3% is always about 50% win rate, so aim for over 100% return on risk