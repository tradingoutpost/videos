---
layout: default
title: "The Cheese Indicator Has Holes Most Traders Miss"
permalink: /cheese-indicator/
date: 2026-08-20
---

# The Cheese Indicator Has Holes Most Traders Miss

{% raw %}
Every figure, name, setting and definition this video puts on screen, chased to the
place it actually comes from.

## The indicator itself

The tool the video takes apart is a real, published one, and its module list is not a
paraphrase: it is the list its own page gives.

- **Name and author.** "Colby Cheese VWAP Setup", by the TradingView user
  **dscottmuller**, published in a v1.0 and a later v2.0. Free to use, published closed
  source.
  https://www.tradingview.com/script/4s5uadpn-Colby-Cheese-VWAP-Setup-v1-0/
  https://www.tradingview.com/script/H62iZaXq-Colby-Cheese-VWAP-Setup-v2-0/

- **What it combines.** Change of character detection, VWAP deviation bands, an EMA
  stack bias, a delta and cumulative volume delta filter, strongest imbalance logic,
  engulfing confirmation, and fixed range volume profile based entry zones. Same source
  as above. This is the list the video walks through in order, and it is why the video
  treats the tool as a stack rather than as a single signal.

- **The EMA periods on screen are 13, 35 and 50**, which are the periods the indicator's
  own stack bias uses. Same source as above. Nothing in this video shows a moving average
  length that the tool does not actually use.

- **Change of character detection** in this tool reads swing highs and lows from either
  the chart's own data or a three minute feed. Same source as above.

- **Entry zones** are pullback zones drawn to recent range extremes using fixed range
  volume profile. Same source as above.

- **In v2.0** an anticipation mode draws its lines and labels when delta and bias agree
  **before** the change of character is confirmed, and change of character signals only
  fire when the price change agrees with the EMA bias.
  https://www.tradingview.com/script/H62iZaXq-Colby-Cheese-VWAP-Setup-v2-0/

## VWAP

- **Definition and formula.** The volume weighted average price is the average price
  weighted by volume, computed as cumulative typical price multiplied by volume, divided
  by cumulative volume. Price moves on higher volume carry more weight than price moves on
  low volume, which is the whole difference between it and an ordinary moving average.
  https://www.tradingview.com/support/solutions/43000502018-volume-weighted-average-price-vwap/

- **It is an intraday reference and it resets.** The calculation begins at the open and
  stops at the close, and the anchor period controls how often it restarts. That reset is
  why it reads as a fair value reference for the session rather than a longer average, and
  it is why the charts in this video are built one session at a time.
  https://www.tradingview.com/support/solutions/43000502018-volume-weighted-average-price-vwap/

- **Deviation bands.** Bands set a chosen number of standard deviations above and below
  the VWAP line, used as dynamic support and resistance and as a way to see when intraday
  price has stretched a long way from the line. The charts here draw one and two standard
  deviations, which is the common pair.
  https://help.trendspider.com/kb/indicators/vwap-with-st-dot-dev-bands
  https://www.schwab.com/learn/story/how-to-use-volume-weighted-indicators-trading

## Moving averages

- **They are built from past prices and they lag.** A moving average follows price action
  rather than leading it, and the longer the average, the more it lags. That is the basis
  for the video's point that a stack can confirm momentum after the clean part of a move
  has already gone.
  https://chartschool.stockcharts.com/table-of-contents/technical-indicators-and-overlays/technical-overlays/moving-averages-simple-and-exponential
  https://www.schwab.com/learn/story/simple-vs-exponential-moving-averages

- **An exponential moving average weights recent prices more heavily** than older ones,
  which makes it quicker to react than a simple average while still trailing price.
  https://chartschool.stockcharts.com/table-of-contents/technical-indicators-and-overlays/technical-overlays/moving-averages-simple-and-exponential

## Volume pressure

- **Delta and cumulative volume delta.** Delta is the difference between volume traded
  aggressively at the ask and volume traded aggressively at the bid. Cumulative volume
  delta is the running total of that, rising while aggressive buying dominates and falling
  while aggressive selling does.
  https://www.luxalgo.com/library/concept/cumulative-volume-delta/

- **Absorption.** When aggressive selling keeps arriving and price refuses to fall, the
  aggression is being met by passive orders that keep refilling. This is exactly the case
  the video describes as aggressive selling looking bearish at the moment price stops going
  down, and the reverse for buying.
  https://bookmap.com/blog/how-cumulative-volume-delta-transform-your-trading-strategy

- **Effort against result.** Where price makes a new extreme and cumulative volume delta
  does not follow, the aggression is not producing progress. That divergence is the
  documented reading behind the video's point that the pressure can exist while the result
  does not.
  https://www.luxalgo.com/library/concept/cumulative-volume-delta/

## Market structure

- **Change of character.** A break of the most recent higher low in an uptrend, or of the
  most recent lower high in a downtrend. It is read as a warning of a possible turn.
  https://dailypriceaction.com/blog/smc-market-structure/

- **Break of structure**, by contrast, is a break in the same direction as the existing
  trend and is read as continuation. The distinction matters to the video's argument that a
  break is a question about which of the two just happened, not an answer.
  https://dailypriceaction.com/blog/smc-market-structure/

## Fixed range volume profile

- **What the entry zones are drawn from.** A fixed range volume profile measures volume at
  price across a selected part of the chart, usually swing point to swing point, and shows
  where trade concentrated. It reports a point of control at the heaviest level, a value
  area holding a chosen share of the volume, and high and low volume nodes.
  https://www.tradingview.com/support/solutions/43000707985-fixed-range-volume-profile-drawing-tool/

## When a signal is actually visible

- **Repainting** is an indicator changing its historical signals once later bars arrive, so
  a marker moves or disappears from where it first showed. Testing against repainted history
  reads future information into the past.
  https://blog.traderspost.io/article/what-is-repainting-in-tradingview
  https://crosstrade.io/blog/pine-script-repainting

- **Acting only on a confirmed bar.** The documented way to avoid taking a signal that has
  not finished forming is to require the bar to be closed before acting on it. This is the
  basis for the video's point that a test should assume the trader could only act after the
  close.
  https://crosstrade.io/blog/pine-script-repainting

- The video is careful that a condition confirming late is **not the same thing as
  repainting**, and that distinction is the one the sources above draw as well: a signal
  that needs several conditions to align is visible late, while a repainting one moves after
  the fact.

## The charts

Every chart in this video is **illustrative**. The price series are generated to show a
mechanism cleanly, and they are labelled on screen as illustrative wherever they appear.
They are never used to claim that a particular move, win rate or result happened in a real
market, and no performance figure, backtest result or historical price appears anywhere in
the video.

The indicator settings drawn on those charts are the real ones listed above.

## Not checked

- The exact swing detection rule, imbalance score and engulfing test inside the Cheese
  indicator cannot be read, because the script is published closed source. The video
  describes those modules at the level its own page describes them and does not state how
  any of them is computed internally.
- Whether this particular indicator repaints. The video does not claim it does; it makes
  the general point that a signal depending on a close or on a swing point is visible later
  than a finished chart makes it look, and asks the reader to establish the rule for
  whatever they are testing.
{% endraw %}
