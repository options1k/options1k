---
title: Naked Put Strategy
description: Option Selling Strategy 4
date: 2023-08-21
tags:
  - strategy
  - active
permalink: "/naked-put-strategy/"
draft: false
---

This is a naked put selling strategy that I have pieced together from <a href="https://www.passiveseeds.com">Gin Lim</a>, <a href="https://great-option-trading-strategies.com/">Brad Castro</a>, and [Options with Davis](https://www.youtube.com/@optionswithdavis).

## Basic overview
Sell puts on *profitable, high quality* companies that I would like to own in the long term.

May consider also combining with put debit spread to create a put ratio spread.  [Note](https://www.youtube.com/watch?v=kNr5QoKhOtc)

## Detailed Overview
Can trade this on either index ETFs, or individual stocks:

### Company / stock selection

1. Stable index ETF

OR, if individual stock:

1. Profitable (Net Margin > 15%)
2. Earnings & Revenue growth over past 5 years (and forseeable future)
3. Manageable debt levels (i.e. low D/E ratio, or great interest coverage)
4. Return on Equity > 15%
5. Good cash flow / quality of earnings
6. High option volume (preferably with weekly options available)

### Entry rules
1. Sell put at calculated target entry price (i.e. fundamentally attractive price that I want to own the stock at). 
2. Collected premium should give annualized return > 15% (e.g. put option with 30DTE should have at least 1.25% return)


### Exit options
There are a few exit options/outcomes for naked puts:

1. **Option expires worthless**
- If stock price never goes below strike, then just let short put expire, and collect premium.  Sell again.

2. **Close position early** 
- If stock price jumps up significantly in a short time, it will probably be worth it to close position early (based on annualized return). You could also just let it run to expiry.

3. **Assigned** 
- If stock price drops below put strike and shares are assigned, it is not a bad thing, because it is a company that I want to own for long term.  
- If something has changed in the company though that has fundamentally reduced target price, then I should think about selling for a loss.
- Otherwise, start selling call options on newly owned shares at assigned price or higher (target exit price).  Aim for at least premium that makes 5% annualized cash flow.  Commonly known as the "Wheel Strategy".
- Sell all shares at calculated target exit price

### Allocation / Risk amount
Controlling amount of risk is maybe the most important part of selling naked puts.

I am going to start conservative and limit myself to around $5,000 - $6,000 of *cash* risk, preferably less.

That means I can only sell ***one*** put option on a stock with $50 - $60 price. (i.e. 100 shares x $50 = $5000).

### Splitting up risk

Will also be looking at implementing the ["Income Grid" strategy](https://www.youtube.com/watch?v=c9RbaekCPt4), which I learned from Options with Davis Youtube.

Basically, split your capital up into a few parts, and sell puts at different price levels over time.  This way, if the stock tanks, you aren't caught with all the shares at one price level (this has happened to me many times before).

For example, if you have $10k, split it up into a 3-4 different levels.  

So, if a stock is $50/share, sell a put at $40 level.  If the stock tanks under $40 and you get assigned (-$4000), then you sell another put at $35.  If it continues tanking and you get assigned again (-$3500), sell another put at $25.  

If it continues tanking, then you get assigned again (-$2500) and have used all your capital.  If it tanks even more, then you're probably screwed.

That's why it's important to choose a solid company (or ETF), as it *should* eventually return (there's always a risk it won't).  While waiting for the price to return, you can sell covered calls at the different levels to get income.

Sounds very good in theory, but does it work in real life?  Guess we'll find out.

### Worst Case Scenario
The worst case scenario, is the stock you get assigend on goes to $0 (or close to 0), and lose everything.

To limit this risk, I will stick to ETFs and very large cap companies. 

The company could still go to $0 though, which is why I will limit myself to stocks that are around $50/share.  

## Summary / Notes
Selling naked puts is how I blew up my account in 2022.  

Mainly, I was way overleveraged (basically maxed out my margin), and was playing with some super volatile companies.  I didn't really understand what I was doing, but was making money so kept going.

When the market started tanking, I got caught with my pants down.

I've learned a lot since then, so hopefully can do a bit better this time. Hopefully. 🙃
