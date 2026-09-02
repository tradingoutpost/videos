---
layout: default
title: "The Perfect Pullback Entry Is Later Than You Think"
permalink: /perfect-pullback-entry/
date: 2026-09-02
---

# The Perfect Pullback Entry Is Later Than You Think

{% raw %}
Every figure, level and percentage this video puts on screen, and where it comes from.

## What the charts are

**Every chart in this video is invented price, and every shot that shows one says so.**
The credit in the bottom left of the frame reads `Source: illustrative price, invented to
show the mechanism`, and that is the literal truth: the bars are generated from a declared
sequence of legs with seeded noise, not taken from any market.

That is the legitimate use of invented data. The video is teaching a mechanism, and a real
window of a real instrument carries a hundred irrelevant things while rarely containing
exactly the case a beat needs. What invented data may never do is stand in for evidence:
nothing here asserts that a particular move happened, that a method wins at some rate, or
that any instrument did anything. There is no backtest, no win rate, no equity curve and no
performance claim anywhere in the video, spoken or drawn.

Each series is deterministic and can be regenerated exactly:

| Series | Used for | Seed | Structure |
| --- | --- | --- | --- |
| `MAIN` | the spine: three impulses, three pullbacks | 23 | seven declared legs |
| `CRISP` | a trend that still has authority | 17 | five legs, low bar overlap |
| `SLOPPY` | an uptrend that has stopped being worth trading | 41 | five legs, high bar overlap |
| `FLUSH` | the touch, the flush and the reclaim | 5 | seven legs |
| `BREAKDOWN` | the pullback that keeps going | 61 | four legs |
| `DOWN` | the downtrend everything is flipped into | 33 | five legs |

## Every number on screen

All of them are arithmetic on the series above, computed in the shot rather than typed, so
a change to a series moves the figure with it. None is a claim about a market.

| Figure | Beats | How it is computed |
| --- | --- | --- |
| Price axis values | every chart | the series' own values, at the visible window |
| Retracement percentages | 24, 26, 28, 29 | `(legHigh − pullbackLow) / (legHigh − legLow)` |
| `5.3% off` | 6 | the pullback low against the prior swing high |
| `% against` on an open trade | 5 | the current close against the entry price |
| `% of the stop left` | 20 | the distance from price to the stop, over the entry to stop distance |
| Stop distances `0.32% / 1.08% / 3.44%` | 59 | each candidate stop against the entry, as a percentage |
| Ordinary bar noise band | 60 | the mean high to low range of the bars across the pullback |
| Reward multiple `0.7R` | 64 | `(obstacle − entry) / (entry − stop)` |
| Dial readings | 23, 25, 63 | positions on a stated 0 to 100 scale, not measurements of anything |

## Position sizing, in beat 61

The two order tickets show the same money at risk producing two different position sizes,
which is arithmetic rather than a claim:

    size = risk allowed / (stop distance as a fraction of entry)

At 200 risked and a 0.9% stop that is 22,222. At 200 risked and a 2.4% stop it is 8,333.
Both are printed by the shot from those two inputs. The relation is the definition of
fixed fractional position sizing and it holds for any instrument and any currency, which is
why no currency symbol appears on screen.

## The concepts the video names

These are established technical analysis definitions rather than findings, and they are
cited so a viewer can go to the source rather than take the video's word for it.

- **A level's role reverses once it is broken.** Old support becoming resistance, and the
  reverse, is Edwards and Magee's principle of polarity, set out in *Technical Analysis of
  Stock Trends* (first published 1948). Beats 36 and 47 draw it.
  <https://www.taylorfrancis.com/books/mono/10.4324/9781315115719/technical-analysis-stock-trends-robert-edwards-john-magee-bassetti>

- **The Fibonacci retracement levels drawn in beat 2** are 23.6%, 38.2%, 50%, 61.8% and
  78.6%, which is the standard set charting packages draw. 23.6, 38.2 and 61.8 come from
  ratios within the Fibonacci sequence. **50% is not a Fibonacci ratio**; it is included by
  convention, from the Dow Theory observation that averages often retrace about half of a
  prior move. The video draws the set as traders have it, and refuses it as a reason to
  enter rather than endorsing it.
  <https://chartschool.stockcharts.com/table-of-contents/chart-analysis/chart-annotation-tools/fibonacci-retracements>

- **Higher highs and higher lows as the definition of an uptrend**, used in beats 16 and 17,
  is Dow Theory's trend definition, and the video's whole argument is that satisfying it is
  not by itself a reason to enter.

## Not checked

- The video's central claim is a judgement about how to trade, not a measurable fact, and
  it is not presented as one. It asserts no success rate, no edge and no expectancy, and
  nothing in the script or the picture could be verified against market data because
  nothing in either is a statement about market data.
- The trend quality dial readings in beats 23, 25 and 63 are positions on an invented
  scale used to show one chart reading better than another. There is no standard measure
  of trend quality and none is implied.
- "Ordinary bar noise" in beat 60 is the mean bar range of that invented series. It is a
  way of showing that a stop can sit inside normal movement, not a threshold anyone should
  carry to a real chart.
{% endraw %}
