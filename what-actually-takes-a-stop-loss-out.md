---
layout: default
title: "What Actually Takes A Stop Loss Out"
permalink: /what-actually-takes-a-stop-loss-out/
date: 2026-08-04
---

# What Actually Takes A Stop Loss Out

Every figure and every claim this video puts on screen, with where it comes from.

Three kinds of thing appear here and they are labelled on screen as well as in this file,
because the difference matters more than any individual number:

- **Sourced.** A statement about how orders, indicators or markets actually work, taken
  from the body that defines it.
- **Illustrative.** Invented price, used to teach a mechanism. Nothing illustrative asserts
  that anything happened in a real market.
- **Simulated.** The output of a stated model, run to show a mathematical property. The
  model is named on screen beside its result.


## What a stop order is, and what it is not

**A stop order becomes a market order when the stop price is reached.** Stated by the SEC's
Office of Investor Education and Advocacy: "When the stop price is reached, a stop order
becomes a market order."

**The stop price is not the execution price.** Same source: "The stop price is not the
guaranteed execution price for a stop order. The stop price is a trigger that causes the
stop order to become a market order. The execution price an investor receives for this
market order can deviate significantly from the stop price in a fast-moving market where
prices change rapidly."

**A stop limit order can fail to fill.** Same source: a stop limit order "becomes a limit
order that will be executed at a specified price (or better)", and "may not be executed if
the stock's price moves away from the specified limit price, which may occur in a
fast-moving market."

Source: SEC Office of Investor Education and Advocacy, *Investor Bulletin: Stop, Stop-Limit,
and Trailing Stop Orders*.
https://www.investor.gov/introduction-investing/general-resources/news-alerts/alerts-bulletins/investor-bulletins-15

The gap between the level and the fill drawn on screen, six pips, and the seventeen pips it
widens to as the book thins, are illustrative. They show the direction of the relationship,
not a measured slippage figure for any instrument.


## True range and average true range

Both were introduced by J. Welles Wilder Jr. in *New Concepts in Technical Trading Systems*
(Trend Research, 1978), which is where every definition used on screen comes from.

**True range is the greatest of three measurements:** the current high minus the current
low; the absolute value of the current high minus the previous close; and the absolute value
of the current low minus the previous close.

**Why the previous close is in there.** A bar's own high minus low measures movement inside
that bar only. When a market opens away from where it closed, the distance price actually
travelled starts at the previous close, and the bar's own range understates it. True range
was defined to capture that, so a gap or a limit move is measured rather than ignored.

**Average true range smooths it.** Wilder's smoothing over a fourteen period lookback is the
previous ATR multiplied by thirteen, plus the current true range, all divided by fourteen.
The first value has no previous ATR to work from, so it is seeded with the arithmetic mean of
the first fourteen true ranges.

**ATR as a share of price.** Dividing ATR by the current price turns a distance into a
percentage, which is the only form in which the same figure can be compared across
instruments quoted on completely different scales.

Sources: Wilder, *New Concepts in Technical Trading Systems*, 1978.
https://books.google.com/books/about/New_Concepts_in_Technical_Trading_System.html?id=WesJAQAAMAAJ
Formula and seeding as documented at https://www.macroption.com/atr-calculation/ and
https://www.macroption.com/true-range/

The ATR percentages shown for the four instruments, 1.90% for a stock, 0.88% for an index,
0.49% for an FX pair and 3.67% for a crypto asset, are **illustrative**. They come from
generated series chosen to sit in plausible ranges for those four asset classes, and they
are on screen to show that one fixed distance means four different things. They are not the
current ATR of any named instrument.



## The chart the video follows

The chart used throughout, an FX pair basing at 1.1013, a stop typed at the round number
1.1000, a wick to 1.0995 and the move afterwards, is **illustrative**. It is built so the
geometry the video is about is exactly visible: an entry at 1.1038, one ATR of 54 pips, a
stop 38 pips away which is 0.70 ATR, and a low that reaches 0.79 ATR below the entry.

Every one of those relationships is arithmetic on the invented prices, and each is drawn
from the same numbers rather than typed on separately. No claim is made that any market did
this.

The buffered stop the video builds, half an ATR below the level at 1.0986, is 52 pips from
the entry, which is 0.96 ATR. That it survives the low while the round number stop does not
is a property of the chart as drawn.


## The measurement

The only non-illustrative numbers in the video come from a stated model, labelled
**simulated** on screen while its result is shown.

**The model.** A zero drift random walk. Ten bars, three sub steps in each bar so a level
can be touched inside a bar rather than only at a close, two thousand independent paths. No
trend, no news, no edge in either direction.

**Distances are quoted in ATR of the walk itself.** The bars the walk produces have their
own true range, and the mean of those true ranges is what one ATR means inside the model.
Quoting distances that way makes the result scale free: the per step volatility cancels, so
the answer is a property of the model rather than of a volatility number chosen to produce
it.

**The result.** A stop is counted as taken out if the path reaches it at any point in the
ten bars.

| Stop distance | Share of runs stopped out |
| --- | --- |
| 0.25 ATR | 84.4% |
| 0.5 ATR | 78.3% |
| 1.0 ATR | 66.3% |
| 2.0 ATR | 45.5% |
| 3.0 ATR | 26.2% |

Every one of those exits happens with no direction in the market at all, which is the entire
point of running it with zero drift.

**What this does and does not say.** It says that a stop placed inside the distance an
instrument covers anyway is reached most of the time by ordinary movement, and that moving
it further out reduces that sharply. It does not say what happens in a real market, it does
not measure any instrument, and the numbers move with the horizon: ten bars is the holding
period the model was run over, and a longer one raises every figure in the table.


## Position sizing

The relationship shown, risk divided by stop distance equals position size, is arithmetic
rather than a claim, and it holds by definition: the money at risk is the position size
multiplied by the distance to the stop, so fixing the first and choosing the second
determines the third.

The worked example, a 10,000 account risking one per cent, which is 100, over a 52 pip stop
giving 19,196 units, is **illustrative** in its inputs and exact in its arithmetic. Doubling
the stop distance to 104 pips halves the size to 9,598 and leaves the money at risk at 100.


## When the market is shut

**Stocks and indices.** The NYSE core trading session runs 09:30 to 16:00 Eastern Time,
Monday to Friday, with the exchange closed on listed holidays. Price can move between a
close and the next open with no book in between.
Source: https://www.nyse.com/markets/hours-calendars

**Forex.** The interbank week runs continuously from Sunday evening to Friday evening and is
closed over the weekend. CME's FX contracts trade Sunday 17:00 through Friday 16:00 Central
Time with a daily break.
Source: https://www.cmegroup.com/trading-hours.html

**Crypto.** Spot venues operate continuously, with no daily open or close and no weekend.
Source: https://www.coinbase.com/blog/24-7-futures-trading-has-arrived

The weekend gap drawn on screen, a market reopening 54 pips below a stop level, is
**illustrative**. It shows what a gap does to a resting order rather than reporting a
particular weekend.


## Caveats worth stating

- The simulation is a random walk. Real price is not one, and the result is a statement
  about the model rather than about any market.
- One ATR is a backward looking average. It describes the range the market has been
  covering, and it widens only after volatility has already expanded, which the video shows
  rather than glosses over.
- The four instrument percentages are plausible rather than measured, and the real figure
  for any instrument changes daily.
- Slippage figures shown are illustrative; actual slippage depends on the venue, the
  instrument, the size and the moment.
- Nothing here is a recommendation to buy or sell anything, and no entry, exit or stop
  placement shown is a signal.
