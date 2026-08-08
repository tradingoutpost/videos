---
layout: default
title: "Top 5 Trading Strategies Explained in 10 Minutes"
permalink: /top-5-trading-strategies-explained-in-10-minutes/
date: 2026-08-08
---

# Top 5 Trading Strategies Explained in 10 Minutes

Everything this video states as fact, and where it comes from.

Two categories are kept apart deliberately, because they carry very different weight:

**Definitions.** Where the video says what an indicator or a convention *is*, the source is
the person who defined it, or the reference implementation everyone else copies. These are
settled and there is no argument to have about them.

**Worked examples.** Where the video says "imagine price moves from 100 to 110", that is a
teaching example the script invents to make a mechanism visible. Every chart in the video is
generated for the same reason, and each one carries an `Illustrative` mark on screen. None
of it is a record of anything that happened in a market, and it is not offered as one.

**No performance claim is made anywhere in this video, and none was measured.** There is no
win rate, no hit rate, no backtest and no equity curve taken from a real system. The two
percentages the video does arithmetic on are its own invented examples, and they are listed
below as such.


## Definitions

### Relative Strength Index, and the 70 and 30 levels

The video shows an RSI pane with an overbought rule at 70 and an oversold rule at 30, and
says that a reading above the upper rule is called overbought and below the lower one
oversold.

RSI was defined by J. Welles Wilder Jr. in *New Concepts in Technical Trading Systems*
(1978), along with the 14 period default and the 70 and 30 levels the video draws. Wilder's
own framing is the one the video uses: these are readings that describe how fast price has
moved, not instructions.

- StockCharts ChartSchool, Relative Strength Index (RSI), which documents Wilder's original
  definition, the 14 period default and the 70 / 30 levels:
  https://chartschool.stockcharts.com/table-of-contents/technical-indicators-and-overlays/technical-indicators/relative-strength-index-rsi
- AAII, Measuring Internal Strength: Wilder's RSI Indicator:
  https://www.aaii.com/journal/article/measuring-internal-strength-wilder-s-rsi-indicator

### Bollinger Bands, and what "the middle of the band" means

The video draws a Bollinger pair as an envelope around a central line and describes the
middle of that band as one of the reference points a mean reversion trader can use.

Bollinger Bands were developed by John Bollinger in the early 1980s. The standard setting,
and the one the video draws, is a 20 period simple moving average with the outer bands at
plus and minus two standard deviations, so the middle band is that moving average.

- Fidelity, Bollinger Bands, technical indicator guide:
  https://www.fidelity.com/learning-center/trading-investing/technical-analysis/technical-indicator-guide/bollinger-bands
- StockCharts ChartSchool, Bollinger Bands:
  https://chartschool.stockcharts.com/table-of-contents/technical-indicators-and-overlays/technical-overlays/bollinger-bands

Bollinger Bands is a registered trademark of John Bollinger.

### Volume weighted average price

The video lists VWAP as one of the reference points price can be measured against and can
revert toward, and draws it as a line through the bars rather than as a horizontal level.

VWAP is the average price over a period weighted by volume traded at each price, which is
why it is drawn as a line that moves rather than as a fixed level.

- Interactive Brokers Traders' Academy, VWAP:
  https://www.interactivebrokers.com/campus/trading-lessons/vwap/


## The claims the video makes about how markets behave

### That trends can persist for longer than people expect

The video's opening argument for trend following is that a market can keep moving in one
direction well past the point where someone would have called the top, and it draws a series
that runs past a marked "where you would have called it" level.

This is the momentum effect, and it is one of the most replicated results in the literature.
Jegadeesh and Titman (1993) documented that buying past winners and selling past losers
produced significant positive returns over three to twelve month holding periods, and that
this was not explained by systematic risk.

- Jegadeesh, N. and Titman, S. (1993), Returns to Buying Winners and Selling Losers:
  Implications for Stock Market Efficiency, *The Journal of Finance* 48(1), 65 to 91:
  https://onlinelibrary.wiley.com/doi/abs/10.1111/j.1540-6261.1993.tb04702.x
- Full text: https://www.bauer.uh.edu/rsusmel/phd/jegadeesh-titman93.pdf

The persistence itself has been shown across markets and across a very long history.

- Hurst, B., Ooi, Y. H. and Pedersen, L. H., A Century of Evidence on Trend Following
  Investing (AQR), which studies trend following across global markets back to 1880:
  https://www.aqr.com/Insights/Research/Journal-Article/A-Century-of-Evidence-on-Trend-Following-Investing

