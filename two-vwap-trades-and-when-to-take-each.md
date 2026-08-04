---
layout: default
title: "Two VWAP Trades, And When To Take Each"
permalink: /two-vwap-trades-and-when-to-take-each/
date: 2026-08-04
---

# Two VWAP Trades, And When To Take Each

Where the ideas in this video come from, and what to read if you want to go further than
nine minutes allows.

VWAP is unusual among the things covered on this channel in that it did not start life as a
chart indicator at all. It was a way of scoring a broker, and it arrived on retail charts
roughly twenty years after institutions began being measured against it. Most of what
follows is about that history, because it explains why the line behaves the way it does.


## Where VWAP came from

**The first execution measured against VWAP is attributed to James Elkins**, then head
trader at the New York agency brokerage Abel Noser, who used it in 1984 for the Ford Motor
Company pension fund. The idea was not to predict anything. It was to answer a question a
pension fund could not otherwise answer: given that our broker spent all day buying, did
they buy well?

- [Volume-weighted average price — Wikipedia](https://en.wikipedia.org/wiki/Volume-weighted_average_price),
  which carries the Elkins attribution and its sourcing
- Schmerken, Ivy. "Abel Noser Bets on Continuous Optimization." *Traders Magazine*,
  26 April 2022

**The academic formalisation came four years later.** Berkowitz, Logue and Noser used the
volume weighted average price over the trading day as the yardstick for total transaction
cost on the New York Stock Exchange, across roughly fourteen thousand institutional trades.
The Noser on that paper is the Noser of Abel Noser, which is the connection between the two
entries above.

- Berkowitz, Stephen A., Dennis E. Logue and Eugene A. Noser Jr. "The Total Cost of
  Transactions on the NYSE." *The Journal of Finance* 43, no. 1 (March 1988): 97–112.
  [Wiley](https://onlinelibrary.wiley.com/doi/abs/10.1111/j.1540-6261.1988.tb02591.x)

That paper is the source for the video's central point about why large orders care: the
line is a scorecard on a job, and the people being scored by it are the people whose orders
are big enough to move price.


## The calculation, and the reset

VWAP is the cumulative value traded divided by the cumulative volume traded over the chosen
window, with each bar contributing its typical price weighted by the size that went through
it. Because it is cumulative from the session open rather than rolling over a fixed number
of bars, it resets every session, which is why it describes today and nothing longer.

- [StockCharts ChartSchool — Volume-Weighted Average Price (VWAP)](https://chartschool.stockcharts.com/table-of-contents/technical-indicators-and-overlays/technical-overlays/volume-weighted-average-price-vwap),
  which sets out the running calculation step by step

## The bands

The standard deviation band idea is not native to VWAP. It is
[John Bollinger](https://www.bollingerbands.com/)'s, developed in the early 1980s, and its
original form puts the bands around a simple moving average. Applying the same construction
with VWAP as the middle line instead is a later adaptation, and it is what the video's
orange bands are.

The distances quoted in the video — about two thirds of the action inside the first pair,
about ninety five per cent inside the second — are the empirical rule for a normal
distribution (68/95/99.7), which is where every platform's default band settings come from.
Worth knowing that real price returns have fatter tails than a normal distribution does, so
the third band gets touched rather more often than 99.7 per cent would suggest.

The observation that the bands pinching in tends to precede a fast move is Bollinger's own,
and he named it the squeeze. His formulation is that low volatility follows high and high
follows low, so a contraction indicates a pending expansion without indicating its
direction.

- [StockCharts ChartSchool — Bollinger Band Squeeze](https://chartschool.stockcharts.com/table-of-contents/trading-strategies-and-models/trading-strategies/bollinger-band-squeeze)
- Bollinger, John. *Bollinger on Bollinger Bands.* McGraw-Hill, 2001

## Acceptance, and why three candles below the line is different from one

The video's test for a real break of the middle line — did price stay there, or did it dip
under and come straight back — is Market Profile's idea of acceptance, and that is
**J. Peter Steidlmayer**'s, developed in the early 1980s at the Chicago Board of Trade. The
underlying claim is that the time a market spends at a price is what tells you whether the
price was accepted or rejected, and a price the market keeps trading at is a price it has
agreed to.

- Steidlmayer, J. Peter, and Steven B. Hawkins. *Steidlmayer on Markets: Trading with
  Market Profile.* 2nd ed. Wiley, 2002
- [Market profile — Wikipedia](https://en.wikipedia.org/wiki/Market_profile)

## Why the middle of the day is thin

The video's warning about the line going quiet is a real and well documented daily pattern
rather than an impression. Intraday volume is U shaped: heavy at the open, falling to a
minimum around the middle of the session, and rising again into the close.

- Admati, Anat R., and Paul Pfleiderer. "A Theory of Intraday Patterns: Volume and Price
  Variability." *The Review of Financial Studies* 1, no. 1 (1988): 3–40 — the theoretical
  account, in which liquidity traders cluster at the open and close on purpose
- Jain, Prem C., and Gun-Ho Joh. "The Dependence Between Hourly Prices and Trading Volume."
  *Journal of Financial and Quantitative Analysis* 23, no. 3 (1988): 269–283 — the
  measurement across NYSE stocks

## VWAP as a benchmark today

The scorecard use described in the video is still current, and it is embedded in regulation.
Article 27 of MiFID II requires firms to take all sufficient steps to obtain the best
possible result for clients, and transaction cost analysis against benchmarks — VWAP among
them, alongside implementation shortfall and arrival price — is how firms evidence it.

- [ESMA — MiFID II](https://www.esma.europa.eu/publications-and-data/interactive-single-rulebook/mifid-ii)
- [T. Rowe Price — MiFID II Execution Quality Report](https://www.troweprice.com/content/dam/trowecorp/Pdfs/MiFID%20II%20Execution%20Quality%20report%20for%202020%20(PDF).pdf),
  a worked example of a real firm reporting against these benchmarks

## On the hit rates quoted for the two setups

The video gives rough figures for how often a fade from the band returns to the middle on a
rotating day against a trending one. These are the figures the trading education literature
generally quotes, and they should be read as the shape of the difference rather than as
measured constants: the gap between the two regimes is the durable finding, and the exact
proportions vary by market, by session and by how the two day types are defined in the first
place. Published backtests of band fades with a regime filter tend to land in the region of
55 to 65 per cent, and materially lower with no filter at all, which is the same point the
video is making about reading the day before taking the setup.

Anyone wanting to hold themselves to a number here should measure it on their own market and
their own definition of a rotating day rather than adopting one from a video, including this
one.

## Further reading

- Bollinger, John. *Bollinger on Bollinger Bands.* McGraw-Hill, 2001 — the bands from the
  person who built them, including the squeeze and the argument against trading a band
  touch as a signal on its own
- Berkowitz, Logue and Noser (1988), above — short, readable, and the reason the line exists
- Dalton, James F., Eric T. Jones and Robert B. Dalton. *Mind Over Markets: Power Trading
  with Market Generated Information.* Wiley, 2013 — the fullest treatment of acceptance,
  value and day types, which is the half of this video that is not about the indicator
