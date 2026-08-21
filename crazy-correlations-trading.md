---
layout: default
title: "This Trading Correlation Trap Fools Smart Traders"
permalink: /crazy-correlations-trading/
date: 2026-08-21
---

# This Trading Correlation Trap Fools Smart Traders

{% raw %}
Every figure, definition and threshold this video puts on screen, chased to a primary
source. The worked examples are illustrative: they demonstrate a mechanism rather than
record what any particular market did on any particular day, and they are labelled that
way on screen wherever they appear.

## Relative Strength Index

RSI was published by J. Welles Wilder in *New Concepts in Technical Trading Systems*
(Trend Research, 1978). Wilder set the default lookback at 14 periods and named 70 as
overbought and 30 as oversold. The video uses the 14 period setting and the 30 threshold
exactly as Wilder defined them.

Wilder's smoothing is not a simple moving average: the first average gain and average
loss are simple means over the lookback, and every value after that is smoothed, which is
why an RSI computed with a plain moving average does not agree with the published one.

- StockCharts ChartSchool, Relative Strength Index:
  https://chartschool.stockcharts.com/table-of-contents/technical-indicators-and-overlays/technical-indicators/relative-strength-index-rsi
- TradingView, Relative Strength Index:
  https://www.tradingview.com/support/solutions/43000502338-relative-strength-index-rsi/

The point the video makes about RSI is not about the formula. An oversold reading in an
uptrend and an oversold reading in a downtrend are the same number describing two
different situations, because the reading measures the size of recent losses relative to
recent gains and says nothing about the environment those losses happened in.

## Volume weighted average price

VWAP is the cumulative typical price weighted by traded size, divided by cumulative size,
and it resets at the start of each session:

    typical price = (high + low + close) / 3
    VWAP = sum(typical price x volume) / sum(volume)

The weighting by size is the whole difference between VWAP and a moving average of price:
a price where a large amount traded pulls the line, and a price where almost nothing
traded barely moves it. The typical price rather than the close is what is averaged,
because a bar that ran high and closed back at its open did trade all the way up there.

- StockCharts ChartSchool, Volume Weighted Average Price:
  https://chartschool.stockcharts.com/table-of-contents/technical-indicators-and-overlays/technical-overlays/volume-weighted-average-price-vwap
- TradingView, Volume Weighted Average Price:
  https://www.tradingview.com/support/solutions/43000502018-volume-weighted-average-price-vwap/

## Why the S and P 500 and the Nasdaq 100 move together

The Nasdaq 100 measures 100 of the largest Nasdaq listed non financial companies. The
S and P 500 measures large capitalisation United States companies across sectors,
including those same Nasdaq listed names. A large Nasdaq listed company is therefore
eligible for both indices at once, which is why the two share a substantial number of
their largest constituents and why those shared names carry heavy weight in both.

- Nasdaq, Nasdaq 100 Index methodology:
  https://indexes.nasdaq.com/docs/Methodology_NDX.pdf
- S and P Dow Jones Indices, S and P U.S. Indices methodology:
  https://www.spglobal.com/spdji/en/documents/methodologies/methodology-sp-us-indices.pdf

The exact number of names in both indices at once changes with every index review, so
the video shows the overlap without stating a count.

## Fuel as a share of airline operating cost

The link between an oil price and an airline share price is real, and this is the size of
it. IATA's 2025 industry outlook put jet fuel at 25.8 per cent of all airline operating
costs, on an average price of 86 dollars a barrel and a total industry fuel bill of 236
billion dollars, down from 261 billion dollars in 2024.

> "Jet fuel is expected to average $86/barrel in 2025 (well below the $99 average in
> 2024), translating into a total fuel bill of $236 billion, accounting for 25.8% of all
> operating costs."

- IATA, Airline Profitability to Strengthen Slightly in 2025 Despite Headwinds,
  2 June 2025: https://www.iata.org/en/pressroom/2025-releases/2025-06-02-01/

That is roughly a quarter of the cost base, which is the point the video makes with it:
enough for fuel to matter to an airline, nowhere near enough for fuel to be the whole
company.

## Why a correlation from a small sample proves very little

For a Pearson correlation to be distinguishable from zero at the conventional five per
cent level, the value it has to reach depends heavily on how many observations produced
it. Derived from the t distribution, with r critical = t / sqrt(t squared + degrees of
freedom):

