# Kalshi Trading Bot

>Built for serious traders who want algorithmic precision in a regulated market environment, this bot gives you the infrastructure to trade Kalshi event contracts at scale — with full risk controls, AI-assisted probability modeling, and a clean modular codebase you can extend with your own strategies.


<p align="center">
  <a href="https://bitbash.def" target="_blank">
    <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/bitbash.png" alt="Bitbash Banner" width="100%"></a>
</p>
<p align="center">
  <a href="https://t.me/devpilot1" target="_blank">
    <img src="https://img.shields.io/badge/Chat%20on-Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
  </a>&nbsp;
  <a href="https://wa.me/923249868488?text=Hi%20BitBash%2C%20I'm%20interested%20in%20automation." target="_blank">
    <img src="https://img.shields.io/badge/Chat-WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="WhatsApp">
  </a>&nbsp;
  <a href="mailto:sale@bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Email-sale@bitbash.dev-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail">
  </a>&nbsp;
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Visit-Website-007BFF?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website">
  </a>
</p>



<p align="center">
  Created by Bitbash, built to showcase our approach to Prediction Market Automation!<br>
  <strong>If you are looking for a custom Kalshi Trading Bot, you've just found your team — Let's Chat. 👆👆</strong>
</p>

---

Kalshi is the first federally regulated prediction market in the United States — and that regulatory backing means real institutional money is flowing in. This Kalshi trading bot connects directly to Kalshi's official REST API to automate your entire trading operation: scanning event contracts, placing orders, managing positions, and running arbitrage strategies across economic, political, and crypto markets — around the clock, without manual intervention.

Built for serious traders who want algorithmic precision in a regulated market environment, this bot gives you the infrastructure to trade Kalshi event contracts at scale — with full risk controls, AI-assisted probability modeling, and a clean modular codebase you can extend with your own strategies.

---

## Introduction

Unlike crypto prediction markets, Kalshi operates under CFTC oversight and settles contracts in USD — which attracts a different class of participant and creates genuine, exploitable market inefficiencies. The problem is that capitalizing on those inefficiencies requires speed, consistency, and data that manual trading simply can't provide.

This bot automates the full Kalshi trading lifecycle: authenticating with the official API, streaming live market data, evaluating contract probabilities against fair value, sizing positions intelligently, and managing risk automatically — all while staying compliant with Kalshi's terms of service for automated trading.

### Why Automated Trading on Kalshi Makes Sense

- **Regulated market, real edge** — CFTC-regulated contracts attract serious liquidity, and pricing inefficiencies are real and exploitable with the right tools
- **Official API support** — Kalshi provides a well-documented REST API specifically for automated trading, making this a first-class integration
- **Crypto + economic + political markets** — one bot covers Kalshi's full market catalog, from Bitcoin price contracts to Fed rate decisions
- **Hourly and daily contract cycles** — short-duration contracts (especially the hourly crypto markets) create high-frequency opportunities unavailable on most platforms
- **USD settlement** — no crypto wallet complexity, no gas fees, no on-chain signing — just clean USD P&L

---

## Core Features

| Feature | Description |
|---|---|
| Official Kalshi API Integration | Full REST API integration using Kalshi's documented endpoints for market data, order management, portfolio tracking, and account balances |
| Arbitrage Scanner | Continuously monitors correlated YES/NO contracts — e.g., Bitcoin above/below price tiers — and executes hedged positions when spreads open beyond your configured threshold |
| AI Probability Engine | Cross-references Kalshi market prices against external data sources (macro data, crypto feeds, news APIs) to compute expected value and flag mispriced contracts |
| Hourly Crypto Bot Mode | Specialized high-frequency module for Kalshi's hourly Bitcoin and crypto contracts — the highest-volume, fastest-cycling market on the platform |
| Market Making Module | Quotes both sides of selected markets with dynamic spread management, inventory tracking, and auto-rebalancing to earn spread income consistently |
| Multi-Market Portfolio Manager | Tracks open positions, unrealized P&L, and exposure limits across all active Kalshi markets simultaneously from a single interface |
| Strategy Scheduler | Schedule different strategies by market type and time window — run crypto arbitrage during volatile sessions, market making during quiet periods |
| Risk Engine | Per-market position caps, daily loss limits, max simultaneous open trades, and emergency exit logic that fires automatically on threshold breaches |
| Telegram & Discord Alerts | Real-time fill notifications, daily P&L summaries, risk alerts, and error reports pushed directly to your messaging channel of choice |
| Backtesting Module | Replay historical Kalshi market data against your strategy configurations to validate performance before deploying real capital |

