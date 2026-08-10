---
layout: default
title: "Why A Perfect Backtest Falls Apart In Live Trading"
permalink: /5-reasons-your-backtest-wont-survive-live-trading/
date: 2026-08-10
---

# Why A Perfect Backtest Falls Apart In Live Trading

Every factual claim the video makes, chased to a primary source. Where a figure could not be
traced to one, it is not printed on screen and it is listed at the end instead.

A note on the charts. The price series, equity curves, parameter sweeps and trade ledgers in
this video are generated from stated models rather than taken from a market, because each one
is teaching a mechanism rather than reporting a result. Every frame that uses one is marked
**Illustrative** on screen. Nothing in the video asserts that a particular strategy returned
a particular number.

---

## Reason one: execution and costs

### A stop's trigger price is not the price it fills at

The US Securities and Exchange Commission's own investor bulletin states that the stop price
is a trigger which converts the order into a market order, and that the execution price
"can deviate significantly from the stop price in a fast-moving market where prices change
rapidly". It further warns that a stop order may be triggered by a short-term intraday price
move and fill at a price substantially worse than expected.

- SEC, *Investor Bulletin: Stop, Stop-Limit, and Trailing Stop Orders*
  https://www.sec.gov/oiea/investor-alerts-bulletins/ib-stoporders

### A limit order may not fill at all

The same bulletin notes that a stop-limit order's limit price requires execution at that price
or better, and that the limit price "may prevent the order from being executed".

- SEC, *Investor Bulletin: Stop, Stop-Limit, and Trailing Stop Orders*
  https://www.sec.gov/oiea/investor-alerts-bulletins/ib-stoporders

### Spreads widen around releases, the rollover and thin hours

Liquidity providers withdraw quotes around high-impact economic releases, and the resulting
drop in available liquidity widens quoted spreads. Liquidity also thins around the daily
rollover and at session edges. The direction of this effect is well established in the
academic literature on price discovery and liquidity in foreign exchange.

- *Economic News, Price Discovery and Liquidity in the Foreign Exchange Market*
  https://www.aof.org.hk/uploads/conference_detail/502/con_paper_0_491_session-3-1_tham_2sep08.pdf

No multiple is stated for how far spreads widen, on screen or in the narration. See
**Not traced to a primary source** below.

---

## Reason two: data and lookahead bias

### Survivorship bias inflates historical results

Testing only on instruments that still exist today excludes those that failed or delisted,
which makes the surviving history look cleaner than the real one was. Elton, Gruber and Blake
(1996) measured survivorship bias in mutual fund returns at approximately 0.9% per year. Brown,
Goetzmann, Ibbotson and Ross found that survivorship can inflate Sharpe ratios by as much as
0.5, which is substantial against a Sharpe of 1.0 being considered strong.

- *The cross-section of stock returns and survivorship bias: evidence from delisted stocks*
  https://www.sciencedirect.com/science/article/abs/pii/S1062976996900216
- Alpha Architect, *Dealing with Delistings: A Critical Aspect for Stock-Selection Research*
  https://alphaarchitect.com/dealing-with-delistings-a-critical-aspect-for-stock-selection-research/

### Repainting is a documented behaviour, and zigzag and pivot tools do it by construction

TradingView's Pine Script documentation carries a dedicated page on indicator repainting: a
script behaves differently on historical bars than in real time when its output depends on data
that arrives later. A zigzag requires subsequent bars to confirm a pivot, so its markers move
after the fact. On a historical bar Pine shows finalised values; on a real-time bar those values
are still changing until the bar closes.

- TradingView, Pine Script documentation, *Indicator repainting*
  https://www.tradingview.com/pine-script-docs/v4/essential/indicator-repainting/
- TradingView, *ZigZag* library, which documents pivots as the highest or lowest value over a
  defined number of bars **before and after** them
  https://www.tradingview.com/script/bzIRuGXC-ZigZag/

---

## Reason three: overfitting

### The more configurations you test, the more likely the result is overfit

Bailey, Borwein, López de Prado and Zhu (2014), in the *Notices of the American Mathematical
Society*, show that high simulated performance is easily achievable after testing a relatively
small number of strategy configurations, and that the probability a backtest is overfit rises
with the number of configurations tried. They also note that the number of configurations tried
is almost never reported, which leaves a reader unable to judge the degree of overfitting.

