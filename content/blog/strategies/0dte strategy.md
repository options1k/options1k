---
title: 0DTE Strategies
description: Strategy 7
date: 2025-01-27
updated: 2025-11-17
tags:
  - strategy
  - active
permalink: "/0dte-strategy/"

---

On this page is a collection of 0DTE strategies I currently use.  

- [SPX METF](#spx-metf-strategy)
- [$5 Iron Condor Strategy on SPX](#spx-5-iron-condor-strategy)
- [Hybrid Iron Condor on SPX](#hybrid-ic-strategy-spx)
- [ORB](#orb)

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
- **Entry time:** 9:40am ([backtest](https://app.optionalpha.com/zdte/backtester/compare/ZT217621735083639191238,ZT217621735656900801240,ZT217474737703108341847,ZT217474737960967671848,ZT217474738365520371850))
- **Delta:** 25 - 35 (25 is better - [backtest](https://app.optionalpha.com/zdte/backtester/compare/ZT21756656679071427279,ZT21756656722239838288,ZT21756656773486275290,ZT21756656892673924294,ZT21756657656210285319)) 
- **Notes:**  
  - 1:45pm, 25delta has similar results
  - 9:40am exactly has best results [backtest](https://app.optionalpha.com/zdte/backtester/compare/ZT21756656679071427279,ZT21756657008012684298,ZT21756657343592485303,ZT21756657808043656334,ZT21756657845840949338)
- **Results:** Profit: 5277; max drawdown 1517; profit factor 1.42

### Tuesday
- **Entry time:** 11:25am (11:15-11:30am all good)([backtest](https://app.optionalpha.com/zdte/backtester/compare/ZT217474746360380341874,ZT217474746644283151875,ZT217474747104471771876,ZT217474747389971861878,ZT217474747540383561879))
- **Delta:** 20 (15-35 all decent: [backtest](https://app.optionalpha.com/zdte/backtester/compare/ZT217543771766695351953,ZT217543772066218101954,ZT217543772383365051956,ZT217543773049922811957,ZT21756738591668549210), 25-30 better over past year) 
- **Notes:**  
  - 1:45pm also solid return, similar return over [past year](https://app.optionalpha.com/zdte/backtester/compare/ZT21756737839112788179,ZT21756738263780798195). 
 - [VIX backtest](https://app.optionalpha.com/zdte/backtester/compare/ZT217543773049922811957,ZT21756738979431574220,ZT21756739003471908222,ZT21756739051736774223,ZT21756739094718076224)
- **Results:** Profit: $7500; max drawdown 1210; profit factor 1.74

### Wednesday
- **Entry time:** 12:05pm([backtest](https://app.optionalpha.com/zdte/backtester/compare/ZT2175681487961416120,ZT2175681488894395822,ZT2175681490044391925,ZT2175681491040640726,ZT2175681491862347327))
- **Delta:** 30-40 ([backtest](https://app.optionalpha.com/zdte/backtester/compare/ZT217677739640999841541,ZT217677740136224031542,ZT217677740792212171545,ZT217677744306256461552,ZT217677744812327531553))
- **Notes:**  
  - bumpy results, but good over past 6 months, didn't trade it when I should've 
- **Results:** Profit: 3311; max drawdown 2512; profit factor 1.22

### Thursday
- **Entry time:** Don't trade; negative returns over past year ([backtest](https://app.optionalpha.com/zdte/backtester/compare/ZT217677764462060621586,ZT217677764378021941585,ZT217677764289335981584,ZT217677765543397741589,ZT217677764591817761587))
- **Delta:** n/a
- **Notes:**  Was OK until 2025, then has been straight downhill.
- **Results:** 

### Friday
- **Entry time:** 3:05pm-3:20pm ([backtest](https://app.optionalpha.com/zdte/backtester/compare/ZT217474794092906171954,ZT217474794219033721955,ZT217474794362378181956,ZT217474794460919001958,ZT217474794594404621959))[Backtest](https://app.optionalpha.com/zdte/backtester/compare/ZT217654393231590261148,ZT217654393476020581149,ZT217654393648516361150,ZT217654393818667811151,ZT217654395704562801152)
- **Delta:** 30-35 (15-35 delta all profitable, best return around 30-35 range  - [backtest](https://app.optionalpha.com/zdte/backtester/compare/ZT217654387168178991135,ZT217654387753023711136,ZT217654388959812761140,ZT217654389344535731143,ZT217654390028117751145) )
- **Notes:**  Friday has been the most consistent and most profitable day.  Main problem is that it is more difficult to get an entry later in the day (after 3pm). Can mitigate this by targeting larger delta ranges (15-40?)..  may think about increasing position/size on Fridays.
- **Results:** Profit: 8900; max drawdown 700; profit factor 1.9

### Summary / Other Notes

Overall, the strategy was going well in 2025, but has been negative/flat after June 2025.  Will continue testing and reducing entries until things start looking up again.

### VIX

Strategy performs worse in low VIX (<15) environments.  May consider not trading it when VIX is low.

Here is backtest of baseline strategy with VIX comparisons: [Backtest](https://app.optionalpha.com/zdte/backtester/compare/ZT21756655562386687232,ZT21756655702926506235,ZT21756655749408994236,ZT21756655782363812239,ZT21756655954079356246)
- green line is VIX < 15
- 
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

## ORB

ORB stands for "Opening Range Breakout", and is a common strategy among 0DTE traders.  

Basically, you look at the highest and lowest price of a certain period after market opens.  For example, a 60 minute ORB would look at the highest and lowest price during the first hour of the market.

If the price breaks through one of the extremes, then you make a trade.  