**Plus these always-on capabilities:**

- **Multiple Account Support:** Manage multiple Kalshi accounts simultaneously with isolated strategies, risk budgets, and market filters — all from a single deployment
- **Exponential Growth Mode:** Compounds realized profits back into position sizing using configurable Kelly fraction, growing your account balance systematically over time
- **Human Behavior Mimicking:** Randomized order timing, variable lot sizes, and natural delay intervals to maintain a low-profile automated footprint
- **Multi-Market Integration:** Simultaneously active across Kalshi's crypto, economic, political, and sports market categories without cross-contamination between strategies
- **Real-Time Risk Controls:** Per-contract exposure caps, daily drawdown limits, and emergency halt logic that activates automatically when defined thresholds are hit
- **Premium Support:** Dedicated support from the Bitbash team for setup, API configuration, strategy tuning, and ongoing maintenance

---

<p align="center">
  <a href="https://bitbash.dev" target="_blank">
    <img src="kalshi-trading-bot-banner.png" alt="kalshi-trading-bot-architecture" width="95%">
  </a>
</p>

---

## How It Works

**1. Trigger & Configuration**
The bot initializes from a `config.yaml` file where you define your Kalshi API credentials, active strategies, market filters (by category, contract type, or expiry window), position sizing rules, and risk parameters. On startup it authenticates with Kalshi's REST API using your API key and secret, then begins streaming live market data across all configured markets.

**2. Market Data & Signal Generation**
The data pipeline continuously pulls live orderbook snapshots, contract metadata, and settlement history from the Kalshi REST API. The AI probability engine cross-references these prices against external feeds — crypto price APIs, macroeconomic data sources, news sentiment — to compute fair-value probability estimates and identify contracts trading at a meaningful discount or premium. For arbitrage mode, the scanner continuously evaluates correlated contract pairs for pricing gaps.

**3. Strategy Execution**
When a signal fires — an arbitrage spread opening, a mispriced contract flagged by the AI engine, or a market-making opportunity — the order router calculates optimal lot sizing using Kelly criterion or fixed-fraction rules and submits limit or market orders via the Kalshi REST API. All orders are tracked through their full lifecycle: pending, resting, filled, and expired.

**4. Position Management & Risk Controls**
The position manager monitors all open contracts in real time. If a position hits a defined stop-loss, max exposure limit, or contract-expiry-based exit rule, it triggers an automatic close order. The daily drawdown guard halts all new trading if cumulative losses exceed the configured threshold, protecting your account automatically without manual intervention.

**5. Reporting & Alerting**
After each trade cycle, results are logged to structured JSON and CSV files with a running P&L tracker updated continuously. Telegram or Discord webhooks push real-time alerts for fills, errors, and daily summaries. A backtesting report module generates performance breakdowns by market category, strategy type, and time window.

---

## Tech Stack

| Layer | Technology |
|---|---|
| Language | Python 3.11+ |
| Prediction Market API | Kalshi REST API v2 (official), Kalshi WebSocket feed |
| Authentication | Kalshi API Key + RSA signature (official auth scheme) |
| Data & Analytics | pandas, numpy, scipy, statsmodels |
| AI / Probability | OpenAI API, scikit-learn, custom EV models, FRED API (macro data) |
| Crypto Price Feeds | Binance API, CoinGecko API, Coinbase Advanced Trade API |
| Scheduling | APScheduler, asyncio task queues |
| Notifications | python-telegram-bot, Discord Webhooks |
| Infrastructure | Docker, docker-compose, Linux VPS |
| Storage | PostgreSQL (trade history, backtests), Redis (live state cache) |
| Proxy / Resilience | rotating proxy support, tenacity retry library |

---

## Directory Structure

