---
layout: default
title: "Why Your Candlestick Patterns Keep Failing"
permalink: /the-candlestick-trap-that-fools-most-traders/
date: 2026-08-12
---

# Why Your Candlestick Patterns Keep Failing

This video makes no numerical claim. It states no win rate, no hit rate, no backtest, no
price, no date and no benchmark, and nothing on screen states one either. What it does
assert is a set of definitions and a set of market mechanics, and those are what is chased
to a primary source below.

Every chart in the video is a synthetic series generated for teaching, and each one says
so on screen. No chart is presented as a record of what any market did.

## What a candlestick encodes

**Claim.** Every candle shows four things for its period: where price opened, where it
closed, how high it went and how low it went. The body spans the open and the close, and
the wick spans from the body out to the extreme actually traded.

**Claim.** A bullish candle is one that closed higher than it opened. A bearish candle is
one that closed lower than it opened.

CME Group's technical analysis course states this directly: candlestick charts take the
same information as a bar chart, open, high, low and close, and represent it as a body and
a wick, where "the body of the candle, the thicker middle portion, shows the open and
closing prices during the time frame" and "the wick, illustrated by a thin line at the top
and bottom of the body, shows the highest and lowest prices traded over the time frame".
It also gives the colour convention the video uses, that a candle closing below its open
is drawn one way and one closing above its open the other.

- CME Group, *Chart Types: candlestick, line, bar*, Technical Analysis course.
  https://www.cmegroup.com/education/courses/technical-analysis/chart-types-candlestick-line-bar

## The pattern names

**Claim.** Engulfing candles, pin bars, doji, hammers, shooting stars, morning stars and
evening stars are the named candlestick patterns a new trader learns first, and an
engulfing candle is one whose body covers the body of the candle before it.

These are the definitions set out in Steve Nison's *Japanese Candlestick Charting
Techniques*, the work that introduced the Japanese candlestick vocabulary to Western
markets and remains the reference the names are taken from. An engulfing pattern there is
defined by the real body of one candlestick completely covering the real body of the
previous one; hammer, shooting star and doji are treated as single candle reversal
patterns, and the morning and evening stars as the multi candle star formations.

- Steve Nison, *Japanese Candlestick Charting Techniques: A Contemporary Guide to the
  Ancient Investment Techniques of the Far East*, 2nd ed., New York Institute of Finance.
  https://books.google.com/books/about/Japanese_Candlestick_Charting_Techniques.html?id=-gXKAgAAQBAJ

## Trend as a sequence of highs and lows

**Claim.** In an uptrend buyers are generally creating higher highs and higher lows, and in
a downtrend sellers are generally creating lower lows and lower highs. A bullish pattern
that leaves that sequence intact has not yet proved a reversal.

This is the structural definition of trend from Dow Theory, codified after Charles Dow's
death by William Peter Hamilton in *The Stock Market Barometer* (1922) and Robert Rhea in
*The Dow Theory* (1932): an uptrend is a sequence of higher highs and higher lows, and a
downtrend its mirror image. The HH, HL, LH and LL labelling the video uses on screen is the
direct descendant of that rule.

- StockCharts ChartSchool, *Dow Theory*, summarising Rhea's codification of the six tenets.
  https://chartschool.stockcharts.com/table-of-contents/market-analysis/dow-theory

## What happens when a stop is triggered

**Claim.** Price pushing through an obvious high or low triggers stops, and that triggering
is itself a source of the move that follows.

A stop order is an instruction to buy or sell once price reaches a specified stop price, and
the SEC is explicit that the stop price is a trigger rather than a guaranteed execution
price: when the stop price is reached, the stop order becomes a market order and executes at
whatever the market is then offering. That is the mechanism by which a cluster of stops
sitting beyond a level turns into a burst of market orders the moment the level is crossed.

- U.S. Securities and Exchange Commission, *Investor Bulletin: Stop, Stop-Limit, and
  Trailing Stop Orders*. https://www.sec.gov/oiea/investor-alerts-bulletins/ib-stoporders

## Why orders sit beyond obvious levels

**Claim.** Many dramatic candlestick patterns form around liquidity grabs: price runs into
an area where orders were likely sitting, fails to continue, and rejects. Price pushing
above an obvious high triggers breakout buyers and short stops; pushing below an obvious
low triggers breakout sellers and long stops.

Carol Osler's study in the *Journal of Finance* is the first work built on individual
currency stop-loss and take-profit order data, and it documents exactly this clustering:
take-profit orders cluster strongly at round numbers, and stop-loss orders cluster strongly
just beyond them, at the round numbers that are commonly used as support and resistance
levels. Osler uses that clustering to explain two long-standing technical claims, that
trends tend to reverse at predictable support and resistance levels, and that moves tend to
be unusually rapid once those levels are crossed. Stop-loss orders in particular are found
to intensify trends rather than damp them.

- Carol L. Osler, "Currency Orders and Exchange Rate Dynamics: An Explanation for the
  Predictive Success of Technical Analysis", *The Journal of Finance*, vol. 58, no. 5
  (2003), pp. 1791-1819. https://onlinelibrary.wiley.com/doi/abs/10.1111/1540-6261.00588
- Working paper version, Federal Reserve Bank of New York Staff Report no. 125.
  https://www.newyorkfed.org/medialibrary/media/research/staff_reports/sr125.pdf

## Sizing a stop against normal noise

**Claim.** A stop that sits inside normal candle noise can be taken out before the setup has
a chance, because markets have noise, spreads and volatility around any level.

The standard measure of that noise is the true range and its average, introduced by J.
Welles Wilder in *New Concepts in Technical Trading Systems* (1978). Wilder defines true
range as the greatest of the current high less the current low, the absolute difference
between the current high and the previous close, and the absolute difference between the
current low and the previous close, and averages it to produce a per period volatility
figure. The volatility system in the same book places its stop at a distance derived from
that figure, widening the gap from price as volatility rises, which is the practice the
video describes when it says an invalidation should sit outside normal noise rather than on
the line itself.

- J. Welles Wilder, *New Concepts in Technical Trading Systems*, Trend Research, 1978.
  https://archive.org/details/newconceptsintec00wild

## Not checked

These are assertions the video makes that could not be chased to a primary source. They are
judgements about how traders behave and about which considerations matter most, not
measured results, and none of them is presented on screen as a figure.

- That most traders read candlesticks in isolation, and that this is the main reason
  candlestick trades fail. No survey or study of trader behaviour is cited for it.
- That location is probably the most important filter of the six. This is a ranking, and no
  comparative test of the six filters against each other is cited.
- That waiting for the next candle to prove acceptance improves outcomes relative to
  entering at the close of the signal candle. Widely taught, but no measured comparison is
  cited here.
- The specific acceptance tests named, holding above or below the midpoint of the signal
  candle, breaking the signal candle's high or low, and forming a higher low or lower high
  after the rejection, are conventions in common use rather than standards with a defined
  source.
- That a hammer at a major support level after a stop run and followed by a strong reclaim
  can be bullish, while the same shape mid trend may be nothing. Stated as a conditional
  judgement about context, not as a measured edge, and no hit rate is claimed for either.
- All price series shown are synthetic and are labelled as illustrative on screen. They
  demonstrate the mechanisms described and are not records of any market.
