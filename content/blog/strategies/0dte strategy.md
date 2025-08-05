---
title: 0DTE Strategies
description: Strategy 7
date: 2025-01-27
tags:
  - strategy
  - active
permalink: "/0dte-strategy/"

---

On this page is a collection of 0DTE strategies I currently use.  

- [SPX METF](#spx-metf-strategy)
- [$5 Iron Condor Strategy on SPX](#spx-5-iron-condor-strategy)
- [Hybrid Iron Condor on SPX](#hybrid-ic-strategy-spx)

-----

## SPX METF Strategy

This is a strategy I first read about on [thetaprofits blog](https://www.thetaprofits.com/how-to-trade-the-metf-0dte-options-strategy/) -- called the METF (Multiple Entry Trend Following) 0DTE Options Strategy.

At certain/multiple times during the day, you compare two EMA lines (exponential moving average) on `SPX`.  If the shorter EMA (i.e. 20) is above the longer EMA (i.e. 50), then it indicates an uptrend.  

In an uptrend, you sell a bull put spread (i.e. put credit spread).

In a downtrend, you would sell a bear call spread.

That's it.

The exact EMAs to use (i.e. 5, 20, 40, etc.), time of day, chart time frame (i.e. 1min, 5min), strike prices, target credit/premium, stop loss, etc., depends on individual preferences.  

Here are the parameters I currently use:

### Entry Parameters

- Ticker: `SPX` 
- 20/40 EMAs on a 1min chart;  if 20 is above 40 on specified entry time, then enter a Bull Put Spread; if 20 is below 40, then enter a Bear Call Spread.
- Target credit: 0.85 - 1.25 (i.e. minimum premium received is $0.85 per spread, max $1.25)
- Strike spread width:  Min spread of 40 points; Max spread of 70 points (e.g. Sell put is 5000; buy put is 4930)
- Delta target:  No specific delta, but as far away from the current (i.e. at the money) price as possible
- Multiple entry times based on backtest:

#### Entry Times:

The entry times I use are based on backtests from the wonderful (and free) [BYOB tool](https://tradeautomationtoolbox.com/byob-ticks/).  I use the above listed entry parameters.

I export all the trades from the backtest, and see which times on which days have the most positive return.  I compare the past 3 months, 6 months, 12 months, and 100 trades.

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

### Automation

I am currently using [Trade Automation Toolbox](https://tradeautomationtoolbox.com/) (i.e. TAT) to automate my 0DTE trades.  

It is a bit pricey for beginners ($50/month subscription + $40/month Windows VPS cost), but has worked well so far.  

Hopefully I can make enough to cover the subscription costs. 😅


### Notes / Thoughts on EMA/METF Strategy

The METF strategy has been profitable the first couple months of testing it.  Hopefully, I can scale it up over time.  

It can be pretty hard to look at the losing days.  The automation software helps a lot with this, as you can just ignore it for a day and let everything run.  I did trade manually at first as I thought the automation software was a bit expensive.  I thought about coding my own basic version, but I am pretty satisfied with TAT right now.

I chose the 20/40 EMA sort of arbitrarly.  I see many traders using 5/40 or 5/20 EMAs instead, which is a lot more choppy.  I guess I like the slighlty smoother 20/40 lines.

Perhaps will do some more of my own backtesting with different EMAs or trendlines later on.

-----

## SPX $5 Iron Condor Strategy

A very simple strategy originally based on this [Option Alpha backtest](https://app.optionalpha.com/zdte/backtester/test/ZT21740248505387007279).  Option Alpha also did a [Youtube video](https://www.youtube.com/watch?v=Iy__R2cWrrI) for similar strategy.

The baseline strategy is to sell a 30 delta iron condor with $5 wide wings everyday at 2:30pm. I thought to improve the strategy by backtesting different times and deltas on each day of the week.

For example, [this backtest](https://app.optionalpha.com/zdte/backtester/test/ZT21740679708505991266) (by someone else) improved on results by trading at 1:45pm on Mon/Tues/Fri only, with VIX<20.

Here are my current optimal setups by day:

### Basic parameters
- Ticker: `SPX`
- Iron condor with $5 wings (e.g. 5000/4995 put credit spread; 5050/5055 call credit spread)
- Delta: 25-30 (may differ by day, see below)
- Entry times (different per day, see below):

### Monday
- **Entry time:** 1:45pm ([backtest](https://app.optionalpha.com/zdte/backtester/compare/ZT217474737399306521846,ZT217474737252432381845,ZT217474737703108341847,ZT217474737960967671848,ZT217474738365520371850))
- **Delta:** 25 - 35 (higher delta seems better; even 40 delta is not bad - [backtest](https://app.optionalpha.com/zdte/backtester/compare/ZT217542954319500461599,ZT217542954686406831600,ZT217542955145696931601,ZT217542955548760681602,ZT217542957070627241604)) 
- **Notes:**  9:35am also has good results, but down a bit more over [past year](https://app.optionalpha.com/zdte/backtester/compare/ZT2174161280181970132,ZT2174161291724766034,ZT2174161305423016036,ZT2174161314060112438). Restricting entries by VIX does not improve results. 11:00am is actually better over past year.
- **Results:** Profit: 5030; max drawdown 1610; profit factor 1.46

### Tuesday
- **Entry time:** 11:25am (11:15-11:30am all good)([backtest](https://app.optionalpha.com/zdte/backtester/compare/ZT217474746360380341874,ZT217474746644283151875,ZT217474747104471771876,ZT217474747389971861878,ZT217474747540383561879))
- **Delta:** 20 (15-30 all decent: [backtest](https://app.optionalpha.com/zdte/backtester/compare/ZT217543771766695351953,ZT217543772066218101954,ZT217543772383365051956,ZT217543773049922811957)) 
- **Notes:**  10:30am was best entry until June 2024, but it is down over [past year](https://app.optionalpha.com/zdte/backtester/compare/ZT2174161280181970132,ZT2174161291724766034,ZT2174161305423016036,ZT2174161314060112438). 1:45 entry is also OK. [VIX backtest](https://app.optionalpha.com/zdte/backtester/compare/ZT217474747389971861878,ZT217474753881942111897,ZT217474754003396991899,ZT217474754278024621900,ZT217474754732154291902)
- **Results:** Profit: $8179; max drawdown 1210; profit factor 1.84

### Wednesday
- **Entry time:** 12:00pm([backtest](https://app.optionalpha.com/zdte/backtester/compare/ZT217474757024541561909,ZT217474756787645671907,ZT217474757383251661910,ZT217474757518123951911,ZT217474757653018201912))
- **Delta:** 25 (lower is worse - [backtest](https://app.optionalpha.com/zdte/backtester/compare/ZT217474757024541561909,ZT217474761902547471922,ZT217474762214669031923))
- **Notes:**  Results are pretty flat over past year, could decide not to trade Wednesday.
- **Results:** Profit: 3456; max drawdown 1612; profit factor 1.23

### Thursday
- **Entry time:** 2:30pm (earlier times have negative returns - [backtest](https://app.optionalpha.com/zdte/backtester/compare/ZT217474766300936031934,ZT217474780431348171945,ZT217474780580618051946,ZT217474780704941531947,ZT217474780840462181948))
- **Delta:** 30 (25 delta is also good; max 32  - [backtest](https://app.optionalpha.com/zdte/backtester/compare/ZT217474766300936031934,ZT217474782306060301949,ZT217474782631156921950,ZT217474782876897821951,ZT217474788333941511952))
- **Notes:**  Early profit take (50%) improves results slightly at 25 delta ([backtest](https://app.optionalpha.com/zdte/backtester/compare/ZT217474766300936031934,ZT217478881210061091599,ZT217478882059519811602))
- **Results:** Profit: 5557; max drawdown 1628; profit factor 1.42

### Friday
- **Entry time:** 3:15pm ([backtest](https://app.optionalpha.com/zdte/backtester/compare/ZT217474794092906171954,ZT217474794219033721955,ZT217474794362378181956,ZT217474794460919001958,ZT217474794594404621959))
- **Delta:** 25-35 (20-35 delta all pretty good  - [backtest](https://app.optionalpha.com/zdte/backtester/compare/ZT217474794092906171954,ZT217474795207535191961,ZT217474796173414131962,ZT217474796723308681964) )
- **Notes:**  
- **Results:** Profit: 8565; max drawdown 767; profit factor 1.9

### Summary / Notes

Best backtest by day of week combined: [Link](https://app.optionalpha.com/zdte/backtester/compare/ZT217474737252432381845,ZT21747490139793901210,ZT21747490197727591212,ZT21747490291669446220,ZT21747490358763528234?combine=1)

Maybe need to think about not trading on Wednesday, as results are not that great over past year.  Could instead increase allocation on Friday as it has best profit factor?

-----

## Hybrid IC Strategy SPX

I thought to further build on the above iron condor strategy by splitting it into separate parts.  

Basically, enter the put side and call side at different times/deltas to see if it improves results.

Initially, here were the baseline tests:

PUT CREDIT SPREAD:
 - 30 delta, bull put spread everyday at 2:30pm 
 - SPX > daily 10ema
 - [Backtest](https://app.optionalpha.com/zdte/backtester/test/ZT21747493634159626453)

CALL CREDIT SPREAD
 - 25 delta, bear call spread everyday at 3:00pm 
 - VIX<25
 - [Backtest](https://app.optionalpha.com/zdte/backtester/test/ZT21743608510600244157)

I realized though that I am basicaly doubling a lot of my entries of the daily iron condor strategy above. So, I decided to only enter if the best times were significantly different.

### Monday
- ~~Put side: 2:30pm~~ (same as IC, don't enter)
- ~~Call side: 2:00pm~~ (same as IC, don't enter)

### Tuesday
- Put side: 1:00pm, 35delta ([backtest](https://app.optionalpha.com/zdte/backtester/compare/ZT21747495335639834492,ZT21747495393162465495,ZT21747495409932863497,ZT21747496106447022533))
- Call side: 2:00pm, 20 delta ([backtest](https://app.optionalpha.com/zdte/backtester/compare/ZT21747497886676099648,ZT21747497998046112663,ZT21747498029152429666,ZT21747498051757151671,ZT21747498077315924676))
  - Note:  call side has very choppy returns, could just enter put side.

### Wednesday
- ~~Put side: 12pm~~ (same as IC, don't enter) ([backtest](https://app.optionalpha.com/zdte/backtester/compare/ZT21747495576868720503,ZT2174549846014539922,ZT2174549851708044325,ZT2174549857195395526,ZT21747495563509354502))
- ~~Call side: 12pm~~ (same as IC, also results aren't great)

### Thursday
- ~~Put side: 230pm~~ (same as IC, don't enter) [backtest](https://app.optionalpha.com/zdte/backtester/compare/ZT217454977618737779,ZT2174549891601390430,ZT2174549893731807731,ZT2174549895561843032,ZT2174549896844118233)
- ~~Call side: 230pm~~ (same as IC, don't enter) [backtest](https://app.optionalpha.com/zdte/backtester/compare/ZT217471991373172811742,ZT21747498592713051749,ZT21747498620341614751,ZT21747498633994928752,ZT21747498648258561753)
### Friday
- Put side: 330pm - 345pm, 30delta (sort of same, maybe enter?) [backtest](https://app.optionalpha.com/zdte/backtester/compare/ZT21747495856828561516,ZT21747495838169290515,ZT21747495872420891517,ZT21747495902818135519,ZT21747495928214227521)
- Call side: 330pm, 30-35delta (sort of same also, maybe enter) [backtest](https://app.optionalpha.com/zdte/backtester/compare/ZT21747498756533741757,ZT21747498850675688762,ZT21747498859949184763,ZT21747498890203437764,ZT21747498943336507765)

### High VIX
I found that the put side performs very well in high VIX environments (i.e. VIX > 20).  VIX >25 also performs well, but there is a lot less positions. ([Backtest](https://app.optionalpha.com/zdte/backtester/compare/ZT21747494644820450471,ZT21747494662764665472,ZT21747494956600625481,ZT21747494990143712483))

So, I will enter additional positions on Tuesday/Wednesday/Thursday/Friday at 3pm if VIX>20, and daily EMA>10.



### Summary

Leg into iron condors on Tuesday and Friday based on times above.