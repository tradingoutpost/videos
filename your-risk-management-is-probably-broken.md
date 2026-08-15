---
layout: default
title: "Your Risk Management Is Probably Broken"
permalink: /your-risk-management-is-probably-broken/
date: 2026-08-15
---

# Your Risk Management Is Probably Broken

{% raw %}
Every figure this video puts on screen, and where it comes from.

Two kinds of number appear, and they are not the same kind of claim. **Arithmetic** is what
a fixed fractional stake does to an account over a run of losses, and what it then takes to
get back; it is exact and true of any account. **Simulated** is drawn from a model that is
named on screen wherever its output appears, because in those cases the model is the
argument rather than a decoration.

Nothing here asserts that anything happened. There is no win rate taken from a real
account, no backtest and no equity curve belonging to a real trader.


## What a run of losses costs, by stake size

Risking a fixed fraction `r` of the current account on each trade, `n` consecutive losses
leave `(1 - r)^n` of the account, so the drawdown is `1 - (1 - r)^n`. Getting back to flat
from a drawdown `d` needs a gain of `1 / (1 - d) - 1` on the reduced account, which is why
the recovery grows faster than the loss that caused it.

Ten consecutive losses:

| Risk per trade | Account left | Drawdown | Gain needed to get back |
| --- | --- | --- | --- |
| 0.5% | 95.1% | 4.9% | +5.1% |
| 1% | 90.4% | 9.6% | +10.6% |
| 2% | 81.7% | 18.3% | +22.4% |
| 5% | 59.9% | 40.1% | +67.0% |

The same asymmetry is what stands behind the depth figures: an account down 50% needs to
double to get back, and one down 75% needs to quadruple.

Ten trades in a single session at 1% each, all losing, is the same calculation and comes to
9.6%, which is the figure shown against the day rather than against the trade.

This is arithmetic rather than a finding, and it holds whatever the instrument, the market
or the strategy. The compounding convention used throughout is that the stake is a fraction
of the account as it stands at that trade, not of the starting balance.


## How long a losing streak is normal

Two results are used, both standard and both long predating any trading application.

**The chance of seeing a run at all.** For independent trades with win probability `p`, the
probability that a sequence of `n` trades contains no run of `k` consecutive losses follows
the classical recurrence for success runs, set out in Feller, *An Introduction to
Probability Theory and Its Applications*, Volume 1, 3rd edition (Wiley, 1968), chapter XIII
on recurrent events and success runs. Taking the complement gives the probability of at
least one such streak.

Over 200 trades at a 45% win rate:

| Losing streak | Chance of seeing at least one |
| --- | --- |
| 5 in a row | 99.4% |
| 8 in a row | 53.0% |
| 10 in a row | 19.9% |
| 12 in a row | 6.4% |

**The length to expect.** The expected longest run of losses in `n` trades is
approximately `log(n·p) / log(1/(1-p))`, the same result as the expected longest run of
heads in a coin sequence, given in Schilling, "The Longest Run of Heads", *The College
Mathematics Journal*, Volume 21, Number 3 (May 1990), pages 196 to 207. At a 45% win rate
over 200 trades this comes to 7.5, which is the line drawn across the chart.

So a strategy that wins 45% of the time and is genuinely profitable will still, more often
than not, hand its owner an eight trade losing streak inside 200 trades. That is the sense
in which the video calls losing streaks mathematically normal rather than rare.

Both figures assume trades are independent of each other. Real trades taken in the same
market on the same day are not, and correlation makes clustering worse rather than better,
so these are the optimistic version.


## Expectancy of the example strategy

The worked example uses a strategy that wins 45% of the time with winners twice the size of
losers. Expectancy per trade is `0.45 × 2R − 0.55 × 1R = +0.35R`. That is what makes it a
strategy worth running, and it is why both traders in the example are trading the same
edge. The number is arithmetic from the two figures stated on screen.


## The two traders

Both traders receive the identical sequence of 200 signals and the identical edge above.
Only the risk process differs, and the model is named on screen where its output appears:

- Trader one risks a flat 0.5% of the current account and stops for the rest of the session
  once three of that session's trades have lost.
- Trader two risks 0.5%, 2% or 5% depending on how the setup feels, doubles the next stake
  after a loss up to a 10% ceiling, and has no session stop.

Run 5,000 times, the worst drawdown each trader goes through:

| | Median worst drawdown | Deepest seen | Chance of a drawdown past 50% |
| --- | --- | --- | --- |
| Trader one | 4.0% | 13.1% | 0% |
| Trader two | 52.3% | 97.1% | 57.4% |

The pair drawn on screen is the run whose two drawdowns both land closest to their own
medians, so neither curve is a best or a worst case.

**What the chart deliberately does not show, and why.** It plots how far below its own high
water mark each account is, not what each account finished at. Both traders are running the
same positive edge, and trader two is staking below the fraction that would maximise
long run growth for that edge, so over 200 trades trader two usually ends up with more money
despite the far deeper holes. The growth optimal fraction for a 45% chance of a 2 to 1
payoff is 17.5%, from the criterion in Kelly, "A New Interpretation of Information Rate",
*Bell System Technical Journal*, Volume 35, Number 4 (July 1956), pages 917 to 926.

That is a real limit on how far the example can be pushed. What the model does support, and
what the chart shows, is that the risk process decides the depth of the hole rather than
the size of the edge: trader two sits past a 50% drawdown more often than not, and a
drawdown is where a trader quits, moves the stops, or abandons the system. What it does not
support is a claim that erratic sizing loses money on average against a positive edge.
See the caveats below.


## Correlated positions

The three semiconductor names shown are drawn with their own published marks and no
correlation figure is put on screen, because the point being made is structural rather than
numerical: three positions that depend on the same underlying move are one position for the
purpose of risk, and counting them as three separate 1% risks understates the exposure by
roughly three times. The arithmetic shown is the 3 × 1% combining into 3%.


## Not chased to a primary source

- The claim that erratic position sizing leads to blowing up. On the model above it leads
  to far deeper drawdowns, not to a lower expected account: the deepest quarter of runs is
  brutal and 6.3% of them go past a 75% drawdown, but a positive edge staked under the
  growth optimal fraction still tends to grow. The stronger version of the claim depends on
  the other behaviours described alongside it, taking correlated trades unknowingly and
  continuing to trade while frustrated, which degrade the edge itself rather than only the
  sizing. That degradation is plausible and is not modelled here, so it is not evidenced.
- The position sizes attached to an average setup and an amazing setup, and the sizes on
  each rung of the ladder. These are illustrative and are marked as such on screen; no
  survey of what traders actually do was used.
- That most traders equate risk management with using a stop loss. It is the premise the
  video opens on and no survey is cited for it.
- The specific behaviours named as signals of oversized risk, staring at the chart, moving
  stops, closing winners early, revenge trading and increasing size when angry. These are
  presented as things to watch for rather than as measured effects, and no study is cited.
- Whether a trader stops trading at any particular drawdown depth. The marker on the
  underwater chart is illustrative of the idea rather than a measured threshold.
{% endraw %}
