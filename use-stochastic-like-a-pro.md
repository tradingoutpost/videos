---
layout: default
title: "Stop Using Stochastic Until You See The Real Trap"
permalink: /use-stochastic-like-a-pro/
date: 2026-08-30
---

# Stop Using Stochastic Until You See The Real Trap

{% raw %}
Every figure, level, setting and definition the finished picture puts on screen, chased to
a primary source. Anything that could not be chased is listed at the bottom and is not
drawn.

## What the oscillator measures

The stochastic oscillator reports where the close sits inside the high to low range of the
lookback period, expressed from zero to one hundred. StockCharts states it as "the level of
the close relative to the high-low range over a given period", and quotes George Lane, who
developed it in the late 1950s, saying that it "doesn't follow price, it doesn't follow
volume or anything like that. It follows the speed or the momentum of price."

- StockCharts ChartSchool, Stochastic Oscillator (Fast, Slow and Full):
  https://chartschool.stockcharts.com/table-of-contents/technical-indicators-and-overlays/technical-indicators/stochastic-oscillator-fast-slow-and-full

## The formula on screen

```
%K = (close  minus  lowest low) / (highest high  minus  lowest low) x 100
%D = 3 period simple moving average of %K
```

Lowest low is the lowest low of the lookback period and highest high the highest high of
the same period. Both are stated in that form by StockCharts. TradingView documents the
smoothed version its own indicator computes as `%K = SMA(100 * (close - lowest low) /
(highest high - lowest low), smoothK)` and `%D = SMA(%K, periodD)`, which is the same
measurement with a smoothing pass added.

- StockCharts ChartSchool, as above.
- TradingView, Stochastic (STOCH) indicator documentation:
  https://www.tradingview.com/support/solutions/43000502332-stochastic-stoch/

## Fourteen, three, three

The three numbers drawn on the setting drums are the lookback period, the %K smoothing and
the %D smoothing.

TradingView's built in Stochastic ships with %K Length 14, %K Smoothing 3 and %D Smoothing
3. StockCharts gives the Full Stochastic Oscillator default as (14,3,3), with the same three
roles, and the Fast and Slow versions as (14,3).

Not every platform ships those numbers. MetaTrader 5's Stochastic Oscillator defaults to a
%K period of 5, a %D period of 3 and a slowing of 3, so the picture attributes 14, 3, 3 to
the platforms that actually document it rather than to platforms in general.

- TradingView, Stochastic (STOCH): https://www.tradingview.com/support/solutions/43000502332-stochastic-stoch/
- StockCharts ChartSchool, Stochastic Oscillator (Fast, Slow and Full), link above.
- MetaTrader 5 help, Stochastic Oscillator:
  https://www.metatrader5.com/en/terminal/help/indicators/oscillators/so

## The eighty and twenty levels

Eighty is the conventional overbought threshold and twenty the conventional oversold
threshold. StockCharts: "Traditional settings use 80 as the overbought threshold and 20 as
the oversold threshold." TradingView ships the same two levels on its built in indicator.
Binance Academy teaches the same pair as a buy and sell reading, which is the reading this
video is about.

- StockCharts ChartSchool, link above.
- TradingView, Stochastic (STOCH), link above.
- Binance Academy, 5 Essential Indicators Used in Technical Analysis:
  https://academy.binance.com/en/articles/5-essential-indicators-used-in-technical-analysis

## A reading above eighty is not by itself bearish

StockCharts states it directly: "Overbought readings aren't necessarily bearish. Securities
can become overbought and remain overbought during a strong uptrend", and adds that "this
is why it's important to identify the bigger trend and trade in the direction of this
trend." The same page notes the indicator "can also be used to identify turns near support
or resistance."

- StockCharts ChartSchool, link above.

## Divergence

Drawn to the standard definitions. "A bullish divergence forms when price records a lower
low, but the Stochastic Oscillator forms a higher low." "A bearish divergence forms when
price records a higher high, but the Stochastic Oscillator forms a lower high."

Every divergence drawn in this video is found in the plotted series by the swing pivot test
rather than placed by hand, so no line is drawn between two points chosen to lean the right
way.

- StockCharts ChartSchool, link above.

## The other indicators shown briefly

One shot shows several momentum tools stacked under one chart. Each is computed from the
same bars to its published definition rather than sketched.

- Relative strength index, Wilder's smoothing, period 14.
- MACD, the twelve and twenty six period exponential moving average difference with a nine
  period signal line.
- Commodity channel index: "CCI = (Typical Price - 20-period SMA of TP) / (.015 x Mean
  Deviation)", typical price being "(High + Low + Close)/3", with the standard plus and
  minus one hundred levels. The 0.015 constant is Donald Lambert's, chosen so that most
  readings fall inside that band.

- StockCharts ChartSchool, Commodity Channel Index:
  https://chartschool.stockcharts.com/table-of-contents/technical-indicators-and-overlays/technical-indicators/commodity-channel-index-cci

## The price series on screen

Every chart in this video is an illustrative series, generated to show the mechanism being
described, and it is labelled as illustrative on screen wherever it appears. No chart
asserts that a particular thing happened in a particular market at a particular time, and
no reading, win rate or outcome is claimed from one. Every number printed beside a chart is
computed from the bars actually drawn, at the settings named on screen.

## Not checked

- The claim that most platforms use fourteen, three, three. Two platforms are documented at
  those values and one widely used platform is documented at five, three, three, so the
  picture shows the setting and names only the platforms that publish it, and never states
  a share of the market.
- The behaviour of any specific instrument, session or date. Nothing of the sort appears on
  screen.
{% endraw %}
