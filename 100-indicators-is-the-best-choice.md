---
layout: default
title: "Your Chart Needs 100 Indicators Or It Is Guessing"
permalink: /100-indicators-is-the-best-choice/
date: 2026-08-21
---

# Your Chart Needs 100 Indicators Or It Is Guessing

{% raw %}
Everything the video states as fact, chased to a source. The video's central claim, that
ninety nine indicators is a professional minimum and the hundredth is a safety measure, is
an argument made to expose a habit rather than a figure taken from anywhere, and it is
listed at the bottom under **Claims with no source** rather than dressed up as one.

## The tools the video names

Every indicator the video lists is a real, published tool with a named author and a
definition. Where the video says what one of them measures, that is what its author
defined it to measure.

| Tool | Author | First published | What it measures |
| --- | --- | --- | --- |
| Relative Strength Index | J. Welles Wilder Jr. | *New Concepts in Technical Trading Systems*, Trend Research, 1978 | The ratio of average up closes to average down closes over a lookback, scaled 0 to 100 |
| Average True Range | J. Welles Wilder Jr. | Same volume, 1978 | Average of the true range, which is the greatest of high minus low, high minus previous close, and previous close minus low |
| Average Directional Index and Directional Movement | J. Welles Wilder Jr. | Same volume, 1978 | Trend strength, without direction |
| Parabolic SAR | J. Welles Wilder Jr. | Same volume, 1978 | A trailing stop and reverse level |
| Moving Average Convergence Divergence | Gerald Appel | 1970s | The distance between a fast and a slow exponential moving average, against a signal line |
| Stochastic Oscillator | George C. Lane | 1950s | Where the close sits inside the high to low range of a lookback |
| Williams %R | Larry Williams | not separately dated | Where the close sits below the highest high of a lookback, scaled 0 to −100 |
| Commodity Channel Index | Donald Lambert | *Commodities* magazine, October 1980 | How far price sits from its own statistical mean, in mean deviations |
| Bollinger Bands | John Bollinger | Early 1980s | A moving average with bands set a number of standard deviations away, so the width adapts to volatility |

Sources: Wilder's 1978 volume is catalogued at the
[Internet Archive](https://archive.org/details/newconceptsintec00wild) and in
[Google Books](https://books.google.com/books/about/New_Concepts_in_Technical_Trading_System.html?id=WesJAQAAMAAJ);
Gerald Appel's authorship of MACD is recorded by the
[CMT Association](https://cmtassociation.org/presenter/gerald-appel/); John Bollinger's
development of the bands in the early 1980s, and the use of standard deviation to make the
bands adaptive, is recorded at [Bollinger Bands](https://en.wikipedia.org/wiki/Bollinger_Bands)
and [John Bollinger](https://en.wikipedia.org/wiki/John_Bollinger); the October 1980
*Commodities* publication of the Commodity Channel Index and George Lane's 1950s
Stochastic are recorded at
[CSI's indicator reference](https://www.csidata.com/?page_id=4477).

## Stochastic and Williams %R point at the same thing

The video says stochastic and Williams percent range can point to similar conditions. They
are the same calculation with the reference end of the range swapped and the result scaled
by −100, so plotted together one is the other inverted:

```
%K  = (Close − Lowest Low)  / (Highest High − Lowest Low) ×  100
%R  = (Highest High − Close) / (Highest High − Lowest Low) × −100
```

StockCharts states the relationship directly: the Fast Stochastic Oscillator and Williams
%R "produce the exact same lines, but with different scaling", %R correcting for the
inversion by multiplying by −100.

Source: [Williams %R, StockCharts ChartSchool](https://chartschool.stockcharts.com/table-of-contents/technical-indicators-and-overlays/technical-indicators/williams-r).

## MACD and RSI both describe momentum

Both are computed only from the closing price series: RSI from the average of up closes
against down closes, MACD from the difference between two exponential moving averages of
the close. Neither reads any input the other cannot see, which is the basis for the
video's point that several momentum tools can repeat one message. Both definitions are in
the author sources above.

## Indicators built from the same data can only repeat it

The video's claim that several indicators may be "repeating the same message with
different costumes" follows from the definitions rather than from any study: RSI,
stochastic, MACD, CCI and rate of change are each a function of the same OHLC series, so
none of them can introduce information the price series does not already contain. That is
a statement about what the formulas take as input, and the inputs are given in the author
sources above.

## A twenty and a twenty one period moving average

The video says these two may not be totally different life forms. Both are moving averages
of the same closes over lookbacks differing by one bar, so their outputs differ only by the
weight given to a single additional observation. This follows from the definition of a
moving average rather than from a source.

## Redundancy is standard engineering practice

The video's comparison to aviation and hospitals is accurate.

**Aircraft.** Transport category aeroplanes are certificated against 14 CFR § 25.1309,
which requires that systems be designed so that no single failure prevents continued safe
flight and landing, and the FAA's Advisory Circular AC 25.1309-1B sets out the accepted
means of showing it. Fly-by-wire transport aircraft commonly carry triple redundancy
across computing, electrical power, hydraulic power and communication.

Sources: [14 CFR § 25.1309, eCFR](https://www.ecfr.gov/current/title-14/chapter-I/subchapter-C/part-25/subpart-F/subject-group-ECFR9f24bf451b0d2b1/section-25.1309),
[AC 25.1309-1B, FAA](https://www.faa.gov/documentLibrary/media/Advisory_Circular/AC_25.1309-1B.pdf).

**Hospitals.** Backup generation is not optional. NFPA 99, the Health Care Facilities
Code, and NFPA 110, the Standard for Emergency and Standby Power Systems, together require
a hospital's Essential Electrical System to be supplied by emergency power, with hospitals
typically classified Level 1, Type 10, meaning acceptable power to critical loads within
ten seconds of a utility failure.

Sources: [NFPA 99 and NFPA 110 hospital generator requirements](https://backuppower.ai/healthcare/hospital-generator-requirements/),
[NFPA 110 requirements for healthcare facilities](https://www.nixonpower.com/blogs/news/nfpa-110-generator-requirements-for-data-centers-and-hospitals).

The video's own point is that this comparison is where the analogy breaks: a backup
generator is an independent source of power, whereas a second momentum oscillator is
another reading of the same price series.

## Claims with no source

These are the video's argument, not findings, and none of them is presented here as fact.

- **"The minimum serious number is ninety nine."** There is no professional standard,
  body, study or convention that sets a minimum number of indicators. The figure is the
  video's device.
- **"The hundredth indicator is a safety measure."** Same. No source, and none implied.
- **"Ninety eight leaves room for amateurism."** Same.
- **"If your chart does not take at least eight seconds to load, you are basically
  guessing."** Load time has no established relationship to anything about a strategy.
- **Alpha Oracle Matrix, Smart Flow Reactor, Quantum Liquidity Compass and Institutional
  Candle Imbalance Engine.** Invented names, used to describe a category of closed source
  tools rather than to name any real product.
- **Fisher transform, wave trend, squeeze tools, delta and cumulative delta.** Real
  categories of tool that exist in many platform specific versions with no single
  canonical published definition, so no author is credited for them above.
- **"Most traders lose because they overtrade."** Widely repeated and plausible, but the
  video states it without a study behind it and no primary source was found that
  establishes it as a general fact.

## What is actually being taught

The material claim the video makes in its own voice, and the only one it asks the viewer
to act on, is that indicators are useful when they answer different questions, and become
misleading when several of them answer the same question and the repetition is mistaken
for independent evidence. That follows from the definitions above rather than from a
study, and the video says so.
{% endraw %}