### That a trend following payoff can be many small losses and occasional very large gains

The video draws a run of small losses followed by one much larger winner, and says some
professional trend following systems are designed around exactly that shape.

That shape is the positive skewness trend following is documented to have: the return
distribution has a long right tail rather than a symmetric spread, which is the same
statement as "lots of small losses, occasionally a very large move".

- A Century of Evidence on Trend Following Investing (as above), on the return profile and
  its behaviour across the largest drawdowns of the last century:
  https://www.aqr.com/Insights/Research/Journal-Article/A-Century-of-Evidence-on-Trend-Following-Investing
- Hoffman, A. and Kaminski, K., Taming of the Skew, on the positive skewness of trend
  following and how it behaves in a portfolio:
  https://www.returnstacked.com/managed-futures-trend-following/

The specific run drawn on screen, seven small losses and one winner many times their size,
is an invented illustration of that shape and not a measured result.

### That orders concentrate at obvious levels, and that price can move quickly once they go

This is the mechanism underneath the whole liquidity sweep section, and underneath the
video's claim that stop losses sit above an obvious high and below an obvious low.

Osler (2003) examined a large sample of currency orders and found that take profit orders
cluster at round numbers while stop loss orders cluster just beyond them, and used that
clustering to explain why price tends to reverse at levels that are visible on a chart and to
move unusually quickly once it has passed through them. Osler's later work follows the second
half of that specifically: stop loss orders triggering in sequence and producing price
cascades.

- Osler, C. L. (2003), Currency Orders and Exchange Rate Dynamics: An Explanation for the
  Predictive Success of Technical Analysis, *The Journal of Finance* 58(5), 1791 to 1819:
  https://onlinelibrary.wiley.com/doi/abs/10.1111/1540-6261.00588
- Federal Reserve Bank of New York Staff Report 125, the working paper version:
  https://www.newyorkfed.org/medialibrary/media/research/staff_reports/sr125.pdf
- Osler, C. L. (2005), Stop Loss Orders and Price Cascades in Currency Markets, *Journal of
  International Money and Finance* 24(2), 219 to 241:
  https://faculty.georgetown.edu/evansm1/New%20Micro/osler1.pdf

Two limits on this, both of which the video states out loud rather than leaving implied. The
evidence is from currency markets, and whether it carries over unchanged to every instrument
is not something this video tested. And the video says explicitly that a retail chart cannot
show where orders actually are, that what is being done is an inference from levels that are
obvious, and it draws that inference as a soft probability cloud rather than as a mark on a
specific candle.

### That a win rate on its own does not tell you whether a strategy makes money

The video works through two invented strategies to make this point, and the arithmetic is the
argument rather than the evidence, so it is checked here rather than sourced.

Strategy A wins 80 out of 100, each winner makes one unit, each loser costs five. That is
`80 × 1 − 20 × 5 = 0`, before any cost at all, which is why the video draws its equity line
finishing below where it started once anything is deducted.

Strategy B wins 40 out of 100, each winner makes three units, each loser costs one. That is
`40 × 3 − 60 × 1 = +60`, from a strategy that loses more trades than it wins.

Both sets of numbers are the script's own invention, chosen because they make the point
cleanly. Neither describes a real system.


## Everything on screen that is a number, and what it is

Every one of these is a teaching example from the script, drawn on generated price. None is a
measurement.

| On screen | What it is |
| --- | --- |
| 100, 110, 106 | The trend following pullback example: price runs from 100 to 110 and pulls back to 106 |
| 50 MA | The moving average variant of a trend entry |
| 20 MA | The reference average in the mean reversion section |
| 100, 98, 99, 90 | The two ways price can approach a level: falling all the way back to 90, or compressing at 98 then 99 |
| Down 10%, down 10%, down 15% | The earnings example, three legs down while it keeps looking oversold |
| Win rate 80%, winner 1 unit, loser 5 units | Strategy A, invented |
| Win rate 40%, winner 3 units, loser 1 unit | Strategy B, invented |
| 90% win rate | The unevidenced social media claim the video weighs against a tested result |
| Zones drawn, chart covered, touches, rejections | Counters over generated charts, illustrating a mechanism |

The instruments, timeframes and markets shown in the testing grid near the end are labels on
an empty grid: the video uses them to say what a person would have to test, and does not
report a result for any cell.