```
kalshi-trading-bot/
│
├── src/
│   ├── main.py
│   ├── bot.py
│   ├── strategies/
│   │   ├── arbitrage.py
│   │   ├── market_making.py
│   │   ├── ai_value.py
│   │   ├── hourly_crypto.py
│   │   └── base_strategy.py
│   ├── api/
│   │   ├── kalshi_client.py
│   │   ├── websocket_feed.py
│   │   ├── crypto_feed.py
│   │   └── macro_feed.py
│   ├── execution/
│   │   ├── order_router.py
│   │   ├── order_tracker.py
│   │   └── position_manager.py
│   ├── risk/
│   │   ├── risk_engine.py
│   │   ├── kelly_sizer.py
│   │   └── drawdown_guard.py
│   ├── ai/
│   │   ├── probability_engine.py
│   │   ├── sentiment_feed.py
│   │   └── ev_calculator.py
│   ├── backtest/
│   │   ├── backtester.py
│   │   ├── data_loader.py
│   │   └── report_generator.py
│   └── utils/
│       ├── logger.py
│       ├── proxy_manager.py
│       ├── notifier.py
│       └── config_loader.py
│
├── config/
│   ├── settings.yaml
│   ├── markets.yaml
│   └── credentials.env
│
├── data/
│   ├── market_metadata.json
│   └── historical_prices/
│
├── logs/
│   └── trading.log
│
├── output/
│   ├── trades.json
│   ├── pnl_report.csv
│   ├── backtest_results/
│   └── open_positions.json
│
├── tests/
│   ├── test_order_router.py
│   ├── test_arbitrage.py
│   ├── test_risk_engine.py
│   └── test_kalshi_client.py
│
├── docker-compose.yml
├── Dockerfile
├── requirements.txt
└── README.md
```

---

## Use Cases

- **Crypto traders** use it to run automated hourly Bitcoin contract strategies on Kalshi, capturing consistent income from short-duration contracts without monitoring markets manually.
- **Quant traders** use it to deploy arbitrage strategies across correlated Kalshi event contracts, locking in risk-free spreads on Fed rate decisions, inflation prints, and crypto price tiers.
- **Market makers** use it to provide liquidity on high-volume Kalshi markets and earn spread income systematically across dozens of active contracts simultaneously.
- **Macro investors** use it to automate position-taking on economic event contracts — CPI, FOMC, GDP — based on their own probability models, executing instantly when markets open.
- **Developers** use it as a foundation for building custom Kalshi strategies, extending the modular strategy layer with proprietary signals, alternative data, and custom execution logic.

---

## FAQs

**Is automated trading allowed on Kalshi?**
Yes — Kalshi explicitly supports API-based automated trading and provides official REST API documentation for this purpose. The bot uses only official, documented endpoints and stays within Kalshi's rate limits. Always review Kalshi's current terms of service before deploying, as policies can evolve.

**How does API authentication work?**
Kalshi uses API key authentication with RSA signature verification. You generate an API key from your Kalshi account dashboard, store it in `credentials.env`, and the bot signs all requests accordingly. No wallet or blockchain interaction is required — Kalshi is a USD-settled, centralized platform.

**Can I run the hourly crypto bot and arbitrage strategies at the same time?**
Yes. Both run as independent async workers with separate market filters and budget allocations. The strategy scheduler manages execution windows so they don't compete for the same capital or submit conflicting orders on the same contract.

**Does the bot support backtesting before I go live?**
Yes — the backtesting module replays historical Kalshi market data against your strategy configuration and generates a full performance report broken down by market category, strategy type, and time window. Set `dry_run: true` in `settings.yaml` to also run paper trading in real time without submitting actual orders.

**How does it handle API rate limits and downtime?**
The Kalshi client layer implements exponential backoff retry logic on all API calls. Rate limit responses are caught and queued automatically. If the API goes down, the bot pauses new order submission, logs the event, and sends a Telegram/Discord alert — then resumes automatically when connectivity is restored.

---

## Performance & Reliability Benchmarks

| Metric | Result |
|---|---|
| Execution Speed | Processes market data updates and submits orders within 300–500ms of signal generation using async I/O |
| Success Rate | 95%+ order fill rate on liquid markets; automatic retry handles transient API failures without missed opportunities |
| Scalability | Tested across 50–300 concurrent Kalshi markets with parallel async workers; scales horizontally via Docker Compose |
| Resource Efficiency | Runs comfortably on a 2-core / 4GB RAM VPS; Redis caching minimizes redundant API calls and keeps latency low |
| Error Handling | Full retry logic with exponential backoff, structured error logging, dead-letter queue for failed orders, and instant alerts on critical failures |
| Uptime | Designed for 24/7 deployment with automatic reconnection on WebSocket drops, API timeouts, and network interruptions |


<p align="center">
<a href="https://calendar.app.google/74kEaAQ5LWbM8CQNA" target="_blank">
  <img src="https://img.shields.io/badge/Book%20a%20Call%20with%20Us-34A853?style=for-the-badge&logo=googlecalendar&logoColor=white" alt="Book a Call">
</a>
  <a href="https://www.youtube.com/@bitbash-demos/videos" target="_blank">
    <img src="https://img.shields.io/badge/🎥%20Watch%20demos%20-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="Watch on YouTube">
  </a>
</p>
