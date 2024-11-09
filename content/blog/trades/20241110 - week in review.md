---
title:  Trump Market - Weekly summary (Nov 4 - Nov 8)
description: Review of trades from past week
date: 2024-11-10
tags:
  - trades
  - weekly
permalink: "/trades-2024-11-10/"
---

Trump won the election, and the market boomed like crazy.

How much more will it go up?  Who knows.

Took a bit of a break from 0DTE trading this week.  Mainly because time zones changed, and screwed up my schedule.

Trying some more small trades on dividend capture, and short put strategies.

## Opened:

<div class="trade-table weekly full-width">

|**Ticker**|**Action**|**Type**|**Date**|**Expiry**|**Sell Strike**|**Buy Strike**|**Premium**|**Qty**|**Fee**|**Net**|
|---|---|---|---|---|---|---|---|---|---|---|
|SPY|open|BCS|2024-11-06|2024-12-20|595|596|0.51|1|1.43|49.57|
|F|open|Long|2024-11-06|-|0|11.038|-11.038|1|1|-1104.8|
|F|open|Covered Call|2024-11-07|2024-11-08|11|0|0.15|1|1.44|13.56|
|SPY|open|BCS|2024-11-07|2024-12-13|599|600|0.51|1|2.13|48.87|
|SLV|open|Short Put|2024-11-07|2024-11-15|28|0|0.21|1|0.57|20.43|
|VIX|open|Long Call|2024-11-07|2024-02-18|0|45|-0.43|1|1.3|-44.3|

</div>

Trying dividend capture strategy with `F` (Ford).  It is only $11 per share, so I am at most risking around $1000.  More on strategy below.

Also, taking short/naked put on `SLV`.  Haven't been doing much naked (or cash/margin secured) puts recently, mainly because my account can't handle it.  `SLV` is only around $30 a share though, so I took a shot.  Low risk, low reward, I suppose.

`VIX` long call is my hedge against some crazy shit happening in the next few months.

## Closed / Expired:

<div class = "trade-table monthly full-width">

|**Ticker**|**Action**|**Type**|**Date**|**Expiry**|**Sell Strike**|**Buy Strike**|**Premium**|**Qty**|**Fee**|**Net**|**Profit/Loss**|
|---|---|---|---|---|---|---|---|---|---|---|---|
|COST|open|BPS|2024-09-17|2024-12-20|795|785|1.43|1|2.15|140.85|$69.44|
|COST|close|BPS|2024-11-06|2024-12-20|785|795|-0.7|1|1.41|-71.41|
|MSFT|open|BPS|2024-09-23|2024-12-20|385|375|1.12|1|2.13|109.87|$58.46|
|MSFT|close|BPS|2024-11-07|2024-12-20|375|385|-0.5|1|1.41|-51.41|
|IYR|open|BPS (IC)|2024-10-01|2024-11-15|98|97|0.22|1|1.42|20.58|-$14.52|
|IYR|close|BPS (IC)|2024-11-08|2024-11-15|97|98|-0.33|1|2.1|-35.1|
|IYR|open|BCS (IC)|2024-10-01|2024-11-15|104|105|0.35|1|1.42|33.58|$34.47|
|IYR|close|BCS (IC)|2024-11-08|2024-11-15|105|104|0.03|1|2.11|0.89|
|VXX|open|BCS|2024-10-02|2024-11-15|50|52|0.76|1|1.44|74.56|$39.45|
|VXX|close|BCS|2024-11-06|2024-11-15|52|50|-0.33|1|2.11|-35.11|
|XSP|open|BCS|2024-10-04|2024-11-08|579|580|0.52|1|1.52|50.48|-$49.52|
|XSP|expired|BCS|2024-11-08|2024-11-08|580|579|-1|1|0|-100|
|XSP|open|BCS|2024-10-07|2024-11-08|581|582|0.5|1|1.52|48.48|-$51.52|
|XSP|assigned/exercised|BCS|2024-11-08|2024-11-08|582|581|-1|1|0|-100|
|MSFT|open|BPS|2024-10-14|2024-01-17|380|370|1.4|1|1.42|138.58|$66.97|
|MSFT|close|BPS|2024-11-07|2024-01-17|370|380|-0.7|1|1.61|-71.61|
|TLT|open|BCS (IC)|2024-10-14|2024-11-22|95|96|0.36|1|2.11|33.89|$20.79|
|TLT|close|BCS (IC)|2024-11-08|2024-11-22|96|95|-0.11|1|2.1|-13.1|
|TLT|open|BPS (IC)|2024-10-14|2024-11-22|90|89|0.19|1|2.11|16.89|$0.79|
|TLT|close|BPS (IC)|2024-11-08|2024-11-22|89|90|-0.14|1|2.1|-16.1|
|SPY|open|BCS|2024-10-17|2024-11-29|591|592|0.530000000000001|1|1.43|51.5700000000001|$24.66|
|SPY|close|BCS|2024-11-05|2024-11-29|592|591|-0.25|1|1.91|-26.91|
|BITO|open|Long|2024-10-31|-|0|20|-20|1|1|-2001|-$1,902.00|
|BITO|dividend|Long|2024-11-01|-|0|0|0.99|1|0|99|
|BITO|open|Covered Call|2024-11-01|2024-11-08|20|0|0.47|1|1.05|45.95|$2,045.95|
|BITO|assigned|Covered Call|2024-11-08|2024-11-08|0|0|20|1|0|2000|
|SPX|open|BCS|2024-11-04|2024-11-04|5745|5785|1|1|3.19|96.81|$96.81|
|SPX|expired|BCS|2024-11-04|2024-11-04|5785|5745|0|1|0|0|
|SPX|open|BCS|2024-11-04|2024-11-04|5740|5765|1|1|3.19|96.81|-$106.38|
|SPX|close|BCS|2024-11-04|2024-11-04|5765|5740|-2|1|3.19|-203.19|

</div>

- **Closed Net Profits/Loss**: $333.85


## Notes and Lessons

The huge market upswing after the US election helped me close a bunch of positions. 

Thanks Trump?  I guess.

It also pushed a bunch of my remaining bear positions into losers.  Thanks Trump.

In any case, it was my first decent profitable week in a while.

### Dividend capture
Closed my first profitable trade using dividend capture strategy on `BITO`.  It has a huge dividend, and I got lucky again with bitcoin price spiking after Trump election.  

Trying strategy again on a very small trade with `F`.  

Basically, I buy 100 shares of the stock a day before ex-dividend.  Hold the shares for 1 day, then sell a call at the same price I bought the shares at.  Choose the closest expiry I can (usually 1-2 weeks or less)

If the stock stays at the same level or goes up a bit, then I will get assigned and keep the dividend as well as the premium.

If the stock goes down a bit, then I keep selling calls at my purchase price, until it rebounds.  Each time I sell a call, it lowers my overall costs.

If the stock goes down A LOT, and there doesn't seem hope for recovery, then I'm fucked and I should probably just sell position for a loss.  I need to decide on an amount...like 10%? Not sure yet.

Choosing a stable company or one where price is flat or uptrending is important for this strategy.  Also, avoid earnings or any other major news.  

ETFs are probably better than individual stocks, but there are not many low priced ETFs with good option volume (and dividend payment).