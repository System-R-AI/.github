<p align="center">
  <a href="https://systemr.ai">
    <picture>
      <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/System-R-AI/.github/main/assets/systemr-logo-dark.svg" />
      <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/System-R-AI/.github/main/assets/systemr-logo-light.svg" />
      <img alt="System R AI" src="https://raw.githubusercontent.com/System-R-AI/.github/main/assets/systemr-logo-light.svg" width="260" />
    </picture>
  </a>
</p>

<h3 align="center">The trading operating system for humans and agents</h3>

<p align="center">
  <a href="https://systemr.ai">Website</a> ·
  <a href="https://docs.systemr.ai">Docs</a> ·
  <a href="https://app.systemr.ai">Platform</a> ·
  <a href="https://agents.systemr.ai">Agents API</a> ·
  <a href="https://x.com/Systemrai">X</a>
</p>

<p align="center">
  <a href="https://pypi.org/project/systemr/"><img src="https://img.shields.io/pypi/v/systemr?style=for-the-badge&color=3ECF8E&label=SDK" alt="PyPI" /></a>
  <a href="https://github.com/System-R-AI/systemr-python/blob/main/LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue?style=for-the-badge" alt="License" /></a>
</p>

---

System R is a complete trading operating system. 55 MCP tools deliver position sizing, risk validation, regime detection, Monte Carlo simulation, behavioral analytics, and execution across 25 brokers — from one API.

Agents call `pre_trade_gate` before every trade. One endpoint checks position sizing (G-formula), risk limits (Iron Fist), market regime, and system health. Returns approved or blocked with the exact number of shares to buy. $0.01 per call.

```python
pip install systemr
```

```python
from systemr import SystemRClient

client = SystemRClient(api_key="sr_agent_...")

# One call before every trade
gate = client.pre_trade_gate(
    symbol="AAPL", direction="long",
    entry_price="185.50", stop_price="180.00",
    equity="100000",
)

if gate["gate_passed"]:
    print(f"Buy {gate['sizing']['shares']} shares")
    # → Buy 160 shares, risk $800 (1.6%), G-Score: 1.12
```

### Same API. Every asset class.

```python
client.pre_trade_gate(symbol="BTC-USDT", direction="long", ...)      # Crypto
client.pre_trade_gate(symbol="EUR-USD", direction="short", ...)       # Forex
client.calculate_options_size(symbol="SPY", strike="530", ...)        # Options
client.calculate_futures_size(symbol="ES", direction="long", ...)     # Futures
client.pre_trade_gate(symbol="TRUMP-WIN", direction="long", ...)     # Prediction Markets
```

### What we built

```
55 MCP Tools        25 Brokers          9 LLM Models
187 Domain Services Every Asset Class   Per-Agent Encryption
13,500+ Tests       $0.003/call         MCP + REST + SDK
```

### Repositories

| Repo | What it is |
|------|-----------|
| [**systemr-python**](https://github.com/System-R-AI/systemr-python) | Python SDK — `pip install systemr` — 55 tools, 25 brokers |
| [**demo-trading-agent**](https://github.com/System-R-AI/demo-trading-agent) | Reference agent — momentum strategy with pre-trade risk gates |

### How it works

```
                    ┌─────────────────────────────────┐
                    │         Your Agent / LLM         │
                    └──────────────┬──────────────────┘
                                   │
                         SDK / MCP / REST API
                                   │
                    ┌──────────────▼──────────────────┐
                    │          System R API            │
                    │                                  │
                    │  ┌──────────┐  ┌─────────────┐  │
                    │  │ Position │  │    Risk      │  │
                    │  │  Sizing  │  │ Validation   │  │
                    │  └──────────┘  └─────────────┘  │
                    │  ┌──────────┐  ┌─────────────┐  │
                    │  │  Regime  │  │  Analysis    │  │
                    │  │Detection │  │  (18 tools)  │  │
                    │  └──────────┘  └─────────────┘  │
                    │  ┌──────────┐  ┌─────────────┐  │
                    │  │  Memory  │  │ Intelligence │  │
                    │  │  & ML    │  │ (11 tools)   │  │
                    │  └──────────┘  └─────────────┘  │
                    └──────────────┬──────────────────┘
                                   │
              ┌────────────────────┼────────────────────┐
              │                    │                    │
        ┌─────▼─────┐      ┌─────▼──────┐      ┌─────▼─────┐
        │Traditional │      │   Crypto    │      │   DeFi    │
        │  IBKR      │      │  Binance    │      │Hyperliquid│
        │  Schwab    │      │  Coinbase   │      │  dYdX     │
        │  Alpaca    │      │  Kraken     │      │  Drift    │
        └────────────┘      └────────────┘      └───────────┘
```

### Links

[systemr.ai](https://systemr.ai) · [docs.systemr.ai](https://docs.systemr.ai) · [app.systemr.ai](https://app.systemr.ai) · [agents.systemr.ai](https://agents.systemr.ai) · [sol.systemr.ai](https://sol.systemr.ai) · [PyPI](https://pypi.org/project/systemr/) · [@Systemrai](https://x.com/Systemrai) · [YouTube](https://youtube.com/@systemr_ai)
