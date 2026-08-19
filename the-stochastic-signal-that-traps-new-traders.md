---
layout: default
title: "The Stochastic Signal That Traps New Traders Often"
permalink: /the-stochastic-signal-that-traps-new-traders/
date: 2026-08-19
---

# The Stochastic Signal That Traps New Traders Often

{% raw %}
Every figure, name, date and setting the finished video puts on screen, chased to a source.

## What the stochastic oscillator measures

The oscillator reports where the close sits inside the high to low range of a lookback
window, expressed as a percentage of that range. It is not a reading of how high or low
price is in absolute terms.

> %K = (Current Close - Lowest Low) / (Highest High - Lowest Low) * 100

> %D = 3-day SMA of %K

Zero is the bottom of the window and one hundred is the top.

- StockCharts ChartSchool, Stochastic Oscillator (Fast, Slow, and Full):
  https://chartschool.stockcharts.com/table-of-contents/technical-indicators-and-overlays/technical-indicators/stochastic-oscillator-fast-slow-and-full
- Wikipedia, Stochastic oscillator, which gives the same formula and describes the reading as
  "the point of a current price in relation to its price range over a period of time",
  expressed "as a percentage of this range with 0% indicating the bottom of the range and
  100% indicating the upper limits":
  https://en.wikipedia.org/wiki/Stochastic_oscillator

## %K and %D

%K is the faster line and %D is the slower one, and %D is a moving average of %K rather
than a separate measurement. On the standard setting %D is a three period simple moving
average of %K.

- StockCharts ChartSchool, as above: "%D = 3-day SMA of %K".

## The 14, 3, 3 default, and the 80 and 20 levels

TradingView's Stochastic ships with %K Length 14, %K Smoothing 3 and %D Smoothing 3, and
with the overbought line at 80 and the oversold line at 20. StockCharts documents the same
trio as the default parameters of the Full Stochastic Oscillator, and the same two
thresholds.

The 14 is the lookback: a 14 period %K uses the most recent close, the highest high of the
last 14 periods and the lowest low of the last 14 periods.

- TradingView, Stochastic (STOCH), the indicator's own documentation, which gives %K Length
  14, %K Smoothing 3, %D Smoothing 3, overbought 80 and oversold 20:
  https://www.tradingview.com/support/solutions/43000502332-stochastic-stoch/
- StockCharts ChartSchool, as above: the Full Stochastic Oscillator's default parameters are
  (14,3,3), and the traditional thresholds are 80 and 20.

## Overbought does not mean price has to fall

This is the video's central claim and it is stated outright by the reference documentation.

> Overbought readings aren't necessarily bearish. Securities can become overbought and
> remain overbought during a strong uptrend. Closing levels that are consistently near the
> top of the range indicate sustained buying pressure.

- StockCharts ChartSchool, as above.

The same source records George Lane's own description of what the indicator follows:

> It follows the speed or the momentum of price. As a rule, the momentum changes direction
> before price.

- StockCharts ChartSchool, as above.

## George Lane, and the late 1950s

Lane, 1921 to 2004, worked at Investment Educators in Illinois and was part of a group of
Chicago futures traders who developed the oscillator. He is credited with popularising it,
which is the claim the video makes, rather than with sole authorship: the roles of Lane and
C. Ralph Dystant in its origin are a documented and long running debate, and the earliest
written articulation of the %K and %D oscillator dates to 1957.

- Wikipedia, George Lane (technical analyst): "He was part of a group of futures traders in
  Chicago who developed the stochastic oscillator" and "He popularized the stochastic
  oscillator": https://en.wikipedia.org/wiki/George_Lane_(technical_analyst)
- Wikipedia, Stochastic oscillator: "George Lane developed this indicator in the late
  1950s": https://en.wikipedia.org/wiki/Stochastic_oscillator
- CMT Association, Technically Speaking, May 2011, on the Dystant and Lane attribution
  question and the 1957 date:
  https://cmtassociation.org/technically_speaking/technically-speaking-may-2011/

## Divergence

Bullish divergence is price making a lower low while the oscillator makes a higher low;
bearish divergence is price making a higher high while the oscillator makes a lower high.
Both describe momentum, and neither is by itself a statement that direction has changed,
which is the distinction the video turns on.

- StockCharts ChartSchool, as above, which covers divergence as a momentum reading and
  treats confirmation from price as a separate requirement.

## Comparison settings

Where the video sets three configurations against each other to show the trade off between
a faster and a smoother reading, the two either side of the default are chosen to bracket
it rather than reported as anybody's published default. Only 14, 3, 3 is presented as a
platform default, and that one is sourced above.

## Not chased to a primary source

- The claim that this is how *most* charting platforms ship the indicator. Two independent
  reference sources give 14, 3, 3 as the default, which is what supports the setting itself,
  but no census of charting platforms and their shipped defaults was found, and platform
  defaults do vary.
{% endraw %}