- Bailey, Borwein, López de Prado and Zhu, *Pseudo-Mathematics and Financial Charlatanism: The
  Effects of Backtest Overfitting on Out-of-Sample Performance*, Notices of the AMS, May 2014
  https://www.ams.org/notices/201405/rnoti-p458.pdf
- SSRN version https://papers.ssrn.com/sol3/papers.cfm?abstract_id=2308659
- Follow-up, *Statistical Overfitting and Backtest Performance*
  https://sdm.lbl.gov/oapapers/ssrn-id2507040-bailey.pdf

### Testing many variants against one dataset requires a statistical correction

White's Reality Check and Hansen's Superior Predictive Ability test exist specifically to adjust
significance when many models are compared against the same data, which is the formal treatment
of the same problem.

- White, *A Reality Check for Data Snooping*, Econometrica 68(5), 2000
  https://www.researchgate.net/publication/4896389_A_Reality_Check_for_Data_Snooping

### Walk-forward analysis is a defined method

Robert Pardo set out walk-forward analysis in *Design, Testing and Optimization of Trading
Systems* (1992; second edition 2008): the strategy is optimised on an in-sample window, tested
on the out-of-sample span immediately following it, and the window is then advanced and the
process repeated, so the reported result is composed only of out-of-sample segments.

- Pardo, *Design, Testing and Optimization of Trading Systems*, Wiley
- Overview and attribution https://en.wikipedia.org/wiki/Walk_forward_optimization

---

## Reason four: market regime

### Trend following depends on persistence that exists at some horizons and not others

Moskowitz, Ooi and Pedersen (2012) document time series momentum across 58 liquid futures
instruments spanning equity indices, currencies, commodities and bonds: returns persist at
horizons of one to twelve months and **partially reverse** over longer horizons. The same rule is
therefore working with the grain of the market at one horizon and against it at another.

- Moskowitz, Ooi and Pedersen, *Time Series Momentum*, Journal of Financial Economics 104(2),
  2012, pp. 228-250
  https://w4.stern.nyu.edu/facdir/lpederse/papers/TimeSeriesMomentum.pdf
- SSRN version https://papers.ssrn.com/sol3/papers.cfm?abstract_id=2089463

### When a momentum strategy fails, the state of the market is the variable, not the rule

Daniel and Moskowitz (2016) show that momentum strategies suffer infrequent and persistent
strings of negative returns which are partly forecastable: they occur in "panic" states,
following market declines and when market volatility is high, and coincide with market rebounds.
The strategy is unchanged throughout; the paper names the conditions that turn against it.

- Daniel and Moskowitz, *Momentum Crashes*, Journal of Financial Economics 122(2), 2016,
  pp. 221-247
  https://www.kentdaniel.net/papers/published/jfe_16.pdf
- NBER working paper https://www.nber.org/papers/w20439

---

## Reason five: the trader

### Behaviour changes the result, measurably

Barber and Odean (2000) studied 66,465 households holding common stock at a large discount
broker between 1991 and 1996. The households that traded most earned an annual return of 11.4%
against a market return of 17.9%, and the average household underperformed a value-weighted
market index by roughly 3.7 percentage points a year. The authors attribute the excess trading
to overconfidence. A live result is therefore the strategy combined with the decisions taken
around it, not the strategy alone.

- Barber and Odean, *Trading Is Hazardous to Your Wealth: The Common Stock Investment
  Performance of Individual Investors*, Journal of Finance 55(2), 2000, pp. 773-806
  https://faculty.haas.berkeley.edu/odean/papers%20current%20versions/individual_investor_performance_final.pdf
- Journal of Finance https://onlinelibrary.wiley.com/doi/abs/10.1111/0022-1082.00226

---

## Not traced to a primary source

These claims are made in the narration and are not supported by a citation above. None of them
appears as a figure on screen.

- **How far spreads widen around a release.** Figures of five to ten times a normal spread
  circulate widely but trace only to broker and vendor commentary, so no multiple is stated.
  The direction of the effect is sourced above.
- **The size of the survivorship effect on a trading strategy specifically.** The 0.9% per year
  and 0.5 Sharpe figures above are measured on funds, not on a rule-based strategy. Figures
  claiming a strategy's return roughly halves, or that excluding delistings can quadruple
  returns, trace only to vendor blogs and are not used.
- **That a one pip spread and one pip of slippage are typical.** These are the script's own
  stated hypothetical for the worked example, not a measurement of any venue.
- **The proportion of traders who abandon a system during a drawdown.** Discussed in general
  terms only; no figure is given.
