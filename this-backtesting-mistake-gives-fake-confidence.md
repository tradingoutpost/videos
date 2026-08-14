---
layout: default
title: "Your Backtest Is Lying To You Right Now"
permalink: /this-backtesting-mistake-gives-fake-confidence/
date: 2026-08-14
---

# Your Backtest Is Lying To You Right Now

Every price series, equity curve, win rate, drawdown and trade result shown in this video
is a generated illustrative example, drawn from a seeded model so it can be reproduced
exactly, and each one carries that label on screen. None of them is the record of a real
strategy, a real account or a real market period, and nothing in the video asserts that
any figure shown was earned.

The parameter values the narration works through — a twenty one period moving average, an
RSI threshold of fifty seven, a stop of one point four ATR, a session window of 08:30 to
10:15, a stop of one point seven ATR, a target of two point three R, and the second Friday
of the month — are the narration's own worked examples of settings a trader might land on.
They are drawn as the dials they are and none of them is presented as a finding.

The claims below are the substantive ones the video makes about how backtesting behaves.


## Testing more variations makes a good looking backtest easier to find by chance

The video's central mechanism: that a strategy tuned across many configurations can reach
a strong historical result without holding any durable edge, and that the more
configurations are tried, the more likely the result is an artefact of the search.

> "We prove that high simulated performance is easily achievable after backtesting a
> relatively small number of alternative strategy configurations, a practice we denote
> 'backtest overfitting'. The higher the number of configurations tried, the greater is the
> probability that the backtest is overfit."

Bailey, D. H., Borwein, J. M., López de Prado, M., and Zhu, Q. J. (2014).
*Pseudo-Mathematics and Financial Charlatanism: The Effects of Backtest Overfitting on
Out-of-Sample Performance.* Notices of the American Mathematical Society, May 2014.
https://www.ams.org/notices/201405/rnoti-p458.pdf
Abstract as published: https://scholarworks.wmich.edu/math_pubs/40/
Working paper: https://papers.ssrn.com/sol3/papers.cfm?abstract_id=2308659

On screen at `018-more-variations` as: **Source: Bailey, Borwein, López de Prado and Zhu,
Notices of the AMS, 2014**


## An overfitted strategy can do worse than nothing once it is traded

The video says the chosen configuration going flat is the optimistic case. The same paper
states the harsher one.

> "Under memory effects, backtest overfitting leads to negative expected returns
> out-of-sample, rather than zero performance. This may be one of several reasons why so
> many quantitative funds appear to fail."

Same citation as above.

On screen at `018-more-variations`, on the forward panel where the selected curve turns
down rather than merely flattening.


## The best rule found in a historical sample often fails in the period after it

The video's out-of-sample argument, and its regime argument, both rest on this: a rule
selected because it was the best performer over a searched history is not reliably the
best performer afterwards.

Sullivan, Timmermann and White applied White's Reality Check bootstrap to the full
universe of technical trading rules the earlier literature had drawn from, over 100 years
of daily Dow Jones Industrial Average data. The best rule was superior in the original
sample even after adjusting for data snooping, and was not superior over the subsequent
ten year post-sample period.

Sullivan, R., Timmermann, A., and White, H. (1999). *Data-Snooping, Technical Trading Rule
Performance, and the Bootstrap.* The Journal of Finance, 54(5), 1647–1691.
https://onlinelibrary.wiley.com/doi/10.1111/0022-1082.00163

On screen at `027-split-the-data` and `028-fails-on-fresh-data` as: **Source: Sullivan,
Timmermann and White, Journal of Finance, 1999**


## A performance figure has to be corrected for how many strategies were tried

Behind the video's warning that a strong number means less when it was selected out of
many attempts: a headline performance ratio taken at face value is inflated by the
selection itself, and the correction is a published one rather than a matter of opinion.

Bailey, D. H., and López de Prado, M. (2014). *The Deflated Sharpe Ratio: Correcting for
Selection Bias, Backtest Overfitting, and Non-Normality.* The Journal of Portfolio
Management, 40(5), 94–107.
https://jpm.pm-research.com/content/40/5/94.abstract
Working paper: https://papers.ssrn.com/sol3/papers.cfm?abstract_id=2460551

On screen at `042-evidence-not-proof` as: **Source: Bailey and López de Prado, Journal of
Portfolio Management, 2014**


## Realistic execution costs are large enough to remove a thin edge

The video's third test. Costs are not a rounding error applied at the end; for strategies
that trade often they are the difference between a gross result and a net one.

Novy-Marx and Velikov measured execution costs from Trade and Quote data and found average
trade execution costs of 20 to 57 basis points for the mid-turnover strategies they
examined. They also found that most strategies turning over less than 50% per month
generated significant net spreads once designed to mitigate costs, and few with higher
turnover did — which is the video's point that the faster the strategy trades, the more of
the edge the costs take.

Novy-Marx, R., and Velikov, M. (2016). *A Taxonomy of Anomalies and Their Trading Costs.*
The Review of Financial Studies, 29(1), 104–147.
https://academic.oup.com/rfs/article/29/1/104/1844518
Working paper: https://www.nber.org/papers/w20721

On screen at `031-third-costs` and `032-edge-too-thin` as: **Source: Novy-Marx and Velikov,
Review of Financial Studies, 2016**


## The gap between a strategy on paper and a person trading it is measurable

The video's closing argument, that a strategy which tests well may still be one you cannot
follow, and that the difference shows up in what people actually earn rather than in what
the method could have earned.

Barber and Odean examined 66,465 households at a large discount broker from 1991 to 1996.
The average household earned an annual return of 16.4 per cent and turned over 75 per cent
of its portfolio a year; the households that traded most earned 11.4 per cent against a
market return of 17.9 per cent over the same period.

Barber, B. M., and Odean, T. (2000). *Trading Is Hazardous to Your Wealth: The Common Stock
Investment Performance of Individual Investors.* The Journal of Finance, 55(2), 773–806.
https://onlinelibrary.wiley.com/doi/abs/10.1111/0022-1082.00226

On screen at `053-the-human-part` as: **Source: Barber and Odean, Journal of Finance, 2000**


## Not checked

- That a backtest assumes perfect execution is a statement about what the method does
  rather than a measured claim, and it is not sourced. A backtest fills every signal it
  generates unless it is explicitly built to model rejected fills, latency and partial
  fills; whether any particular platform does so varies and is not covered here.
- The video's claim that fragile settings are a warning sign, and that a real edge should
  degrade gracefully rather than collapse when a parameter moves one notch, is standard
  practitioner guidance on robustness testing rather than a result chased to a primary
  source here. No figure is put on screen asserting how wide a stable plateau ought to be.
- The specific list of what forward testing exposes — hesitation, signal clarity, platform
  issues, spread changes and whether the rules can be followed — is the script's own
  enumeration and is not sourced item by item.
- No claim is made or shown about how often curve fitting occurs among retail traders, and
  no such figure appears on screen.
