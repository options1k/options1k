---
title:  0DTE Win, but Trade Ideas fail - Weekly summary (Oct 14 - Oct 18)
description: Review of trades from past week
date: 2024-10-20
tags:
  - trades
  - weekly
permalink: "/trades-2024-10-14/"
---

Great week for my 0DTE trades.  

Made up for the big loss last week.

Unfortunately, basically all my other trades lost money, mainly a ton of ["trade ideas"](/options-alpha-strategy/) taken from Option Alpha platform.

Thinking of stopping those trades for awhile, the losses have been piling up.  Perhaps the platform's "probabiliity" calculation is not very good.

Here are trades from last week:

## Opened:


<div class="trade-table weekly full-width">

|**Ticker**|**Action**|**Type**|**Date**|**Expiry**|**Sell Strike**|**Buy Strike**|**Premium**|**Qty**|**Fee**|**Net**|
|---|---|---|---|---|---|---|---|---|---|---|
|MSFT|open|BPS|2024-10-14|2024-01-17|380|370|1.4|1|1.42|138.58|
|TLT|open|BCS (IC)|2024-10-14|2024-11-22|95|96|0.36|1|2.11|33.89|
|TLT|open|BPS (IC)|2024-10-14|2024-11-22|90|89|0.19|1|2.11|16.89|
|SPY|open|BCS|2024-10-14|2024-11-22|591|592|0.51|1|1.43|49.57|
|SPY|open|BCS (IC)|2024-10-15|2024-10-25|594|597|0.38|1|3.09|34.91|
|SPY|open|BPS (IC)|2024-10-15|2024-10-25|567|564|0.22|1|3.09|18.91|
|SPY|open|BCS|2024-10-15|2024-11-15|589|590|0.5|1|3.11|46.89|
|SPY|open|BCS|2024-10-17|2024-11-29|591|592|0.530000000000001|1|1.43|51.5700000000001|
|XLP|open|BCS|2024-10-18|2024-12-20|83|84|0.5|1|1.41|48.59|

</div>

Decided to open an iron condor for my weekly `SPY` trade.  Not sure why, maybe to make up for forgetting to trade it last week.  

After some more research though, seems like I may abandon my original `SPY` strategy, or at least change how I trade it.

Opened new `MSFT` position and few trades form Option Alpha "trade ideas".  As mentioned, may also abandon "trade ideas" strategy soon as it has been losing a lot.

## Closed / Expired:

<div class = "trade-table monthly full-width">

|**Ticker**|**Action**|**Type**|**Date**|**Expiry**|**Sell Strike**|**Buy Strike**|**Premium**|**Qty**|**Fee**|**Net**|**Profit/Loss**|
|---|---|---|---|---|---|---|---|---|---|---|---|
|MSFT|open|BPS|2024-07-09|2024-10-18|410|395|1.63|1|2.11|160.89|$79.48|
|MSFT|close|BPS|2024-10-14|2024-10-18|395|410|-0.8|1|1.41|-81.41|
|GLD|open|BCS (IC)|2024-09-03|2024-10-18|243|246|0.41|1|1.4|39.6|-$260.40|
|GLD|assigned/exercised|BCS (IC)|2024-10-18|2024-10-18|246|243|-3|1|0|-300|
|GLD|open|BPS (IC)|2024-09-03|2024-10-18|221|218|0.48|1|1.4|46.6|$46.60|
|GLD|expired|BPS (IC)|2024-10-18|2024-10-18|218|221|0|1|0|0|
|SPY|open|BCS|2024-09-03|2024-10-18|560|562|1.12|1|1.43|110.57|-$89.43|
|SPY|assigned/exercised|BCS|2024-10-18|2024-10-18|562|560|-2|1|0|-200|
|SPY|open|BCS|2024-09-06|2024-10-18|552|553|0.5|1|2.13|47.87|-$52.13|
|SPY|assigned/exercised|BCS|2024-10-18|2024-10-18|553|552|-1|1|0|-100|
|XSP|open|BCS|2024-09-11|2024-10-18|550|551|0.49|1|1.86|47.14|-$52.86|
|XSP|assigned/exercised|BCS|2024-10-18|2024-10-18|551|550|-1|1|0|-100|
|XSP|open|BCS|2024-09-13|2024-10-18|565|566|0.569999999999999|1|1.86|55.1399999999999|-$44.86|
|XSP|assigned/exercised|BCS|2024-10-18|2024-10-18|566|565|-1|1|0|-100|
|XSP|open|BCS|2024-09-17|2024-10-18|575|576|0.54|1|1.86|52.14|-$47.86|
|XSP|assigned/exercised|BCS|2024-10-18|2024-10-18|576|575|-1|1|0|-100|
|BITO|open|Short Put|2024-10-01|2024-10-18|16|0|0.17|1|1.05|15.95|$15.95|
|BITO|expired|Short Put|2024-10-18|2024-10-18|0|16|0|1|0|0|


</div>

- **Closed Net Profits/Loss**: -$405.51

Shitload of failed trade ideas. Lost over $500 from them this week.

I have been mainly targetting a 50-60% "probability of max profit", but so far I'm more at like 20% probability right now. 

These trade ideas have been responsible for nearly $700 of losses this month so far.  Might be time to pull the plug on this strategy.


## 0DTE Trades:

