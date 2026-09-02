---
layout: default
title: "Your TradingView Setup Is Making You Trade Worse"
permalink: /three-tradingview-mistakes-that-cost-traders/
date: 2026-09-02
---

# Your TradingView Setup Is Making You Trade Worse

{% raw %}
Everything the finished picture states about how TradingView behaves, chased to
TradingView's own documentation. Anything that could not be chased is at the bottom and is
not rendered on screen.

The price series, ladders, spreads and equity curves in the shots are invented and
illustrative. They demonstrate a mechanism; none of them asserts that anything happened.


## What a layout actually holds

> A layout contains charts, their settings, drawing tools, and indicators. It is identified
> by a unique URL.

Watchlists and alerts are not stored in a layout.

Source: TradingView Help Center, *Layouts, charts, drawings, indicators, and their
interaction*
https://www.tradingview.com/support/solutions/43000692404-layouts-charts-drawings-indicators-and-their-interaction/

Used by: 013-what-a-layout-holds, 014-it-is-memory, 024-separate-by-job.


## Drawings sync across charts and layouts

The same page gives drawing tools three synchronisation modes:

- **Disabled.** "Drawing objects will be saved only on a specific chart of a particular
  layout."
- **By layout.** "Synchronization by layout synchronizes the drawings on the current symbol
  across all charts in the current layout."
- **Global.** "Drawing objects will be synchronized across all charts and layouts, which
  means they will appear even in completely new layouts."

Global synchronisation is what puts a level drawn on one chart onto a chart it was never
drawn for, which is the mechanism the video describes.

Source: as above.

Used by: 020-drawings-sync, 021-swing-follows-scalp.


## What an alert can be created from

> [An alert condition] can be either a price alert or a technical alert for an indicator,
> strategy or drawing tool on your chart.

Source: TradingView Help Center, *Learn how to configure alerts*
https://www.tradingview.com/support/solutions/43000763312-learn-how-to-configure-alerts/

Used by: 040-what-can-trigger.


## The trigger frequency is a setting, and it decides what the alert means

- **Only Once.** "An alert is triggered only once. Alert conditions have to match the exact
  parameters that you set for it to be triggered."
- **Once Per Bar.** "The system checks every bar and triggers an alert whenever conditions
  are met (no more than once per bar)."
- **Once Per Bar Close.** "Same as above, but the bar needs to close for an alert to be
  triggered."
- **Once Per Minute.** "The system checks conditions every minute and triggers an alert
  whenever conditions are met."

This is the documented difference between an alert that can fire on a wick during a live
bar and one that cannot fire until the bar has closed.

Source: TradingView Help Center, *Differences between alert frequencies*
https://www.tradingview.com/support/solutions/43000474415-differences-between-alert-frequencies/

Used by: 041-settings-decide, 042-touch-versus-close, 056-respect-the-close.


## Regular and extended sessions are two different charts of the same instrument

A regular session chart excludes pre-market and post-market data; an extended session chart
includes it. The setting is per symbol, under Settings, Symbol, Extended Hours, and is
available on intraday timeframes only.

Sources: TradingView, *Extended and regular sessions*
https://www.tradingview.com/pine-script-docs/v4/essential/extended-and-regular-sessions/
and TradingView Help Center, *I want to access Extended Hours data*
https://www.tradingview.com/support/solutions/43000502023-i-want-to-access-extended-hours-data/

Used by: 071-wrong-session, 072-which-session-counts, 073-deliberate-answer,
074-chosen-by-accident, 082-panel-and-session.


## Delayed data is marked on the chart

A delayed symbol carries a "D" on the chart. The length of the delay is set by the
exchange, not by TradingView, and differs from market to market, which is why the video
asks whether the data is real time rather than naming a number of minutes.

Source: TradingView Help Center, *Alerts based on real-time and non-real-time symbols*
https://www.tradingview.com/support/solutions/43000698958-alerts-based-on-real-time-and-non-real-time-symbols/

Used by: 063-all-the-variants, 081-symbol-and-feed.


## The chart and the broker order panel are not the same source

TradingView's own answer for a connected broker account is explicit that the two feeds are
separate: chart quotes come from the data package on the TradingView account, while the bid
and ask in the order panel and DOM come from the broker.

> Data packages purchased on TradingView do not cover these quotes. They allow users to see
> real-time on the charts, watchlist, and screener (for stocks).

> We receive Ask and Bid prices from the brokers once users log on their broker accounts on
> TradingView.

Source: TradingView Help Center, *Why is the data delayed in the Order Panel and DOM on my
Interactive Brokers account?*
https://www.tradingview.com/support/solutions/43000719859-why-is-the-data-delayed-in-the-order-panel-and-dom-on-my-interactive-brokers-account/

Used by: 010-problem-three, 067-not-the-same-source, 069-break-resistance,
070-the-fill-is-worse, 082-panel-and-session.


## Synthetic chart types use prices a real order could not get

TradingView documents this directly for backtests:

> Because of the inherently synthetic nature of price levels on non-standard charts,
> backtesting results calculated on them will typically not produce results representing
> real market conditions.

> Strategy orders are filled using the chart's OHLC values.

> Renko brick levels, being disconnected from actual market prices at any given moment,
> will fill orders using their own prices and therefore, will not produce reliable strategy
> results.

And for Heikin Ashi specifically, the direction of the error:

> The HA open will often be lower on long entries and higher on short entries, resulting in
> unrealistically advantageous fills.

TradingView also documents the remedy, which is the "Using standard OHLC" option in a
strategy's Properties: the strategy can be calculated on Heikin Ashi data while opening and
closing positions on standard chart prices.

Source: TradingView Help Center, *Strategy produces unrealistic results on non-standard
chart types (Heikin Ashi, Renko, etc.)*
https://www.tradingview.com/support/solutions/43000481029-strategy-produces-unrealistic-results-on-non-standard-chart-types-heikin-ashi-renko-etc/

Used by: 064-backtest-values, 075-synthetic-types, 076-perspective-not-entries,
077-values-never-reached, 078-plain-translation, 079-standard-candles-verify,
083-backtest-reachable.


## Not checked

- Every price series, spread, ladder, slippage figure and equity curve on screen is
  invented for the shot. They are illustrative of a mechanism and none of them is a record
  of a real market.
- How often beginners actually set each kind of alert. No published breakdown exists, so
  no proportion is rendered on screen: 055-most-are-watch shows the three instruments and
  no counts.
- How large the difference between a chart quote and a broker fill typically is. The
  narration says it is tiny in a slow market and brutal in a fast one, which is a
  characterisation rather than a measured figure, and no figure is claimed for it.
- Whether a given exchange's delay is ten minutes, fifteen, or none. It is set per exchange
  and per data package, so the picture shows a delayed feed running behind a live one and
  never names a number.
{% endraw %}
