<p align="center">
  <a href="https://systemr.ai">
    <img src="https://raw.githubusercontent.com/System-R-AI/.github/main/assets/banner.svg" alt="System R AI" width="100%" />
  </a>
</p>

<p align="center">
  <a href="https://pypi.org/project/systemr/"><img src="https://img.shields.io/pypi/v/systemr?style=for-the-badge&color=3ECF8E&label=SDK" alt="PyPI" /></a>
  <a href="https://github.com/System-R-AI/systemr-python/blob/main/LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue?style=for-the-badge" alt="License" /></a>
</p>

<p align="center">
  <a href="https://systemr.ai">Website</a> ·
  <a href="https://docs.systemr.ai">Docs</a> ·
  <a href="https://app.systemr.ai">Platform</a> ·
  <a href="https://agents.systemr.ai">Agents API</a> ·
  <a href="https://x.com/Systemrai">X</a>
</p>

---

## What is System R

System R is an **agentic operating system for trading and investing**. It gives humans and AI agents a single platform to research markets, plan trades, execute across brokers, analyze performance, and improve through feedback — all with encrypted privacy, audit trails, and usage-based billing.

It operates across **six asset classes**:

**Equities** · **Options** · **Futures** · **Crypto** · **Prediction Markets** · **Forex**

Connected to **25 brokers and exchanges** — from Interactive Brokers and Schwab to Binance, Hyperliquid, dYdX, Polymarket, and Kalshi.

---

## What it does

System R covers the full trading lifecycle. Not just analytics — the entire operating loop.

### Research

Market regime detection (trending, ranging, volatile, quiet), structural break analysis, pattern recognition, price structure mapping, correlation matrices, liquidity profiling, options Greeks and IV surface analysis, futures curve analysis. Web research for context and news. All results feed into trade decisions.

### Planning

Position sizing using the **G-formula** (geometric growth optimization, not fixed fractional). Kelly criterion calculation. Options contract sizing from premium risk and Greeks. Futures sizing from margin and tick value. Full trade plan generation with entry, stop, target, and risk/reward profile.

### Execution

**Pre-trade gate** — one API call before every trade. Validates position size, checks risk limits (daily loss, max drawdown, correlation, concentration), detects market regime, and scores system health. Returns `APPROVED` or `BLOCKED` with the exact number of shares, contracts, or coins to trade. Cost: $0.01.

Execution routes through 25 broker adapters — place orders, manage positions, cancel, modify — all through the same API regardless of broker or asset class.

**Kill switch** — emergency halt. Stops all trading instantly when drawdown limits or consecutive loss thresholds are hit. Activate or deactivate via API, CLI, or dashboard.

### Analysis

18 statistical analysis tools: Monte Carlo simulation (1,000 equity paths), drawdown profiling, win/loss distribution, rolling consistency, execution quality scoring (slippage, MFE/MAE), segmentation by direction/asset/time, peak-valley analysis, risk-adjusted returns (Sharpe, Sortino, Calmar).

**G-Score** — System R's composite performance metric. Not just returns. Measures geometric growth quality, consistency, and edge stability. Grades your system A through F.

**Variance killer detection** — identifies the specific trades dragging performance down.

### Feedback Loop

Every trade outcome feeds back into the system. Behavioral bias detection (disposition effect, recency bias, overtrading, loss aversion). Behavioral fingerprinting (risk appetite, decision speed, adaptability). ML-based trajectory prediction. Anomaly detection for style drift. Trade clustering by outcome and strategy.

The system learns from your history and adapts its context.

### Memory

Persistent memory across sessions. Agents store insights, recall past analysis, and build knowledge over time. Six memory layers — semantic, episodic, procedural, graph, prospective, and emotional. Every query can reference what the agent has learned.

### Audit & Compliance

Full audit trail on every action. Compliance checks against configurable rule sets — position limits, concentration limits, restricted lists. Guardian system for platform-wide risk observation. Trust scoring and tier-based access control for agents.

### Encrypted Privacy

Per-agent encryption. Every agent's data is encrypted with its own key. Trading history, memory, journal entries, broker credentials — all encrypted at rest. Zero-trust architecture.

---

## How humans use it

