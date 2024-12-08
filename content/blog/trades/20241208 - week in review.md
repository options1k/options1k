---
title:  Good start to the month - Weekly summary (Dec 2 - Dec 6)
description: Review of trades from past week
date: 2024-12-06
tags:
  - trades
  - weekly
permalink: "/trades-2024-12-02/"
---

Was a a good first week to the last month of the year.

Was also my first week automating 0dte trades, and it luckily worked out in my favor.

Here are the trades from last week:

## Opened:

<div class="trade-table weekly full-width">

|**Ticker**|**Action**|**Type**|**Date**|**Expiry**|**Sell Strike**|**Buy Strike**|**Premium**|**Qty**|**Fee**|**Net**|
|---|---|---|---|---|---|---|---|---|---|---|
|KHC|open|Covered Call|2024-12-02|2024-12-06|32|0|0.11|1|0.57|10.43|$10.43|
|EEM|open|Covered Call|2024-12-02|2024-12-06|43.5|0|0.18|1|0.8|17.2|$4,367.20|
|SLV|open|Covered Call|2024-12-02|2024-12-06|28|0|0.26|1|0.74|25.26|$2,825.26|
|SPY|open|BCS|2024-12-02|2024-01-10|607|608|0.5|1|2.12|47.88|$47.88|
|QQQ|open|BCS|2024-12-02|2024-01-10|519|520|0.52|1|1.41|50.59|$50.59|
|SPY|open|BCS|2024-12-03|2024-01-17|576|571|0.42|1|2.09|39.91|$39.91|
|SPY|open|BCS|2024-12-04|2024-01-10|610|611|0.52|1|1.41|50.59|$50.59|
|PFE|open|Short Put|2024-12-05|2024-12-13|25|0|0.17|1|0.63|16.37|$16.37|
|V|open|BPS|2024-12-06|2024-03-21|280|270|0.95|1|2.31|92.69|$91.27|
|CSCO|open|Covered Call|2024-12-06|2024-12-13|60|0|0.49|1|0.7|48.3|$48.30|

</div>

A bunch of covered calls, and few mathematical trade ideas.  Rolled the covered call on `CSCO` out one more week, as it was right near the strike price at expiry.

Also started testing a 45-DTE trade on `SPY`.  According to many sources, this seems to be the optimal trade to make.  The premium seems a bit small, but we'll see how it goes.

Bit of risky short put on `PFE`.  The stock has been absolutely pummelled over the past couple years after COVID panic died down.  It could continue going to 0, but it is still a profitable company, is currently undervalued, and has a history of overcoming drawdowns.


## Closed / Expired:

<div class = "trade-table monthly full-width">

|**Ticker**|**Action**|**Type**|**Date**|**Expiry**|**Sell Strike**|**Buy Strike**|**Premium**|**Qty**|**Fee**|**Net**|**Profit/Loss**|
|---|---|---|---|---|---|---|---|---|---|---|---|
|IWM|open|BPS (IC)|2024-10-25|2024-12-06|210|209|0.22|1|1.42|20.58|$20.58|
|IWM|expired|BPS (IC)|2024-12-06|2024-12-06|209|210||1||0|
|IWM|open|BCS (IC)|2024-10-25|2024-12-06|227|228|0.35|1|1.41|33.59|-$66.41|
|IWM|assigned/exercised|BCS (IC)|2024-12-06|2024-12-06|228|227|-1|1|0|-100|
|SPY|open|BCS|2024-10-30|2024-12-06|590|591|0.52|1|2.13|49.87|-$50.13|
|SPY|close|BCS|2024-12-06|2024-12-06|591|590|-1|1|0|-100|
|SLV|open|Short Put|2024-11-07|2024-11-15|28|0|0.21|1|0.57|20.43|-$2,779.57|
|SLV|assigned|Short Put|2024-12-06|2024-11-15|0|28|-28|1|0|-2800|
|EEM|open|Short Put|2024-11-13|2024-11-15|43|0|0.18|1|1.04|16.96|-$4,283.04|
|EEM|assigned|Short Put|2024-12-06|2024-11-15|0|43|-43|1|0|-4300|
|EEM|open|Covered Call|2024-11-18|2024-11-22|43.5|0|0.26|1|1.06|24.94|$24.94|
|EEM|expired|Covered Call|2024-12-06|2024-11-22|0|43.5||1|0|0|
|SLV|open|Covered Call|2024-11-18|2024-11-22|29|0|0.19|1|0.57|18.43|$18.43|
|SLV|expired|Covered Call|2024-12-06|2024-11-22|0|29|0|1|0|0|
|MSFT|open|BPS|2024-11-19|2024-02-21|370|355|1.55|1|2|153|$81.61|
|MSFT|close|BPS|2024-12-04|2024-02-21|355|370|-0.7|1|1.39|-71.39|
|EEM|open|Covered Call|2024-11-25|2024-11-29|43.5|0|0.2|1|1.06|18.94|$18.94|
|EEM|expired|Covered Call|2024-12-06|2024-11-29|0|43.5|0|1|0|0|
|SLV|open|Covered Call|2024-11-25|2024-11-29|28|0|0.15|1|1.05|13.95|$13.95|
|SLV|expired|Covered Call|2024-12-06|2024-11-29|0|28|0|1|0|0|
|EEM|open|Covered Call|2024-12-02|2024-12-06|43.5|0|0.18|1|0.8|17.2|$4,367.20|
|EEM|assigned|Covered Call|2024-12-06|2024-12-06|43.5|0|43.5|1|0|4350|
|SLV|open|Covered Call|2024-12-02|2024-12-06|28|0|0.26|1|0.74|25.26|$2,825.26|
|SLV|assigned|Covered Call|2024-12-06|2024-12-06|28|0|28|1|0|2800|

