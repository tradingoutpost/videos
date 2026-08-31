---
layout: default
title: "Your VWAP Entries Are Failing For One Simple Reason"
permalink: /mastering-vwap-entries/
date: 2026-08-31
---

# Your VWAP Entries Are Failing For One Simple Reason

{% raw %}
Every factual claim this video makes about what VWAP is, how it is calculated, when it
resets and who uses it, chased to a source and cited. The trade management ideas built on
top of those facts (what a pullback, a reclaim or a rejection is, where a stop belongs)
are method rather than fact, and are presented as method.

Every chart in this video is an illustrative price series built to show a mechanism. No
chart carries a ticker or a date and nothing here claims that a particular market did a
particular thing on a particular day.


## What VWAP is, and how it is calculated

**Claim.** VWAP means volume weighted average price: the average price the session has
transacted at, with every price weighted by the size that went through it, so a price where
a large amount traded pulls the line and a price where almost nothing traded barely moves
it.

**Source.** TradingView's indicator documentation gives the calculation as
`VWAP = Cumulative(Typical Price x Volume) / Cumulative(Volume)`, with the typical price
for each period taken as `(High + Low + Close) / 3`.

- https://www.tradingview.com/support/solutions/43000502018-volume-weighted-average-price-vwap/
- https://en.wikipedia.org/wiki/Volume-weighted_average_price

**Claim.** That weighting is what makes it different from a moving average, which gives
every bar in its window the same influence regardless of how much traded.

**Source.** Follows directly from the two formulas: the moving average divides by a count
of periods, VWAP divides by the total volume across them. Same source as above.


## The session reset

**Claim.** Standard VWAP resets at the session open, which is what makes it a reading about
today rather than a longer average, and why it is jumpy at the open and stubborn near the
close.

**Source.** TradingView's documentation describes an Anchor Period setting that specifies
"how frequently the VWAP calculation will be reset", with Session as one of the available
anchors alongside Week, Month, Quarter and Year.

- https://www.tradingview.com/support/solutions/43000502018-volume-weighted-average-price-vwap/

The behaviour at each end of the session follows from the calculation being cumulative:
early in the session the running totals are small, so one more trade moves the ratio a long
way; late in the session most of the day's volume is already inside the sums, so the same
trade moves it very little.


## VWAP as an execution benchmark

**Claim.** Institutions use VWAP as an execution benchmark, and a large buyer filled below
VWAP has achieved a better average fill than one filled above it. A large seller filled
above it has done the same in reverse.

**Source.** The measure was introduced in the academic literature by Berkowitz, Logue and
Noser, who used the volume weighted average price over the trading day to measure the
execution cost of institutional transactions on the NYSE, applied to a set of more than
fourteen thousand actual trades.

- Berkowitz, S. A., Logue, D. E. and Noser, E. A. Jr. (1988), "The Total Cost of
  Transactions on the NYSE", *The Journal of Finance*, 43(1), 97 to 112.
  https://doi.org/10.1111/j.1540-6261.1988.tb02591.x

The CFA Institute's curriculum on trade strategy and execution describes VWAP as one of the
two common intraday benchmarks used to measure trade execution, alongside time weighted
average price, and as the benchmark of choice for managers participating with volume over
an execution horizon rather than acting on a short term view.

- https://www.cfainstitute.org/insights/professional-learning/refresher-readings/2026/trade-strategy-execution

**Not claimed.** The video is explicit that this does not mean an institution is defending
the line. Being measured against a benchmark is a reason to care where price is relative to
it; it is not a commitment to hold it.


## The session clock on the charts

**Claim.** The charts are labelled 09:30 through 16:00 on five minute bars, which is a
regular United States equity session.

**Source.** The NYSE publishes its core trading session for equities as 9:30 a.m. to
4:00 p.m. Eastern Time, with the opening auction at 9:30 and the closing auction at 4:00.

- https://www.nyse.com/markets/hours-calendars


## Figures on screen

Every number the video prints is computed at render time from the series it is drawn over
rather than typed into a shot: reward multiples from the entry, stop and target prices in
the bracket; the count of VWAP crossings and the count of bars spent on one side from the
series itself; the weighted price under the beam from the weights loaded onto it. There are
no stated performance figures, win rates or backtest results anywhere in this video, and
none are claimed.
{% endraw %}