This week, I traded the "METF" 0DTE strategy (i.e. multiple entry trend following strategy), which I first came across on the [Theta Profits blog](https://www.thetaprofits.com/how-to-trade-the-metf-0dte-options-strategy/). Also called the 0DTE EMA strategy.

Traded every day, except Friday.  I did a backtest using [byob](https://tradeautomationtoolbox.com/byob-ticks/), which showed that trading on Fridays this year had negative returns.

Everything worked out well:

<div class = "trade-table monthly full-width">

|**Ticker**|**Action**|**Type**|**Date**|**Expiry**|**Sell Strike**|**Buy Strike**|**Premium**|**Qty**|**Fee**|**Net**|**Profit/Loss**|
|---|---|---|---|---|---|---|---|---|---|---|---|
|SPX|open|BPS|2024-10-14|2024-10-14|5840|5765|1|1|3.21|96.79|$96.79|
|SPX|expired|BPS|2024-10-14|2024-10-14|5765|5840|0|1|0|0|
|SPX|open|BCS|2024-10-14|2024-10-14|5865|5890|1|1|3.21|96.79|-$129.86|
|SPX|close|BCS|2024-10-14|2024-10-14|5890|5865|-2.25|1|1.65|-226.65|
|SPX|open|BPS|2024-10-14|2024-10-14|5850|5820|1.05|1|3.21|101.79|$101.79|
|SPX|expired|BPS|2024-10-14|2024-10-14|5820|5850|0|1|0|0|
|SPX|open|BCS|2024-10-15|2024-10-15|5855|5880|1.05|1|3.21|101.79|$101.79|
|SPX|expired|BCS|2024-10-15|2024-10-15|5880|5855|0|1|0|0|
|SPX|open|BCS|2024-10-15|2024-10-15|5845|5865|1|1|3.21|96.79|$96.79|
|SPX|expired|BCS|2024-10-15|2024-10-15|5865|5845|0|1|0|0|
|SPX|open|BCS|2024-10-15|2024-10-15|5850|5875|0.55|1|3.12|51.88|$51.88|
|SPX|expired|BCS|2024-10-15|2024-10-15|5875|5850|0|1|0|0|
|SPX|open|BPS|2024-10-16|2024-10-16|5810|5780|1.1|1|3.21|106.79|$106.79|
|SPX|expired|BPS|2024-10-16|2024-10-16|5780|5810|0|1|0|0|
|SPX|open|BPS|2024-10-16|2024-10-16|5820|5770|0.9|1|3.21|86.79|$86.79|
|SPX|expired|BPS|2024-10-16|2024-10-16|5770|5820|0|1|0|0|
|SPX|open|BPS|2024-10-17|2024-10-17|5840|5785|0.95|1|3.21|91.79|-$146.42|
|SPX|close|BPS|2024-10-17|2024-10-17|5785|5840|-2.35|1|3.21|-238.21|
|SPX|open|BCS|2024-10-17|2024-10-17|5875|5900|0.95|1|3.21|91.79|$91.79|
|SPX|expired|BCS|2024-10-17|2024-10-17|5900|5875|0|1|0|0|
|SPX|open|BCS|2024-10-17|2024-10-17|5870|5895|0.95|1|3.21|91.79|$91.79|
|SPX|expired|BCS|2024-10-17|2024-10-17|5895|5870|0|1|0|0|


</div>

- **0DTE Closed Net Profits/Loss**: $549.92

- **TOTAL WEEKLY NET PROFITS/LOSS**: $144.41


## Notes and Lessons

0DTE salvaged my week.

It killed me last week.

I have very volatile feelings about it so far.  

This week, I traded the 0DTE "METF" strategy (multiple entry trend following).  I think it is better for my smaller account size compared to MEIC (multiple entry iron condor) strategy.  I ran a bunch of backtests using the awesome [BYOB 0DTE backtester](https://tradeautomationtoolbox.com/byob-ticks/).  It has had pretty consistent returns over the past 5 years, which I like.

Will give it some more time to see how it goes.

### Trade Ideas fail

Have been making a ton of trades recently using [Option Alpha's](https://optionalpha.com/) trade ideas.  

I am mainly targetting a 50-60% probability of max profit, with 100% return on risk.  Mathematically, every trade I make should have a positive edge.

Since settling on a percentage/risk target, I have closed around 50 trades.  Only around 15 of them have been profitable, which is well below the expected value.

Of course, 50 trades is probably not enough, and perhaps I need to trust the "law or large numbers" concept a bit more.

Will give it some more time, and review again around 100 closed trades?

Also, I should probably space out my expirations a bit more, so not so many positions close on the same week.  Perhaps, only have 2-3 positions at the same DTE.

### New / adjusted strategies
Since I dropped my original options strategy last week, and will also maybe drop Option Alpha trade ideas strategy, I am looking for some new strategies to add.

First, not really a new strategy, but I am looking at trading more short puts, so that I can play the "wheel" strategy if assigned.  I am limited to lower priced ETFs/stocks though (i.e. $50 and under), as my margin will be more affected

Also, looking at implementing some sort of monthly credit spreads or iron condor on the main index ETFs (`SPY`, `QQQ`, `IWM`, etc.), and maybe some commodity ETFS (`GLD`, etc.). Have been reading/watching a lot of stuff on iron condors recently, so will probably start testing some ideas out soon.  Probably going for 45 DTE, 15-20 delta, with 50% profit take, and/or exit/roll at 21DTE.  Need to hash out the details a bit more.

I also want to try some dividend capture strategy combined with ITM (in the money) short calls.  I tried a couple times over the past few weeks, but got assigned before I could collect dividend.  So, I either need to hold the stocks/ETFS for longer before selling the call, or sell the call with further out DTE.

Lastly, I am thinking of adjusting or ending my weekly (10 DTE) SPY strategy.  It has been super profitable actually, but I think I was just lucky to trade it with the huge bull market run we've had over the past year or so.
Now that I understand a bit more about, the backtest results I originally did were not actually very good.  Need to think about it more.

Gonna be a busy week.