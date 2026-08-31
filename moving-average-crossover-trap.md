---
layout: default
title: "Your Moving Average Crossover Is Probably Too Late"
permalink: /moving-average-crossover-trap/
date: 2026-08-31
---

# Your Moving Average Crossover Is Probably Too Late

{% raw %}
Every figure, period and definition the finished picture puts on screen, chased to a
source. Anything that could not be sourced is not drawn.

## What a moving average computes

A simple moving average is the mean of the closing prices over a fixed number of periods,
so every bar inside its window carries the same weight. StockCharts states it plainly:
"A simple moving average is formed by computing the average price of a security over a
specific number of periods." Fidelity puts the same thing as "SMA is simply the mean, or
average, of the stock price values over the specified period."

- https://chartschool.stockcharts.com/table-of-contents/technical-indicators-and-overlays/technical-overlays/moving-averages-simple-and-exponential
- https://www.fidelity.com/learning-center/trading-investing/technical-analysis/technical-indicator-guide/sma

An exponential moving average weights recent prices more heavily. The weighting multiplier
is `2 / (periods + 1)`, which is the figure the weighting sled prints on screen. StockCharts
gives the formula as "Multiplier = (2 / (Time periods + 1))" and works it through with a ten
period example, where the most recent price carries 18.18 per cent of the weight.

- https://chartschool.stockcharts.com/table-of-contents/technical-indicators-and-overlays/technical-overlays/moving-averages-simple-and-exponential

## Why the reading arrives after the move

A moving average is computed from prices that have already printed, so it describes the
direction rather than anticipating it. StockCharts: "A moving average doesn't predict price
direction. Instead, it defines the current direction. However, a moving average tends to lag
because it's based on past prices."

The longer the window, the larger the delay. Fidelity: "the longer the period of the SMA,
the smoother the result, but the more lag that is introduced between the SMA and the
source." StockCharts makes the same comparison directly, noting that a 100 day average
changes course far more slowly than a 10 day one.

- https://chartschool.stockcharts.com/table-of-contents/technical-indicators-and-overlays/technical-overlays/moving-averages-simple-and-exponential
- https://www.fidelity.com/learning-center/trading-investing/technical-analysis/technical-indicator-guide/sma

Every "bars late" and "bars of lag" figure drawn against a chart in this video is measured
off the series that chart is drawing, between the bar price turned on and the bar the
crossover completed on. Nothing on screen states a general lag in bars for a given period.

## What a crossover is, and the two conventional pairs

A crossover happens when the shorter average crosses the longer one. StockCharts: "A bullish
crossover occurs when the shorter moving average crosses above the longer moving average,"
with the inverse producing the bearish signal. Fidelity describes the same rule as a trading
convention: "When a short period SMA crosses above a long period SMA, you may want to go
long. You may want to go short when the short-term SMA crosses back below the long-term SMA."

The two pairs the video names are both established conventions rather than findings.
StockCharts documents the 50 and 200 day pair, whose bullish version is widely known as the
golden cross and whose bearish version is the death cross, alongside shorter combinations
such as 5 and 35. The 9 and 21 pair is a widely used short term combination on the same
principle: a short term trend line read against a medium term one.

- https://chartschool.stockcharts.com/table-of-contents/technical-indicators-and-overlays/technical-overlays/moving-averages-simple-and-exponential
- https://www.fidelity.com/learning-center/trading-investing/technical-analysis/technical-indicator-guide/sma
- https://www.fidelity.com/viewpoints/active-investor/moving-averages

## Why a directionless market breaks the strategy

The whipsaw problem is documented rather than asserted. StockCharts: "These signals work
great when a good trend takes hold. However, when there's no strong trend, a moving average
crossover system will produce many whipsaws." Fidelity's technical indicator guide makes the
matching point about crossover systems generally, that the lag which filters noise in a trend
is the same lag that produces repeated false signals in a range.

- https://chartschool.stockcharts.com/table-of-contents/technical-indicators-and-overlays/technical-overlays/moving-averages-simple-and-exponential
- https://www.fidelity.com/learning-center/trading-investing/technical-analysis/technical-indicator-guide/macd

## The periods a charting platform ships by default

The settings dialog drawn on screen shows the inputs TradingView's built in Moving Average
actually exposes, and the length it ships with. TradingView's own documentation gives the
default Length as 9, with Source defaulting to Close and Offset to 0.

- https://www.tradingview.com/support/solutions/43000502589-moving-average/

## Not established at a primary source

- The 9 and 21 pair is described widely across trading education material as a common short
  term combination, but no exchange, vendor or standards body defines it the way the 50 and
  200 pair is documented. It is drawn on screen as the periods of two lines, and no claim is
  made on screen about how often it is used.
- Nothing in this video reports a win rate, an expectancy, a backtest result or a return.
  The parameter sweep, the equity lines and the drawdown profiles on screen are drawn from
  the series shown beside them and are labelled as illustrations, so no performance figure
  is asserted anywhere.
{% endraw %}