| observations | degrees of freedom | critical t | correlation needed |
| --- | --- | --- | --- |
| 7 | 5 | 2.571 | 0.754 |
| 200 | 198 | 1.972 | 0.139 |

So a correlation of 0.7 measured across seven observations does not clear the bar, while
a correlation of 0.15 measured across two hundred does. A high number from a short window
is the expected behaviour of random data, not evidence against it.

The same arithmetic covers the run of seven sessions. A run of seven independent coin
flips all landing the same way has probability 1 in 2 to the power 7, which is 1 in 128,
or 0.78 per cent. In a long enough stream of sessions, runs of seven appear regularly
without anything causing them.

- NIST/SEMATECH e-Handbook of Statistical Methods, critical values of the t distribution:
  https://www.itl.nist.gov/div898/handbook/eda/section3/eda3672.htm

## Searching until something looks good

Testing many configurations and keeping the best one inflates the best result even when
nothing in the data is real, and the more configurations are tried the worse the problem
gets. Bailey, Borwein, Lopez de Prado and Zhu showed that a strong backtest is easy to
produce from a relatively small number of alternative strategy configurations, and that
the probability a backtest is overfit rises with the number tried. Because the number of
configurations tried is almost never reported alongside the result, someone reading only
the result cannot tell how much of it is selection.

- Bailey, Borwein, Lopez de Prado and Zhu, Pseudo Mathematics and Financial Charlatanism:
  The Effects of Backtest Overfitting on Out of Sample Performance, Notices of the
  American Mathematical Society, 2014:
  https://papers.ssrn.com/sol3/papers.cfm?abstract_id=2308659
- Bailey, Borwein, Lopez de Prado and Zhu, The Probability of Backtest Overfitting:
  https://papers.ssrn.com/sol3/papers.cfm?abstract_id=2326253

The general form of the problem is not specific to trading. Ioannidis set out why a
research finding is less likely to be true when the study is small, when the effect is
small, when many relationships are tested with little preselection, and when there is
flexibility in definitions and analysis, all four of which describe a trader scanning
windows and settings for a correlation.

- Ioannidis JPA, Why Most Published Research Findings Are False, PLoS Medicine 2(8):
  e124, 2005: https://journals.plos.org/plosmedicine/article?id=10.1371%2Fjournal.pmed.0020124

## Correlations between unrelated series

Two series can produce a very high correlation coefficient with no connection between them
whatsoever. Tyler Vigen's Spurious Correlations project searched large public datasets for
exactly this and published nearly two hundred examples, each with a real Pearson
correlation and no mechanism of any kind. It is the standard demonstration that a high
correlation, on its own, carries no evidence about causation.

- Tyler Vigen, About Spurious Correlations:
  https://tylervigen.com/about-spurious-correlations

The reef counts, oat milk orders, chair squeaks and pizza sales in this video are invented
for the sake of the argument and are shown as such. The behaviour they illustrate, that
unrelated series routinely correlate strongly, is the documented one above.

## Correlation, lead lag and concentration

Three separate ideas the video keeps apart, and the reason it keeps them apart:

Correlation measures whether two series moved together over a measured window. It carries
no information about which one moved first, and none about whether a trade in either was
available at a usable price.

Lead lag asks whether one series reliably moves before the other, which is a different
measurement: the correlation is computed at a range of offsets rather than at zero, and
what matters is whether a peak away from zero is stable rather than whether the value at
zero is large.

Concentration is what correlation between open positions actually tells an account
holder. Positions that are highly correlated with each other do not diversify risk, so
several positions that all depend on the same market direction carry closer to the risk
of one large position in that direction than to the risk of several independent ones.
This is the mechanism behind the video's point about holding several names that all
track the same index.

## Not chased to a primary source

- The number of Nasdaq 100 constituents that are also S and P 500 constituents. It moves
  at every index review, so no count is stated or shown.
- The relative contribution of oil, earnings, travel demand, debt, regulation and the
  broad market to any particular airline share price. Fuel's share of operating cost is
  sourced above; the split of what moves the share price is not, and the video shows
  those inputs unsized rather than claiming proportions.
- Whether price reacts at VWAP more often than at an arbitrary line. The video says
  traders watch it and that price can bounce, cut through or chop around it, and does
  not claim a hit rate for any of the three.
{% endraw %}
