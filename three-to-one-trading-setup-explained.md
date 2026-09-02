---
layout: default
title: "The 3:1 Setup Is Not What Most Traders Really Think"
permalink: /three-to-one-trading-setup-explained/
date: 2026-09-02
---

# The 3:1 Setup Is Not What Most Traders Really Think

{% raw %}
Every figure this video puts on screen, and where it comes from.

The video makes two kinds of numerical claim and they are sourced differently.

**Arithmetic** is derived rather than cited. A break even win rate, an expectancy and a
hundred trade total are all consequences of the definitions the video states out loud, so
the honest source is the derivation, and it is written out below. A citation to somebody
else repeating the same sum would be weaker, not stronger.

**Everything else on screen is invented, and is labelled as such in the frame.** No price
series in this video is real, no account curve is real, and no order book is real. They are
there to show a mechanism, and each carries a `Source:` line saying so. Nothing in this
video asserts that a particular thing happened in a particular market, and there is no
claim anywhere about how often any real strategy wins.

---

## The ratio, and what breaks even

**A 3:1 setup breaks even at 25 percent before costs.**

If a winning trade returns `R` times the amount risked and a loser costs one unit, then
over `n` trades at a win rate `w` the account changes by

```
n * ( w * R  -  (1 - w) * 1 )
```

which is zero when `w * R = 1 - w`, that is when

```
w = 1 / (1 + R)
```

Evaluated at the three payoffs the video names:

| Payoff | Break even win rate |
| --- | --- |
| 1 to 1 | 50 percent |
| 2 to 1 | 33.3 percent |
| 3 to 1 | 25 percent |

Those are the three figures on the payoff stacks and the marked point on the break even
curve. The curve on screen is `1 / (1 + R)` plotted directly.

**The money version.** Risking 100 to make 300 across 100 trades at the break even rate:

```
25 wins   x 300 = 7,500
75 losses x 100 = 7,500
```

Flat before costs, which is what the two bars of equal length in that shot are showing.
After costs it is negative, because every trade pays a spread and a commission and those
are subtracted from both sides.

**The 20 percent case.** The same 3:1 targets at a 20 percent win rate:

```
20 wins   x 3R = 60R
80 losses x 1R = 80R
```

A loss of 20R over 100 trades, before costs. That is the account line in the intro and in
chapter two, and its end value is computed from the run of outcomes the shot draws rather
than typed in.

**Expectancy.** What one average trade produces, in R:

```
E = w * R - (1 - w)
```

At 3:1 and a 25 percent win rate, `E = 0`. At 35 percent, `E = 0.35 * 3 - 0.65 = 0.40R`
per trade. At 20 percent the same sum is `0.20 * 3 - 0.80`, a fifth of an R lost per trade.
Those are the figures on the expectancy readout and the two dials.

**The worked example.** Entry 100, stop 98, target 106. Risk is 2 points, reward is 6
points, so the ratio is 3 to 1. Risking 100 dollars with a 10 point stop puts the target 30
points away for the same reason.

## How often a target that far away is reached

The falling curve in chapter two is not an invented decay. It is the classic gambler's ruin
result for a fair game: starting from stake `z`, with ruin at 0 and a target at `M`, the
probability of reaching `M` before 0 is `z / M`.

> Grinstead and Snell, *Introductory Probability*, section 12.2, Gambler's Ruin.
> https://stats.libretexts.org/Bookshelves/Probability_Theory/Introductory_Probability_(Grinstead_and_Snell)/12:_Random_Walks/12.02:_Gambler's_Ruin

A trade with its stop 1R below the entry and its target `R` above is that game with
`z = 1` and `M = 1 + R`, so with no edge and no costs the chance of the target landing
first is

```
1 / (1 + R)
```

At 3:1 that is 25 percent, which is exactly the break even win rate above. The two are the
same expression, and that is the point: a 3:1 setup with no edge behind it wins precisely
often enough to finish flat, and then loses to costs. It is why the video argues that the
ratio judges a trade idea rather than replacing one.

This is also what the video means by a target three times further away being harder to hit.
Under the same model a target 0.6R away is reached first 62.5 percent of the time, and a
target 4R away 20 percent of the time.

## The planned and realised figures

The 1.7R average winner and the 1.1R average loser are the figures the script states, and
the journal shots are built from them: a single seeded run of outcomes at a fixed win rate,
with each outcome rendered at the planned pair and again at the realised pair. The tape,
the two average rules and the gap measured between them all come from that one run.

**These illustrate a gap rather than measure one.** No trader's log was examined and no
population of trades was sampled. The shots carry
`Source: simulated, one run of outcomes at the stated averages`.

## What is on screen and is invented

All of the following are drawn to show a mechanism and are labelled in frame:

- Every price series. Generated from a seeded model with a stated drift and volatility, so
  the same chart is reproducible, and carrying
  `Source: illustrative price data, drawn to show the mechanism`.
- Every account curve, from a stated win rate and payoff, labelled with both.
- The depth ladder and its resting sizes.
- The touch counts in the near and far target comparison. The number printed under each
  pane is counted off the bars actually drawn in that pane, so the two panes cannot
  disagree with their own charts, but the bars themselves are invented.
- The levels, zones and swing points on every chart. Each is measured off its own series
  with the same high and low search the shots use, rather than positioned by eye.

## Marks

Two real marks appear. The charting platform's own mark is shown on the two beats about a
drawing tool and about a screenshot, because that is what those lines are describing. A row
of market marks appears once, under the claim that the same three chart shapes turn up
whatever is being traded. Both are the published geometry from the simple-icons project.
No mark is drawn against invented price data, and no instrument is named on any chart in
this video.

## Not checked

- That the three named situations, a trend pullback, a breakout retest and a failed move,
  are where a 3:1 shape most often appears cleanly. This is the script's editorial
  judgement about chart structure rather than a measured frequency, and no study is cited
  for it. The shots illustrate what each situation looks like; they do not assert how often
  it occurs or how often it works.
- That a breakout candle is often late. Stated as general market experience in the script,
  not as a measured statistic, and the shot shows only the distance between the level and
  the close of that bar.
- That trapped traders' exits help fuel the move against them. A widely described
  mechanism, but no order flow data is cited and none is shown.
- The costs figure used in the after costs account curve. A fixed fraction of R is
  subtracted per trade to show the direction of the effect. It is not a spread, commission
  or slippage measurement for any real instrument or venue.
{% endraw %}
