---
layout: default
title: "Your Breakeven Stop Is Killing Your Best Trades"
permalink: /stopping-moving-your-stop-to-breakeven/
date: 2026-08-29
---

# Your Breakeven Stop Is Killing Your Best Trades

{% raw %}
Every figure, claim and mechanism the finished picture states, chased to a primary source.
Anything that could not be chased to one is listed under "Not checked" and is deliberately
kept off the screen.

## Stop loss orders can drive fast, self reinforcing moves

The video says that research on currency markets found stop loss orders can contribute to
fast, self reinforcing moves when clustered levels are triggered.

Osler states it in the abstract, in those terms:

> In this paper, I provide evidence that currency stop-loss orders contribute to rapid,
> self-reinforcing price movements, which I call "price cascades."

Three empirical results support it:

1. Exchange rate trends are unusually rapid when rates reach levels at which stop loss
   orders have been documented to cluster.
2. The response to stop loss orders is larger than the response to take profit orders,
   which generate negative feedback trading and are therefore unlikely to contribute to
   price cascades.
3. The response to stop loss orders lasts longer than the response to take profit orders.

Most results are statistically significant for hours, though not for days. Osler notes the
same mechanism may help explain the fat tails of the exchange rate return distribution.

Source: C. L. Osler, "Stop-Loss Orders and Price Cascades in Currency Markets", Federal
Reserve Bank of New York Staff Report No. 150, June 2002.
https://www.newyorkfed.org/medialibrary/media/research/staff_reports/sr150.pdf

Published as: C. L. Osler, "Stop-loss orders and price cascades in currency markets",
Journal of International Money and Finance, 24(2), 2005, pp. 219 to 241.
https://www.sciencedirect.com/science/article/abs/pii/S0261560604001147

## Stop orders cluster at obvious prices

The video says stop orders often cluster around obvious prices, and lists round numbers,
prior highs, prior lows, breakout levels and retest levels as the places traders make
similar decisions.

Osler examined the order book of a large foreign exchange dealing bank covering almost
9,700 stop loss and take profit orders placed between 1 September 1999 and 11 April 2000,
in dollar yen, dollar pound and euro dollar. The distribution of requested execution rates
is far from smooth:

> execution rates tend to cluster, with particularly strong clusters at round numbers

The clustering patterns of the two order types differ, and that difference is the finding:

- Take profit orders cluster more strongly **at** round numbers, which makes those levels
  behave as partially reflecting barriers.
- Stop loss orders cluster **just beyond** round numbers, which is why rates trend strongly
  after crossing one.

The single greatest cluster is at levels ending in 00.

Source: C. L. Osler, "Currency Orders and Exchange-Rate Dynamics: Explaining the Success of
Technical Analysis", Federal Reserve Bank of New York Staff Report No. 125, March 2001.
https://www.newyorkfed.org/medialibrary/media/research/staff_reports/sr125.pdf

Published as: C. L. Osler, "Currency Orders and Exchange Rate Dynamics: An Explanation for
the Predictive Success of Technical Analysis", The Journal of Finance, 58(5), 2003,
pp. 1791 to 1819. https://onlinelibrary.wiley.com/doi/abs/10.1111/1540-6261.00588

Note what this does not say, which the video is careful about too: the clustering is a
property of where many people independently place orders, not evidence that anyone is
hunting a particular account's stop.

## Expectancy, and why the average result is the thing that matters

The video's arithmetic claim is that trading is won by positive expectancy, meaning the
average result across many trades has to be worth taking, and that a rule which reduces
full losses while also reducing large winners can lower that average.

This is a definition rather than an empirical finding. Expectancy is the probability
weighted average outcome per trade, conventionally written as

    (win rate x average win) minus (loss rate x average loss)

so a change that lowers the average win and the loss rate at the same time moves the result
in two directions at once, and the sign of the net move is an empirical question about a
specific strategy rather than something that can be asserted in general. The video treats it
that way: it says the tradeoff has to be measured on your own trades, and the journal test in
the later chapter is how it says to measure it.

The picture therefore draws the shape of the tradeoff, the right tail of the outcome
distribution being clipped while the left tail is trimmed, and prints no percentage.

## Not checked

Two claims in the narration could not be chased to a primary source, so **no figure from
either appears anywhere in the picture**. The shots for those beats draw the mechanism the
words describe and carry no number and no source line.

- A research test of a breakeven rule added to an existing strategy, moving the stop to
  entry once price reached one R in profit, which reduced drawdown and cut the average
  profit per trade by more than a quarter. The general direction of this result is widely
  reported by trading educators and backtesting sites, but no published study, dataset or
  reproducible backtest stating that specific reduction could be located.
- A simulation of a strategy with a three R target in which adding a breakeven move at one
  R dropped full losses, dropped winners, and made the average result per trade fall
  sharply. No underlying study, dataset or reproducible backtest could be located.

Both are consistent with the arithmetic of expectancy above, and neither is presented on
screen as a measured result.
{% endraw %}