1. **Sign up** at [app.systemr.ai](https://app.systemr.ai) — email, Google, or GitHub
2. **Verify email** and set up MFA (TOTP)
3. **Add credits** — $5 free on signup. Top up via Stripe (card) or crypto (SOL, USDC, USDT, PYUSD, OSR)
4. **Set up workspace** — choose your market (equities, crypto, options, futures, forex, prediction markets), connect a broker, configure risk limits
5. **Chat with System R** — natural language interface. Ask it to size positions, analyze your trades, detect regimes, run Monte Carlo, or build a trade plan. It picks the right tools automatically.
6. **Dashboard** — manage API keys with spending limits and operation restrictions, configure LLM preferences (auto, single model, custom mix, or bring your own key), monitor usage and billing, manage broker connections

### LLM Management

System R is **model-agnostic**. Nine models available:

| Provider | Models |
|----------|--------|
| Claude (Bedrock) | Sonnet 4.6, Opus 4.6 |
| GPT (Azure) | GPT-4o, GPT-4o Mini, GPT-5.3, GPT-5.4 Mini |
| Reasoning | O4 Mini |
| Open Source | DeepSeek R1, Llama 4 Maverick |

Four LLM modes: **Auto** (System R picks per task), **Single** (you choose one), **Custom** (mix models), **External** (bring your own Anthropic/OpenAI key — $0 LLM cost, tool calls still billed).

---

## How agents use it

Agents don't need email or passwords. They operate programmatically.

1. **Register** via API — `POST /v1/agents/register` returns an API key
2. **Or connect a Solana wallet** — wallet becomes the agent's identity
3. **Deposit credits** — SOL, USDC, USDT, PYUSD, or OSR tokens
4. **Call tools** — 55 MCP tools via REST, Python SDK, or MCP protocol
5. **Connect brokers** — authenticate and trade across 25 exchanges
6. **Scale** — multiple agents, each with isolated encryption, memory, and billing

### OSR Token Discount

Agents whose linked wallet participated in the [OSR token presale](https://osrprotocol.com) receive a **permanent 20% discount** on every tool call. Verified on-chain. The discount applies for life.

---

## Access points

| Surface | What it is | Get it |
|---------|-----------|--------|
| **Python SDK** | `pip install systemr` — 55 tools, 25 brokers, chat, BYOK | [systemr-python](https://github.com/System-R-AI/systemr-python) |
| **MCP Server** | All 55 tools in Claude Desktop, Cursor, or any MCP client | [MCP docs](https://docs.systemr.ai/mcp/overview) |
| **REST API** | Direct HTTP — 413 endpoints | [agents.systemr.ai](https://agents.systemr.ai) |
| **Web Platform** | Chat UI, dashboard, billing, broker management | [app.systemr.ai](https://app.systemr.ai) |
| **CLI** | Terminal trading OS — Bun + Ink, 12 commands, 24 slash commands | Private (coming soon) |
| **Desktop App** | Electron — macOS, Windows, Linux with native notifications | Private (coming soon) |
| **Mobile App** | Expo + React Native — iOS and Android | Private (coming soon) |

---

## 55 MCP Tools

| Category | Count | What they do |
|----------|-------|-------------|
| **Core** | 4 | Position sizing (G-formula), risk validation (Iron Fist), performance evaluation (G-Score), pricing |
| **Analysis** | 18 | Monte Carlo, Kelly criterion, drawdown, equity curves, win/loss, segmentation, correlation, execution quality, rolling G, System R Score |
| **Intelligence** | 11 | Regime detection, pattern recognition, structural breaks, trend structure, technical indicators, price structure, Greeks, IV surface, futures curve, liquidity, correlations |
| **Planning** | 4 | Options sizing, futures sizing, options trade plan, futures trade plan |
| **Data** | 3 | P&L calculation, expected value, compliance checks |
| **System** | 5 | Signal scoring, trade outcome classification, margin calculation, scanner evaluation, equity curve |
| **Compound** | 2 | Pre-trade gate ($0.01) — the one call before every trade. Full system assessment ($2.00) — quarterly review with verdict |
| **Journal** | 1 | Trade journaling with R-multiples, P&L, notes |
| **Memory & ML** | 7 | Persistent memory, behavioral biases, fingerprinting, trajectory prediction, anomaly detection, trade clustering |

Every tool is callable via `client.call_tool("tool_name", **kwargs)` or through MCP.

---

## 25 Brokers and Exchanges

| Category | Brokers |
|----------|---------|
| **Equities & Options** | Interactive Brokers, Charles Schwab, Alpaca, Tradier, Tastytrade, TradeStation, E*TRADE |
| **Forex** | OANDA |
| **Crypto (CEX)** | Binance, Bybit, OKX, Coinbase, Kraken, Deribit, KuCoin, Gate.io, Gemini, Bitfinex, Aster |
| **DeFi** | Hyperliquid, dYdX, Drift |
| **Prediction Markets** | Polymarket, Kalshi |

Same API for all of them. Connect credentials, get positions, place orders, cancel — regardless of broker or asset class.

---

## Billing

**Usage-based. No subscriptions. No minimums.** New accounts get $5 free credit.

Tool calls cost between $0.002 and $2.00 depending on the operation. LLM usage billed separately (or $0 with BYOK).

| Payment Method | Details |
|----------------|---------|
| **Stripe** | Card payment via checkout |
| **SOL** | Solana native token |
| **USDC / USDT / PYUSD** | Stablecoins on Solana |
| **OSR** | Compute credit token — 70% burned, 30% retained. Presale buyers get **permanent 20% discount**. |

API key management includes per-key spending limits (daily and monthly caps) and operation-level restrictions.

---

## The workflow

```
  ┌──────────────────────────────────────────────────────────────────────┐
  │                     Human or AI Agent                               │
  │         (Web App · CLI · Desktop · Mobile · SDK · MCP)              │
  └───────────────────────────────┬──────────────────────────────────────┘
                                  │
                    SDK / MCP / REST API (413 endpoints)
                                  │
  ┌───────────────────────────────▼──────────────────────────────────────┐
  │                         System R Platform                           │
  │                                                                     │
  │  ┌─────────────┐ ┌─────────────┐ ┌─────────────┐ ┌──────────────┐  │
  │  │  Research    │ │  Planning   │ │  Execution  │ │  Analysis    │  │
  │  │             │ │             │ │             │ │              │  │
  │  │ Regime      │ │ G-Formula   │ │ Pre-Trade   │ │ G-Score      │  │
  │  │ Patterns    │ │ Kelly       │ │ Gate        │ │ Monte Carlo  │  │
  │  │ Structural  │ │ Options     │ │ Kill Switch │ │ Drawdown     │  │
  │  │ Breaks      │ │ Futures     │ │ Order       │ │ Win/Loss     │  │
  │  │ Indicators  │ │ Trade Plans │ │ Routing     │ │ Segmentation │  │
  │  │ Correlations│ │             │ │             │ │ Equity Curve │  │
  │  └─────────────┘ └─────────────┘ └─────────────┘ └──────────────┘  │
  │                                                                     │
  │  ┌─────────────┐ ┌─────────────┐ ┌─────────────┐ ┌──────────────┐  │
  │  │  Memory     │ │  Feedback   │ │  Security   │ │  Billing     │  │
  │  │             │ │             │ │             │ │              │  │
  │  │ 6-Layer     │ │ Bias        │ │ Per-Agent   │ │ Usage-Based  │  │
  │  │ Persistent  │ │ Detection   │ │ Encryption  │ │ Compute      │  │
  │  │ Semantic    │ │ Fingerprint │ │ Audit Trail │ │ Credits      │  │
  │  │ Episodic    │ │ Trajectory  │ │ Guardian    │ │ BYOK         │  │
  │  │ Procedural  │ │ Anomaly     │ │ Trust Score │ │ OSR/SOL/USDC │  │
  │  │ Graph       │ │ Clustering  │ │ Compliance  │ │ Stripe       │  │
  │  └─────────────┘ └─────────────┘ └─────────────┘ └──────────────┘  │
  │                                                                     │
  │                    187 Domain Services · 13,500+ Tests              │
  └───────────────────────────────┬──────────────────────────────────────┘
                                  │
          ┌───────────────────────┼───────────────────────┐
          │                       │                       │
  ┌───────▼────────┐    ┌────────▼────────┐    ┌─────────▼────────┐
  │  Traditional   │    │     Crypto      │    │  DeFi & Predict  │
  │                │    │                 │    │                  │
  │  IBKR          │    │  Binance        │    │  Hyperliquid     │
  │  Schwab        │    │  Bybit          │    │  dYdX            │
  │  Alpaca        │    │  OKX            │    │  Drift           │
  │  Tastytrade    │    │  Coinbase       │    │  Polymarket      │
  │  TradeStation  │    │  Kraken         │    │  Kalshi          │
  │  E*TRADE       │    │  Deribit        │    │                  │
  │  Tradier       │    │  KuCoin +4 more │    │                  │
  │  OANDA (FX)    │    │                 │    │                  │
  └────────────────┘    └─────────────────┘    └──────────────────┘
```

---

## Quick start

```bash
pip install systemr
```

```python
from systemr import SystemRClient

client = SystemRClient(api_key="sr_agent_...")

# One call before every trade — sizing, risk, regime, health
gate = client.pre_trade_gate(
    symbol="AAPL", direction="long",
    entry_price="185.50", stop_price="180.00",
    equity="100000",
)

if gate["gate_passed"]:
    print(f"Buy {gate['sizing']['shares']} shares")
    # → APPROVED: 160 shares, risk $800 (1.6%), G-Score: 1.12
```

Works across every asset class:

```python
client.pre_trade_gate(symbol="BTC-USDT", direction="long", ...)      # Crypto
client.pre_trade_gate(symbol="EUR-USD", direction="short", ...)       # Forex
client.calculate_options_size(symbol="SPY", strike="530", ...)        # Options
client.calculate_futures_size(symbol="ES", direction="long", ...)     # Futures
client.pre_trade_gate(symbol="TRUMP-WIN", direction="long", ...)     # Prediction Markets
```

---

## Repositories

| Repo | What it is |
|------|-----------|
| [**systemr-python**](https://github.com/System-R-AI/systemr-python) | Python SDK — `pip install systemr` — 55 tools, 25 brokers, chat, BYOK |
| [**demo-trading-agent**](https://github.com/System-R-AI/demo-trading-agent) | Reference agent — momentum strategy with pre-trade risk gates. 53 trades gated, max drawdown 9%. |

---

## Links

[systemr.ai](https://systemr.ai) · [docs.systemr.ai](https://docs.systemr.ai) · [app.systemr.ai](https://app.systemr.ai) · [agents.systemr.ai](https://agents.systemr.ai) · [sol.systemr.ai](https://sol.systemr.ai) · [PyPI](https://pypi.org/project/systemr/) · [@Systemrai](https://x.com/Systemrai) · [YouTube](https://youtube.com/@systemr_ai)
