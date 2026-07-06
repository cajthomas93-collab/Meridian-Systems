# Meridian-Systems

A personal, systematic trading terminal for NIFTY index options — built and used privately by one person.

Show Image

What it is

Meridian is a self-hosted trading terminal I built for my own use. It connects
to my brokerage account's market-data API, turns the live tick stream into
candles and indicator readings in real time, and runs a rules-based options
strategy in paper-trading mode while I evaluate it. Everything runs
locally on my own machine (localhost) — there is no public deployment, no
other users, no paywall, and no plan for either.

Highlights


Own market data: live WebSocket tick feed via Zerodha Kite Connect
(my brokerage), aggregated in-process into 5-second, 1-minute, and 3-minute
candles. The feed persists across trading sessions; nothing depends on
third-party chart data.
Live signal terminal: a real-time dashboard showing the exact indicator
readings the trading engine computes each cycle, with health indicators,
an activity feed, and full manual controls (direction, exit modes, halt).
Paper execution engine: simulated order lifecycle (entries, stops,
scaling, exits) driven by the strategy rules, with per-trade logs for
post-session review.
Engineering discipline: an offline regression suite (22 test suites)
runs before every change lands; the system writes forensic crash/shutdown
reports; the data layer is thread-safe and windowed for all-day sessions.
Charts: the terminal currently renders its candles and indicator panes
with TradingView Lightweight Charts™ (attribution below). I am
requesting Advanced Charts access to give this internal terminal a
fuller charting experience — drawing tools, richer chart types — fed by my
own Kite Connect data through the terminal's existing chart-data API.


Tech

Python 3 / FastAPI backend · vanilla HTML/JS dashboard · Zerodha Kite Connect
(REST + WebSocket) · TradingView Lightweight Charts™ for rendering.

Source code

The trading engine's source is not published — the strategy logic is the
private core of this project. This repository exists to describe the product
for integration/review purposes.

Attribution

Charting is powered by TradingView Lightweight Charts™,
© TradingView, Inc., used under the Apache-2.0 license.

Status & intent


Solo personal project (Meridian Systems — John Thomas, India).
Internal use only: runs on my machine, against my own brokerage data.
Not affiliated with Zerodha or TradingView. Nothing here is financial advice.

Content1783325474769_nifty-trader__2_.zipzip1783325639003_MERIDIAN_STATUS (6).mdmd1783379054712_charting-library-tutorial-master.zipzip1783379054712_charting-library-examples-master.zipzip1783379080368_TradeX-chart-master.zipzip1783325646314_MERIDIAN_MASTER_RECONCILIATION.md144 linesmd1783325651637_FRONTEND_BACKEND_RECONCILIATION (1).md109 linesmd1783326363221_PS C.docx79 linesdocx
