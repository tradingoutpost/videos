---
layout: default
title: "Your Stop Was Never Wrong. It Was Just Too Close."
permalink: /avoid-this-scalping-mistake/
date: 2026-08-06
---

# Your Stop Was Never Wrong. It Was Just Too Close.

Every figure this video puts on screen, and where it comes from.

Three kinds of number appear, and they are labelled on screen as they appear:

- **Definitional.** How an indicator is calculated, what a lot is, which price a stop is
  checked against. Cited to the platform or the original description.
- **Simulated.** A result that follows from a stated model, named on screen as
  "Simulated: driftless random walk". The model is the argument, so it is stated rather
  than hidden, and every figure taken from it is reproducible from the model alone.
- **Illustrative.** An invented one minute series used to show a mechanism, labelled
  "Illustrative" on screen. No illustrative number asserts that anything happened.

Nothing here asserts a historical result, a win rate or a backtest, and no figure in this
video is presented as measured from a real price series.


## Average true range

**True range is the greatest of three measures: the bar's high minus its low, the absolute
distance from the previous close to this bar's high, and the absolute distance from the
previous close to this bar's low. Average true range is a smoothed average of that.**

The indicator is J. Welles Wilder's, introduced in *New Concepts in Technical Trading
Systems* (Trend Research, 1978).

- TradingView, Average True Range (ATR) help: "J. Welles Wilder created the ATR and
  featured it in his book New Concepts in Technical Trading Systems. The book was
  published in 1978." It also states that absolute values are used "because the ATR does
  not measure price direction, only volatility".
  https://www.tradingview.com/support/solutions/43000501823-average-true-range-atr/
- StockCharts ChartSchool, Average True Range: sets out the same three candidate measures
  and the smoothing.
  https://chartschool.stockcharts.com/table-of-contents/technical-indicators-and-overlays/technical-indicators/average-true-range-atr-and-average-true-range-percent-atrp
- Wilder, J. Welles, *New Concepts in Technical Trading Systems*, 1978.
  https://books.google.com/books/about/New_Concepts_in_Technical_Trading_System.html?id=WesJAQAAMAAJ

**The 14 period setting.** Fourteen is the platform default and the most common choice
rather than a law of nature. TradingView: "The look back period to use for the ATR is at
the trader's discretion however 14 days is the most common", and 14 is the default in its
inputs. The video shows ATR 14 and says the number belongs to the timeframe it is measured
on.


## The reach over several bars

**Over n bars, the distance price covers grows with the square root of n, not with n.**

This is the square root of time scaling of a driftless random walk. It is the same rule
supervisors use to scale a one day risk figure to a ten day one, by multiplying by the
square root of ten.

- Danielsson, J. and Zigrand, J-P., "On time-scaling of risk and the square-root-of-time
  rule", London School of Economics, Financial Markets Group discussion paper 439.
  Sets out the rule, its assumptions and where it breaks down.
  https://eprints.lse.ac.uk/24827/1/dp439.pdf
- Danielsson and Zigrand, *Journal of Banking and Finance*, 2006, the published version.
  https://www.sciencedirect.com/science/article/abs/pii/S0378426606000070

**The ladder on screen, 1 bar 2.0, 4 bars 4.0, 9 bars 6.0, 16 bars 8.0 pips**, is that rule
applied to an ATR of 2.0 pips. Four times the bars, twice the distance.

**Ten bars gives ATR times the square root of ten, about 6.3 pips.** Same arithmetic,
2.0 x 3.162.

**Why the range and the deviation are not the same number.** The expected high to low range
of a driftless random walk over a period is the square root of eight over pi, about 1.60,
times its standard deviation over that period. Converting between the two is what lets an
ATR reading be used in a probability rather than being compared to one.

- Feller, W., "The asymptotic distribution of the range of sums of independent random
  variables", *Annals of Mathematical Statistics*, 1951, gives the distribution of the
  range. Parkinson, M., "The extreme value method for estimating the variance of the rate
  of return", *Journal of Business*, 1980, gives its moments and is the basis of every
  high-low volatility estimator since.
  https://link.springer.com/article/10.1007/s11203-020-09229-x

## The chance a stop is touched

**A stop d away is touched at some point within n bars with probability twice the normal
probability of finishing beyond it.** This is the reflection principle for the running
minimum of a driftless random walk: the path reaches a level with twice the probability
that the endpoint is beyond it, because every path that reaches the level and comes back
pairs with one that reaches it and carries on.

- MIT OpenCourseWare 15.070J Advanced Stochastic Processes, Lecture 7, Brownian motion,
  states the reflection principle and the first passage result.
  https://ocw.mit.edu/courses/15-070j-advanced-stochastic-processes-fall-2013/aca1518a09539a09ddd37428ab0d0268_MIT15_070JF13_Lec7.pdf
- Lalley, S., University of Chicago, Lecture 5, Brownian motion, gives the same argument.
  http://galton.uchicago.edu/~lalley/Courses/390/Lecture5.pdf

Applied to an ATR of 2.0 pips over ten bars, that gives the two figures on screen:

| Distance the market has to travel | Chance it is touched within ten bars |
| --- | --- |
| 3 pips | 45% |
| 7 pips | 8% |

And the pair used for the two hours:

