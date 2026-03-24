## System R AI

**Trading and investment operating system for AI agents**

### The Platform

System R is not a chatbot that answers questions about markets. It is a complete operating system where AI agents get the same infrastructure that institutional trading desks rely on: risk management, position sizing, compliance validation, execution routing, portfolio analytics, and real-time intelligence. Agents connect, authenticate, deposit compute credits, and operate across 25 brokers and exchanges spanning 9 asset classes.

Every tool is built for programmatic access. 18 statistical analysis tools cover regime detection, volatility modeling, Greeks analysis, equity curves, signal scoring, correlation matrices, and drawdown analysis. 11 intelligence tools deliver sentiment, earnings, macro, geopolitical, sector rotation, and flow analysis. Trade planning tools handle position sizing with Kelly criterion, risk of ruin, and multi-leg options structuring. Execution goes through a pre-trade gate that validates risk, compliance, and account state before any order touches a broker. Memory, ML pipelines, and journaling round out the system. 380+ API endpoints, all backed by 13,241+ verified tests.

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

**1. Register**
```bash
curl -X POST https://agents.systemr.ai/api/v1/auth/register \
  -H "Content-Type: application/json" \
  -d '{"email": "agent@example.com", "password": "your-password"}'
```

**2. Install**
```bash
pip install systemr
```

**3. Call**
```python
from systemr import SystemRClient

client = SystemRClient(api_key="sr_agent_...")
gate = client.pre_trade_gate(
    symbol="AAPL", direction="long",
    entry_price="185.50", stop_price="180.00",
    equity="100000",
)
```

### Tool Categories

| Category | Count | Examples |
|---|---|---|
| **Core** | 4 | Pre-trade gate, portfolio snapshot, account overview, order management |
| **Analysis** | 18 | Regime detection, volatility modeling, Greeks, equity curves, signal scoring, correlation |
| **Intelligence** | 11 | Sentiment, earnings, macro, geopolitical, sector rotation, flow analysis |
| **Planning** | 4 | Position sizing, Kelly criterion, risk of ruin, multi-leg structuring |
| **Data** | 3 | Market data, historical bars, options chains |
| **System** | 5 | Health, usage, rate limits, API keys, webhooks |
| **Compound** | 2 | Full analysis pipeline, research-to-trade workflow |
| **Memory and ML** | 7 | Pattern storage, model training, prediction, feature engineering |
| **Journal** | 1 | Trade journaling with tagging and review |

### Supported Brokers

IBKR, Schwab, Alpaca, Tradier, Tastytrade, TradeStation, E\*TRADE, OANDA, Binance, Bybit, OKX, Coinbase, Kraken, Deribit, KuCoin, Gate.io, Gemini, Bitfinex, Hyperliquid, dYdX, Drift, Aster, Polymarket, Kalshi

### Payment

Deposit OSR, SOL, USDC, USDT, or PYUSD for compute credits. No free tier. Every API call costs credits. Presale buyers get a permanent 20% discount on all platform operations.

### OSR Token

OSR is the compute credit token for the platform. Burn and Mint Equilibrium model on Solana. Every platform operation burns tokens, so supply decreases as usage grows. 1B total supply, mint authority revoked, freeze authority revoked.

Token: [`E2grvu8fyeeuVaxj2DrHVBqv8j21jK3vyJpXG8FJjJNc`](https://solscan.io/token/E2grvu8fyeeuVaxj2DrHVBqv8j21jK3vyJpXG8FJjJNc) | [osrprotocol.com](https://osrprotocol.com)

### Team

**Ashim Nandi** (Founder) and **Shannon** (Co-Founder).

### Links

[agents.systemr.ai](https://agents.systemr.ai) | [systemr.ai](https://www.systemr.ai) | [osrprotocol.com](https://osrprotocol.com) | [PyPI](https://pypi.org/project/systemr/) | [X: @OsrProtocol](https://x.com/OsrProtocol)
