---
layout: default
title: "The RSI Mistake That Makes Traders Fight The Trend"
permalink: /use-rsi-indicators-like-a-pro/
date: 2026-08-30
---

# The RSI Mistake That Makes Traders Fight The Trend

{% raw %}
Every figure, level, date and definition the video states, chased to a source.

## Where RSI comes from

**The relative strength index was developed by J. Welles Wilder and published in 1978.**
Wilder set it out in *New Concepts in Technical Trading Systems* (Trend Research, 1978), and
it appeared the same year in Commodities magazine.

- StockCharts ChartSchool, Relative Strength Index (RSI): "a momentum oscillator developed
  by J. Welles Wilder" in his "1978 book, New Concepts in Technical Trading Systems".
  https://chartschool.stockcharts.com/table-of-contents/technical-indicators-and-overlays/technical-indicators/relative-strength-index-rsi
- J. Welles Wilder, *New Concepts in Technical Trading Systems*, Trend Research, 1978.
  https://books.google.com/books/about/New_Concepts_in_Technical_Trading_System.html?id=WesJAQAAMAAJ

## The default setting, and the scale

**The usual default is fourteen periods, and the reading moves between zero and one hundred.**

- StockCharts ChartSchool: "This RSI calculation is based on 14 periods, the default Wilder
  suggested in his book," and "The RSI moves up and down (oscillates) between zero and 100."
  https://chartschool.stockcharts.com/table-of-contents/technical-indicators-and-overlays/technical-indicators/relative-strength-index-rsi

## What the calculation compares

**RSI compares average gains with average losses over the lookback.**

The published form is `RSI = 100 - 100 / (1 + RS)`, where `RS = Average Gain / Average Loss`.
After the first window, Wilder smooths both averages rather than taking a plain mean:
`Average Gain = [(previous Average Gain) x 13 + current Gain] / 14`, and the same for losses.

That is the whole basis of the video's claim that the reading is a statement about recent
upward closes against recent downward closes, and not about price being expensive or cheap.

- StockCharts ChartSchool, formula and smoothing.
  https://chartschool.stockcharts.com/table-of-contents/technical-indicators-and-overlays/technical-indicators/relative-strength-index-rsi

## Seventy and thirty

**Above seventy is conventionally called overbought and below thirty oversold.** These are
Wilder's own thresholds and are conventions rather than findings.

- StockCharts ChartSchool: "When the RSI is above 70, it generally indicates overbought
  conditions; when the RSI is below 30, it indicates oversold conditions."
  https://chartschool.stockcharts.com/table-of-contents/technical-indicators-and-overlays/technical-indicators/relative-strength-index-rsi

## An extreme reading can persist

**A momentum oscillator can reach an extreme and stay there while the trend continues.**

- StockCharts ChartSchool: "Momentum oscillators can become overbought (oversold) and remain
  so in a strong up (down) trend."
  https://chartschool.stockcharts.com/table-of-contents/technical-indicators-and-overlays/technical-indicators/relative-strength-index-rsi

## The trend ranges: forty to ninety, and ten to sixty

**In a bull market RSI tends to occupy roughly forty to ninety, and in a bear market roughly
ten to sixty.** These are the two ranges the video builds its regime argument on, and they
are Constance Brown's, reported in the same reference.

- StockCharts ChartSchool: RSI tends to "fluctuate between 40 and 90 in a bull market" and
  "between 10 and 60 in a bear market", with the lower bound acting as support and the upper
  bound as resistance respectively.
  https://chartschool.stockcharts.com/table-of-contents/technical-indicators-and-overlays/technical-indicators/relative-strength-index-rsi
- The related range shift work is Andrew Cardwell's, described at
  https://www.tradingview.com/chart/XAUUSD/aB1EGX45-The-Cardwell-RSI-Range-Shift-Strategy/

## The fifty line

**Above fifty, the average gain over the lookback is larger than the average loss. Below
fifty, the average loss is larger.**

This follows from the published formula rather than from a convention, and it is exact.
`RSI = 100 - 100 / (1 + RS)` is above 50 exactly when `RS > 1`, and `RS` is the average gain
divided by the average loss, so `RS > 1` is the same statement as the average gain exceeding
the average loss. The fifty line is therefore the point at which the two averages are equal.

- Formula as above, StockCharts ChartSchool.
  https://chartschool.stockcharts.com/table-of-contents/technical-indicators-and-overlays/technical-indicators/relative-strength-index-rsi
- Fifty as a coarse trend filter, and its use after a pullback that holds forty in an
  uptrend or sixty in a downtrend, is Cardwell's.
  https://www.tradingview.com/chart/XAUUSD/aB1EGX45-The-Cardwell-RSI-Range-Shift-Strategy/

## Divergence

**A bullish divergence is a lower low in price against a higher low in RSI, and a bearish
divergence is a higher high in price against a lower high in RSI.**

**Divergence is unreliable inside a strong trend**, which is the video's central caution
about it.

- StockCharts ChartSchool: "Divergences are misleading in a strong trend. A strong uptrend
  can show numerous bearish divergences before a top materializes."
  https://chartschool.stockcharts.com/table-of-contents/technical-indicators-and-overlays/technical-indicators/relative-strength-index-rsi

## Failed signals

**A failure swing is a documented RSI pattern, and it is the pattern the video describes as
a failed signal.** A bullish failure swing is RSI moving below thirty, bouncing back above
it, pulling back while holding above thirty, and then breaking its prior high. The bearish
version mirrors it around seventy.

- StockCharts ChartSchool, failure swings.
  https://chartschool.stockcharts.com/table-of-contents/technical-indicators-and-overlays/technical-indicators/relative-strength-index-rsi

## Not verifiable

**The charts in this video are illustrative rather than records of any market.** Every price
series shown is generated to demonstrate the behaviour being described, and every number
printed on screen is computed from the series it sits beside. Nothing in the video claims
that a named instrument did any of these things on any date, and no win rate, hit rate or
backtest result is stated anywhere in it.

**The interpretive parts of the video are judgement rather than measurement.** Whether a
particular pullback is a reset or a reversal, whether a level is worth respecting, and
whether a signal has been confirmed are readings a trader makes, and no source establishes
them as facts.
{% endraw %}