| Hour | ATR shown | Chance a 4 pip stop is touched |
| --- | --- | --- |
| Quiet | 1.0 pips | 13% |
| London and New York overlap | 3.0 pips | 61% |

Both rows follow from the model alone and are reproducible from it. They are labelled on
screen as simulated, and the ATR values they use are labelled illustrative.


## Bid, ask, and where the stop really sits

**You buy at the ask and sell at the bid, so a round trip crosses the spread.** This is the
definition of the two quotes rather than a claim about any particular market.

**A stop on a long position is checked against the bid, not against the price you paid.**
MetaTrader 5's own documentation: "This order condition for long positions is checked using
the Bid price (the order is always set below the current Bid price) and the Ask price is
used for short positions (the order is always set above the current Ask price)."

- MetaTrader 5 Help, Trading, Basic Principles.
  https://www.metatrader5.com/en/terminal/help/trading/general_concept
- MetaTrader 4 Help, Order Types, states the same rule.
  https://www.metatrader4.com/en/trading-platform/help/positions/orders

That is where the arithmetic on screen comes from. A stop set four pips below the fill on a
one pip spread is three pips from where the bid was at entry, because the bid started one
pip below the fill. The spread is a fixed subtraction, so it takes a quarter of a four pip
stop, an eighth of an eight pip stop and a twentieth of a twenty pip stop.

**A touch is enough.** A stop order becomes a market order the moment the trigger price is
reached; nothing has to close beyond it. Nasdaq's glossary: a stop loss order is "an order
to sell a stock when the price falls to a specified level".

- Nasdaq glossary, stop-loss order.
  https://www.nasdaq.com/glossary/s/stop-loss-order

**The one pip spread used throughout.** Retail standard account spreads on EUR/USD sit
around this level and vary by broker and by account type. Broker testing published in 2026
put the all-in average across a field of retail brokers at about 0.86 pips on EUR/USD, with
standard accounts commonly quoted between 0.8 and 1.6 pips. One pip is a round number in
that range rather than any single broker's figure.

- Compare Forex Brokers, spread testing methodology and results.
  https://www.compareforexbrokers.com/our-methodology/forex-fees/tightest-spreads/

**The spread is not a constant.** It widens with volatility and around scheduled releases,
which is what the video shows happening to the distance a stop really sits at.

- Financial Conduct Authority, Occasional Paper 63, on liquidity provision around
  scheduled macroeconomic announcements.
  https://www.fca.org.uk/publication/occasional-papers/op63.pdf


## Not every hour is the same

**Activity in foreign exchange is concentrated in the hours when the two largest centres
are both open.** The Bank for International Settlements' Triennial Central Bank Survey for
April 2025 puts the United Kingdom at about 38% of global foreign exchange trading and the
United States at about 19%, the two largest shares by a wide margin, with global turnover
at 9.6 trillion dollars a day.

- BIS, OTC foreign exchange turnover in April 2025.
  https://www.bis.org/statistics/rpfx25_fx.htm

**Within a day, volume, quote revision and volatility move together, and the spread moves
against them.** Ito and Hashimoto examined firm quotes and transactions on an electronic
broking system and confirmed a U shape in intraday activity for Tokyo and London
participants.

- Ito, T. and Hashimoto, Y., "Intraday seasonality in activities of the foreign exchange
  markets: evidence from the electronic broking system", *Journal of the Japanese and
  International Economies*, 20(4), 2006, pp. 637 to 664.
  https://www.nber.org/papers/w12413

The hour by hour profile drawn on screen is labelled illustrative. It carries that shape,
quietest through the late Asian hours and heaviest across the London and New York overlap,
and it is not a measurement of any particular day.


## Position size

**One standard lot is 100,000 units of the base currency, and on a pair quoted to four
decimal places against the dollar one pip on that size is ten dollars.**

- OANDA, what is a pip.
  https://www.oanda.com/bvi-en/cfds/learn/introduction-to-leverage-trading/what-is-a-pip/

From that, with a fifty dollar risk budget, which is one per cent of a five thousand dollar
account:

| Stop | Risk per pip | Size | Spread paid on a round trip at one pip |
| --- | --- | --- | --- |
| 4 pips | 12.50 | 1.25 lots | 12.50 |
| 8 pips | 6.25 | 0.63 lots | 6.25 |

Both positions lose the same fifty dollars if the stop is reached. The wider stop is the
smaller position and crosses the spread at half the cost.


## What was not checked

- The one minute series on screen is invented from a stated model. Its ATR reads 2.0 pips
  because the model was chosen to make it read that, not because any market did.
- The ATR figures for the two hours, 1.0 pips and 3.0 pips, are illustrative values carrying
  the published shape of intraday activity. They are not measurements of a particular
  session, pair or day.
- The dollar and cent figures shown beside the currency example are illustrative, to make
  the point that the same measurement arrives in a different unit in each market.
- The touch probabilities assume a driftless random walk with constant volatility.
  Real returns have fatter tails and volatility that clusters, so the true chance of a very
  close stop being touched is higher than the model says, not lower. The direction of that
  error works against tight stops rather than for them.
- Ten bars is used throughout as a stand in for how long a short term trade is open. It is a
  round number for the arithmetic, not a claim about how long anybody holds.
- Spreads and volatility both move. Every figure here is a level, and the point of the
  video is that the level has to be measured rather than remembered.