</div>

- **Closed Net Profits/Loss**: $191.76

Couple of my short puts turned covered calls positions (i.e. 'wheel strategy') closed for decent profits -- `SLV`, `EEM`.  

Maybe was too conservative with the sell call strikes, but I currently have a larger-than-wanted negative cash balance in my account right now, so trying to reduce that.

Rest of my profits came from 0DTE:

## 0DTE Trades

First full week using automation software [Trade Automation Toolbox](https://tradeautomationtoolbox.com/).  

Was a bit nervous something stupid would happen, but it worked out in the end.

Got a bit lucky on the last day I think with a trade 15 minutes before close. 

<div class = "trade-table monthly full-width">

|**Ticker**|**Action**|**Type**|**Date**|**Expiry**|**Sell Strike**|**Buy Strike**|**Premium**|**Qty**|**Fee**|**Net**|**Profit/Loss**|
|---|---|---|---|---|---|---|---|---|---|---|---|
|SPX|open|BPS|2024-12-02|2024-12-02|6035|5995|1.1|1|3.19|106.81|$106.81|
|SPX|close|BPS|2024-12-02|2024-12-02|5995|6035|0|1|0|0|
|SPX|open|BCS|2024-12-02|2024-12-02|6050|6075|0.95|1|3.19|91.81|-$109.83|
|SPX|close|BCS|2024-12-02|2024-12-02|6075|6050|-2|1|1.64|-201.64|
|SPX|open|BCS|2024-12-03|2024-12-03|6055|6100|1.05|1|3.19|101.81|$101.81|
|SPX|close|BCS|2024-12-03|2024-12-03|6100|6055|0|1|0|0|
|SPX|open|BPS|2024-12-03|2024-12-03|6035|6000|0.9|1|3.19|86.81|$86.81|
|SPX|close|BPS|2024-12-03|2024-12-03|6000|6035|0|1|0|0|
|SPX|open|BCS|2024-12-03|2024-12-03|6050|6085|0.9|1|3.19|86.81|-$99.83|
|SPX|close|BCS|2024-12-03|2024-12-03|6085|6050|-1.85|1|1.64|-186.64|
|SPX|open|BPS|2024-12-06|2024-12-06|6075|6035|1.1|1|3.19|106.81|-$151.38|
|SPX|close|BPS|2024-12-06|2024-12-06|6035|6075|-2.55|1|3.19|-258.19|
|SPX|open|BCS|2024-12-06|2024-12-06|6100|6125|1.05|1|3.19|101.81|$101.81|
|SPX|close|BCS|2024-12-06|2024-12-06|6125|6100|0|1|0|0|
|SPX|open|BCS|2024-12-06|2024-12-06|6085|6070|1.05|1|3.19|101.81|$101.81|
|SPX|close|BCS|2024-12-06|2024-12-06|6070|6085|0|1|0|0|

</div>

- **0DTE Closed Net Profits/Loss**: $138.01

Pretty bad slippage on one of the stops -- loss should've been around $120, but ended up at $150.  Other than that, everything went pretty much as it should've.

- **TOTAL WEEKLY NET PROFITS/LOSS**: $329.77


## Notes and Lessons

Overall, was a good week for me.  

My 0DTE trades made money, and all my other strategies made money too.

The market also continued pushing new all-time highs.

Why can't every week be like this?

Currently, I do have one position that I'm a bit weary about with -- `KHC`.  It was a dividend capture play from last week.  It unfortunately dropped a bit too much after, and it is reaching a point where selling calls at my purchase price is becoming worthless.  

Need to decide at what price I should cut it off and take the loss.  Should I put a stop loss on the stock?  Or just play it by ear.  Will see how it goes next week.

Have also been reducing positions on my `MSFT` strategy.  Originally, I was allocating $5k risk to it, but now I think that it's a bit much, so am going to scale it back to $1-$2k.




