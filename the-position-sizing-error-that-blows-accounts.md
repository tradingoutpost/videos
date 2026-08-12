---
layout: default
title: "The Number That Blows Accounts Is Not Your Entry"
permalink: /the-position-sizing-error-that-blows-accounts/
date: 2026-08-12
---

# The Number That Blows Accounts Is Not Your Entry

Every figure the finished video puts on screen, chased to a primary source.

Most of what this video states is arithmetic rather than a claim about the world: an account
size, a risk percentage, a stop distance and the share count that falls out of the three.
Those are sourced to the definitions they follow from and are checked below. Charts drawn to
teach a mechanism carry invented prices and are marked ILLUSTRATIVE on the frame; nothing
invented is used to assert that a particular thing happened anywhere.

## The position sizing calculation

**Position size = risk in money / risk per unit.** The video runs this three times.

- A $10,000 account risking 1% has $100 on the trade. `10,000 x 0.01 = 100`.
- An entry at $50 with a stop at $49 is $1 of risk per share, so $100 buys 100 shares.
  `100 / 1 = 100`.
- The same account and the same 1% with the stop $2 away is $2 of risk per share, so the
  same $100 buys 50 shares. `100 / 2 = 50`. Holding 100 shares instead would put $200 on
  the trade, which is 2% rather than 1%.

The method, in this order, is the one published in regulators' and exchanges' own investor
education material rather than a house rule of this channel:

- U.S. Securities and Exchange Commission, *Investor.gov*, "Assessing Your Risk Tolerance"
  and "Investing Basics" — deciding what loss is acceptable before choosing an amount to
  commit. https://www.investor.gov/introduction-investing/investing-basics/assessing-your-risk-tolerance
- CME Group Education, "Managing Risk" — risk per trade expressed as a fixed fraction of
  account equity, with size derived from the distance to the exit rather than chosen first.
  https://www.cmegroup.com/education/courses/introduction-to-futures/managing-risk.html
- U.K. Financial Conduct Authority, PS20/10, *Restricting contract for difference products*
  — the FCA's own account of how leveraged retail positions produce losses larger than
  intended. https://www.fca.org.uk/publications/policy-statements/ps20-10-restricting-contract-difference-products-retail-consumers

## Pip value, and the ten versus fifty pip comparison

The video shows one standard lot with a 10 pip stop losing $100 and the same lot with a 50
pip stop losing $500, and says the second risks five times more.

A standard lot is 100,000 units of the base currency, so a one pip move in a pair quoted to
four decimal places against the U.S. dollar is `100,000 x 0.0001 = $10`. Ten pips is $100 and
fifty pips is $500. Five times the distance at the same size is five times the money.

- CME Group Education, "Understanding FX Quotes and Pips" — lot sizes and pip value.
  https://www.cmegroup.com/education/courses/introduction-to-fx/understanding-fx-quotes.html
- Bank for International Settlements, *Triennial Central Bank Survey of foreign exchange and
  OTC derivatives markets*, for standard contract conventions in the FX market.
  https://www.bis.org/statistics/rpfx22.htm

## Three losses at one percent, and the fourth trade at five

- Three consecutive losses at 1% of a $10,000 account is roughly 3%, or about $300. Compounded
  exactly, `10,000 x 0.99^3 = 9,702.99`, a fall of 2.97%.
- A fourth trade risking 5% of what is left puts about $485 on that single trade, more than
  the first three losses put together.

Arithmetic, from the same definition as above.

## Losses compound against you, so a deeper drawdown needs a larger gain to recover

The video's argument that a drawdown taken at larger size is qualitatively different rests on
the recovery arithmetic: a 10% loss needs 11.1% to get back to level, a 25% loss needs 33.3%,
and a 50% loss needs 100%. `1 / (1 - L) - 1`.

- U.S. Securities and Exchange Commission, Office of Investor Education and Advocacy,
  *Investor Bulletin: How Fees and Expenses Affect Your Investment Portfolio*, for the
  compounding convention. https://www.sec.gov/investor/alerts/ib_fees_expenses.pdf

## Correlated positions and total exposure

The video says that several positions which all depend on the same market direction may be
one risk rather than several, using large technology shares held alongside a broad index as
the example, and that risk has to be counted across the whole book rather than per ticket.

The finished video does not put any index weight, correlation coefficient or company specific
figure on screen. The claim it makes is the general one: that a broad index contains the same
large holdings, so buying both is the same exposure bought twice, and that positions which
share a driver do not diversify each other.

- S&P Dow Jones Indices, *S&P 500 Index Methodology* — the index is a capitalisation weighted
  measure of its constituents, so a holder of the index holds every constituent in proportion.
  https://www.spglobal.com/spdji/en/documents/methodologies/methodology-sp-us-indices.pdf
- European Securities and Markets Authority, *Guidelines on risk measurement and the
  calculation of global exposure* — exposure aggregated across positions rather than assessed
  one position at a time, and netting only where positions genuinely offset.
  https://www.esma.europa.eu/document/guidelines-risk-measurement-and-calculation-global-exposure-and-counterparty-risk-ucits
- Bank of England, *Financial Stability Report*, on correlated positioning and the way
  apparently separate exposures move together in a sell off.
  https://www.bankofengland.co.uk/financial-stability-report/2024/november-2024

## Loss limits and stopping rules

The video's rules — stop or reduce risk after three losses, walk away at a daily loss limit,
trade minimum size after breaking a rule — are presented as a plan a trader writes rather than
as a finding. The underlying practice of a pre committed daily loss limit is standard risk
control rather than this channel's invention:

- CFTC, *Customer Advisory: Understand the Risks of Virtual Currency Trading* and the CFTC's
  general guidance on setting loss limits before trading rather than during it.
  https://www.cftc.gov/LearnAndProtect/AdvisoriesAndArticles/customer_advisory_urvct.html
- CME Group, *Risk Management* rulebook material on position and loss limits set in advance.
  https://www.cmegroup.com/clearing/risk-management/

## Not checked

- The trader behaviour the video describes — revenge trading after a losing run, size creeping
  up during a winning streak, moving a stop because a position feels too large — is described
  as a pattern rather than measured. No study is cited for how common any of it is, and none is
  claimed on screen.
- Every chart in the video is drawn from invented prices to show a mechanism, and is marked
  ILLUSTRATIVE where it appears. No chart asserts that a particular market did a particular
  thing on a particular day.
- The dollar figures in the two worked examples are the script's own round numbers, chosen to
  make the arithmetic legible. They are not drawn from any account.
