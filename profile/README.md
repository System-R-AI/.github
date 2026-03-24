## System R AI

Build AI trading agents with institutional-grade infrastructure.

### The Platform

System R is a complete trading operating system for AI agents. 55 MCP tools deliver risk management, position sizing, compliance validation, execution routing, portfolio analytics, and real-time intelligence. Agents connect, authenticate, deposit compute credits, and operate across 25 brokers and exchanges spanning 9 asset classes.

18 statistical analysis tools cover regime detection, volatility modeling, Greeks analysis, equity curves, signal scoring, correlation matrices, and drawdown analysis. 11 intelligence tools deliver sentiment, earnings, macro, geopolitical, sector rotation, and flow analysis. Trade planning tools handle position sizing with Kelly criterion, risk of ruin, and multi-leg options structuring. Execution goes through a pre-trade gate that validates risk, compliance, and account state before any order touches a broker. Memory, ML pipelines, and journaling round out the system. 380+ API endpoints, all backed by 13,241+ verified tests.

### By the Numbers

| Metric | Value |
|---|---|
| **MCP Tools** | 55 |
| **Brokers and Exchanges** | 25 |
| **API Endpoints** | 380+ |
| **Verified Tests** | 13,241+ |
| **Asset Classes** | 9 (equities, options, futures, forex, crypto, commodities, energy, fixed income, prediction markets) |
| **Payment Methods** | 5 (OSR, SOL, USDC, USDT, PYUSD) |

### Get Started

```bash
pip install systemr
```

```python
from systemr import SystemRClient

client = SystemRClient(api_key="sr_agent_...")
gate = client.pre_trade_gate(
    symbol="AAPL", direction="long",
    entry_price="185.50", stop_price="180.00",
    equity="100000",
)

if gate["gate_passed"]:
    print(f"Buy {gate['sizing']['shares']} shares")
```

### Tool Categories

| Category | Count | Examples |
|---|---|---|
| **Core** | 4 | Pre-trade gate, position sizing, performance evaluation, pricing |
| **Analysis** | 18 | Monte Carlo, Kelly criterion, drawdown, equity curves, signal scoring |
| **Intelligence** | 11 | Regime detection, patterns, volatility surface, Greeks, correlations |
| **Planning** | 4 | Options sizing, futures sizing, trade plan builders |
| **Data** | 3 | P&L calculation, expected value, compliance |
| **System** | 5 | Signal scoring, margin, scanner evaluation |
| **Compound** | 2 | Full analysis pipeline, system assessment |
| **Memory and ML** | 7 | Persistent memory, behavioral analytics, ML prediction |
| **Journal** | 1 | Trade journaling with tagging and review |

### Supported Brokers

IBKR, Schwab, Alpaca, Tradier, Tastytrade, TradeStation, E\*TRADE, OANDA, Binance, Bybit, OKX, Coinbase, Kraken, Deribit, KuCoin, Gate.io, Gemini, Bitfinex, Hyperliquid, dYdX, Drift, Aster, Polymarket, Kalshi

### Payment

Deposit OSR, SOL, USDC, USDT, or PYUSD for compute credits. Pay per call. Presale buyers receive a permanent 20% discount on all platform operations.

### OSR Token

OSR is the compute credit token for the platform. Burn and Mint Equilibrium model on Solana. Every platform operation strengthens the token economy. 1 billion supply. Immutable. Mint authority permanently revoked. Freeze authority permanently revoked.

Token: [`E2grvu8fyeeuVaxj2DrHVBqv8j21jK3vyJpXG8FJjJNc`](https://solscan.io/token/E2grvu8fyeeuVaxj2DrHVBqv8j21jK3vyJpXG8FJjJNc) | [osrprotocol.com](https://osrprotocol.com)

### Team

**Ashim Nandi** (Founder) and **Shannon** (Co-Founder).

### Links

[agents.systemr.ai](https://agents.systemr.ai) | [systemr.ai](https://www.systemr.ai) | [osrprotocol.com](https://osrprotocol.com) | [PyPI](https://pypi.org/project/systemr/) | [X: @OsrProtocol](https://x.com/OsrProtocol)
