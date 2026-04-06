<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/System-R-AI/.github/main/assets/banner.svg">
  <img alt="System R AI — The Trading Operating System for AI Agents" src="https://raw.githubusercontent.com/System-R-AI/.github/main/assets/banner.svg" width="100%">
</picture>

<p align="center">
  <a href="https://docs.systemr.ai">Documentation</a> &nbsp;&middot;&nbsp;
  <a href="https://app.systemr.ai">Web App</a> &nbsp;&middot;&nbsp;
  <a href="https://pypi.org/project/systemr/">Python SDK</a> &nbsp;&middot;&nbsp;
  <a href="https://agents.systemr.ai/openapi.json">OpenAPI Spec</a> &nbsp;&middot;&nbsp;
  <a href="https://docs.systemr.ai/billing/pricing">Pricing</a>
</p>

---

**System R is the operating system for trading and investment** — for humans and AI agents.

Research. Planning. Execution. Trade management. Journaling. Data analysis. Feedback loop. All with encrypted privacy, a complete audit trail, and cognitive memory that compounds over time.

55 tools across six layers. 25 brokers and exchanges across equities, options, futures, crypto, forex, and prediction markets. One platform that covers the full lifecycle of every trade. System R operates through its own specialized agentic system — domain-expert workflows that reason about risk, markets, and portfolio construction, not generalized LLM responses.

**Humans**: Sign up at [systemr.ai](https://app.systemr.ai) and get **$5 free compute credits** to start. Voice chat available. Use it through the **[web app](https://app.systemr.ai)**, the **[desktop CLI](https://github.com/System-R-AI/systemr-cli)**, or the **[mobile app](https://github.com/System-R-AI/systemr-mobile)**.

**AI Agents**: No signup required. Connect via **[MCP protocol](https://docs.systemr.ai/mcp/overview)**, **[Python SDK](https://pypi.org/project/systemr/)**, or **[REST API](https://agents.systemr.ai/openapi.json)** — or pay per call with a Solana wallet using x402, no account needed.

Pay only for what you use. Every tool call is a micro-transaction on a **usage-based compute credit** system — no subscriptions, no monthly fees, credits never expire. The **[OSR token](https://solscan.io/token/E2grvu8fyeeuVaxj2DrHVBqv8j21jK3vyJpXG8FJjJNc)** is the native compute credit on Solana — pay with OSR for a 50% credit bonus and connect DeFi liquidity directly into your trading infrastructure via [sol.systemr.ai](https://sol.systemr.ai).

---

### How it works

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/System-R-AI/.github/main/assets/architecture.svg">
  <img alt="System R Architecture — Agent to System R to Markets" src="https://raw.githubusercontent.com/System-R-AI/.github/main/assets/architecture.svg" width="100%">
</picture>

<br>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/System-R-AI/.github/main/assets/trade-flow.svg">
  <img alt="One API call — what happens inside" src="https://raw.githubusercontent.com/System-R-AI/.github/main/assets/trade-flow.svg" width="100%">
</picture>

---

### Try it

```bash
pip install systemr
```

```python
from systemr import SystemRClient

client = SystemRClient(api_key="sr_agent_...")

# One call: position sizing + risk validation + system health
gate = client.pre_trade_gate(
    symbol="AAPL",
    direction="long",
    entry_price="185.50",
    stop_price="180.00",
    equity="100000",
)

gate["gate_passed"]       # True
gate["sizing"]["shares"]  # 363
gate["risk"]["score"]     # 23
```

Or use the REST API directly:

```bash
curl -X POST https://agents.systemr.ai/v1/tools/call \
  -H "X-API-Key: sr_agent_..." \
  -H "Content-Type: application/json" \
  -d '{"tool": "pre_trade_gate", "params": {"symbol": "AAPL", "direction": "long", "entry_price": "185.50", "stop_price": "180.00", "equity": "100000"}}'
```

---

### 55 tools, six layers

<details>
<summary><strong>Risk</strong> — 12 tools &nbsp; <sub>Position sizing, validation, and controls</sub></summary>
<br>

| Tool | What it does | Cost |
|:-----|:-------------|:-----|
| `calculate_position_size` | G-formula geometric growth optimization | $0.003 |
| `check_trade_risk` | Iron Fist risk validation (position + portfolio + daily limits) | $0.004 |
| `evaluate_performance` | G-metric analysis — score, grade, rolling trend | $0.10 — $1.00 |
| `analyze_drawdown` | Drawdown periods, depth, recovery time | $0.005 |
| `run_monte_carlo` | 1,000–10,000 simulated equity paths | $0.008 |
| `calculate_kelly` | Kelly criterion (full, half, quarter) | $0.004 |
| `find_variance_killers` | Trades that damage geometric growth | $0.006 |
| `analyze_win_loss` | Win/loss statistics and streaks | $0.004 |
| `run_what_if` | G-improvement scenarios | $0.008 |
| `analyze_confidence` | Confidence intervals on R-multiples | $0.005 |
| `analyze_risk_adjusted` | Sharpe, Sortino, Calmar ratios | $0.005 |
| `calculate_system_r_score` | Composite score 0–100, grade A+ through F | $0.005 |

</details>

<details>
<summary><strong>Intelligence</strong> — 11 tools &nbsp; <sub>Market regime, patterns, and signals</sub></summary>
<br>

| Tool | What it does | Cost |
|:-----|:-------------|:-----|
| `detect_patterns` | Breakouts, pullbacks, MA crossovers, RSI divergences, gaps | $0.008 |
| `detect_structural_break` | Distribution break detection (recent vs historical) | $0.006 |
| `analyze_trend_structure` | Bollinger/ATR expansion, compression, squeeze detection | $0.006 |
| `calculate_indicators` | SMA, EMA, RSI, MACD, Bollinger Bands, ATR | $0.004 |
| `analyze_price_structure` | Support/resistance, swing points, consolidation zones | $0.006 |
| `analyze_correlations` | Multi-symbol correlation matrix | $0.008 |
| `analyze_liquidity` | Volume analysis — normal, thinning, stressed, spike | $0.004 |
| `analyze_greeks` | Options Greeks portfolio exposure | $0.006 |
| `analyze_iv_surface` | Implied volatility surface structure | $0.008 |
| `analyze_futures_curve` | Term structure — contango, backwardation, flat | $0.006 |
| `analyze_options_flow` | Options order flow directional signals | $0.006 |

</details>

<details>
<summary><strong>Analysis</strong> — 18 tools &nbsp; <sub>Statistical analysis and diagnostics</sub></summary>
<br>

| Tool | What it does | Cost |
|:-----|:-------------|:-----|
| `analyze_consistency` | Behavioral drift detection | $0.005 |
| `analyze_correlation` | Serial correlation in trade outcomes | $0.005 |
| `analyze_distribution` | Skewness, kurtosis, normality testing | $0.005 |
| `analyze_recovery` | Recovery patterns after drawdowns | $0.005 |
| `segment_trades` | G-metrics by symbol, day, strategy, or regime | $0.005 |
| `analyze_execution_quality` | MAE/MFE analysis | $0.005 |
| `detect_peak_valley` | Peaks and valleys in equity curve | $0.005 |
| `calculate_rolling_g` | Rolling G over sliding windows | $0.005 |
| `calculate_equity_curve` | Equity curve from trade history | $0.004 |
| `score_signal` | Signal quality scoring | $0.003 |
| `analyze_trade_outcome` | Individual trade outcome analysis | $0.003 |
| `calculate_margin` | Margin requirement calculation | $0.002 |
| `evaluate_scanner` | Scanner/screener evaluation | $0.005 |
| `calculate_pnl` | Profit/loss calculation | $0.003 |
| `calculate_expected_value` | Expected value per trade | $0.004 |
| `check_compliance` | Compliance rule validation | $0.004 |
| `detect_regime` | Market regime classification | $0.006 |
| `detect_anomalies` | Trades deviating from your patterns | $0.006 |

</details>

<details>
<summary><strong>Planning</strong> — 4 tools &nbsp; <sub>Options and futures position building</sub></summary>
<br>

| Tool | What it does | Cost |
|:-----|:-------------|:-----|
| `size_options_position` | 4 modes: equity risk, premium, delta-adjusted, spread | $0.004 |
| `size_futures_position` | 3 modes: margin-based, tick value, notional | $0.004 |
| `build_options_plan` | Complete options plan from thesis (bullish/bearish/neutral/volatile) | $0.008 |
| `build_futures_plan` | Structured futures plan with entry, stop, and target | $0.008 |

</details>

<details>
<summary><strong>Execution</strong> — 25 brokers &nbsp; <sub>Trade across every asset class</sub></summary>
<br>

| Category | Brokers |
|:---------|:--------|
| **Equities & Options** | Interactive Brokers, Charles Schwab, Alpaca, Tradier, Tastytrade, TradeStation, E\*TRADE |
| **Crypto** | Binance, Bybit, OKX, Coinbase, Kraken, Deribit, KuCoin, Gate.io, Gemini, Bitfinex, Aster |
| **DeFi** | Hyperliquid, dYdX, Drift |
| **Forex** | OANDA |
| **Prediction Markets** | Polymarket, Kalshi |
| **Paper Trading** | Demo broker (sandbox mode) |

All broker credentials encrypted per-agent. Decrypted only at moment of execution. $0.015 per order.

</details>

<details>
<summary><strong>Memory</strong> — 8 tools &nbsp; <sub>Learning, biases, and behavioral analysis</sub></summary>
<br>

| Tool | What it does | Cost |
|:-----|:-------------|:-----|
| `store_memory` | Encrypted memory storage with categories | $0.003 |
| `search_memory` | Semantic similarity search across memories | $0.003 |
| `get_trading_biases` | Detects disposition effect, recency bias, overtrading, loss aversion, anchoring | $0.005 |
| `get_behavioral_fingerprint` | Trading style: risk profile, hold duration, concentration, streaks | $0.005 |
| `predict_trajectory` | Performance forecast over next N trades | $0.008 |
| `detect_anomalies` | Extreme wins/losses, pattern breaks | $0.006 |
| `cluster_trades` | Groups trades by outcome patterns | $0.006 |
| `record_trade_journal` | Log completed trades with R-multiple, P&L, and notes | $0.003 |

</details>

---

### Connect any agent

System R is an MCP server. Any AI agent that speaks MCP can discover and call all 55 tools natively.

<details>
<summary><strong>Claude Desktop</strong></summary>
<br>

Add to `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) or `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{
  "mcpServers": {
    "systemr": {
      "transport": { "type": "sse", "url": "https://agents.systemr.ai/mcp/sse" },
      "metadata": { "api_key": "sr_agent_YOUR_KEY_HERE" }
    }
  }
}
```

</details>

<details>
<summary><strong>Claude Code</strong></summary>
<br>

```bash
claude mcp add systemr
```

</details>

<details>
<summary><strong>Cursor</strong></summary>
<br>

Add to `.cursor/mcp.json` in your project root:

```json
{
  "mcpServers": {
    "systemr": {
      "transport": { "type": "sse", "url": "https://agents.systemr.ai/mcp/sse" },
      "metadata": { "api_key": "sr_agent_YOUR_KEY_HERE" }
    }
  }
}
```

</details>

<details>
<summary><strong>Any MCP client</strong></summary>
<br>

SSE endpoint: `https://agents.systemr.ai/mcp/sse`

Pass your API key in session metadata. All 55 tools auto-discovered by the client.

</details>

<details>
<summary><strong>Python SDK</strong></summary>
<br>

```bash
pip install systemr
```

```python
from systemr import SystemRClient
client = SystemRClient(api_key="sr_agent_...")
```

Single dependency (httpx). Python 3.9+.

</details>

<details>
<summary><strong>REST API</strong></summary>
<br>

Base URL: `https://agents.systemr.ai`

```bash
curl -X POST https://agents.systemr.ai/v1/tools/call \
  -H "X-API-Key: sr_agent_..." \
  -H "Content-Type: application/json" \
  -d '{"tool": "calculate_position_size", "params": {...}}'
```

Full spec: [`agents.systemr.ai/openapi.json`](https://agents.systemr.ai/openapi.json)

</details>

---

### Security

| | |
|:--|:--|
| **Per-agent encryption** | AES encryption with unique keys derived from agent identity. Credentials, strategies, wallet data, and memories encrypted at rest. Only the owning agent can decrypt. System R operators cannot read agent data. |
| **Complete audit trail** | Every data read, risk check, and decision logged with timestamps. What was read, what passed, what was decided and why. Queryable via API. |
| **Zero-trust architecture** | Platform Guardian monitors all activity. Threat scoring, rate limiting, session binding, request signing. |
| **Agent isolation** | Each agent has separate keys, credits, broker connections, encryption keys, and audit trails. Agent A cannot access Agent B's data. |

---

### Pricing

**Usage-based. No subscriptions. No monthly fees.** $5 free credits on signup. Credits never expire. Balance stops at $0 — no surprise charges.

#### Tool calls

| Category | Price range | Examples |
|:---------|:-----------|:---------|
| **Core** | $0.003 – $1.00 | Position sizing ($0.003), risk validation ($0.004), performance eval ($0.10–$1.00) |
| **Analysis** | $0.004 – $0.008 | Monte Carlo ($0.008), Kelly criterion ($0.004), drawdown ($0.005) |
| **Intelligence** | $0.004 – $0.008 | Pattern detection ($0.008), regime detection ($0.006), Greeks ($0.006) |
| **Planning** | $0.004 – $0.008 | Options sizing ($0.004), full options plan ($0.008) |
| **Memory & ML** | $0.003 – $0.008 | Store/search memory ($0.003), bias detection ($0.005), trajectory ($0.008) |
| **Compound** | $0.01 – $2.00 | Pre-trade gate ($0.01), full system assessment ($2.00) |
| **Execution** | $0.015 | Broker order |

#### LLM models (per 1M tokens)

Use System R's hosted models, or bring your own key.

| Model | Input | Output |
|:------|:------|:-------|
| GPT-4o Mini | $0.15 | $0.60 |
| Llama 4 Maverick | $0.50 | $0.77 |
| GPT-5.4 Mini | $0.50 | $2.00 |
| o4 Mini | $1.10 | $4.40 |
| DeepSeek R1 | $0.55 | $2.19 |
| GPT-4o | $2.50 | $10.00 |
| GPT-5.3 | $5.00 | $15.00 |
| Claude Sonnet 4.6 | $9.00 | $45.00 |
| Claude Opus 4.6 | $45.00 | $225.00 |

**BYOK** (Bring Your Own Key): Connect your own Anthropic or OpenAI API key. LLM usage billed directly by the provider — System R charges only for tool calls.

#### Real-world cost examples

| Workflow | Cost |
|:---------|:-----|
| Single pre-trade gate | $0.01 |
| Position size + risk check | $0.007 |
| Backtest diagnostic (6 tools) | ~$0.032 |
| Chat session (Sonnet, ~2K tokens) | ~$0.10 |
| Chat session (Opus, ~2K tokens) | ~$0.50 |
| 100 pre-trade gates / day | $1.00 |
| 1,000 position sizing calls | $3.00 |
| Full system assessment (7 tools) | $2.00 |

#### Payment methods

| Method | Rate | Min / Max |
|:-------|:-----|:----------|
| Card (Stripe) | 1:1 USD | $5 – $10,000 |
| USDC / USDT / PYUSD | 1:1 USD | Solana mainnet |
| SOL | Live market rate (CoinGecko) | Solana mainnet |
| [OSR token](https://solscan.io/token/E2grvu8fyeeuVaxj2DrHVBqv8j21jK3vyJpXG8FJjJNc) | Market price + **50% bonus** | 70% burned, 30% retained |

**OSR presale buyers** receive a **permanent 20% discount** on all platform operations — stacks with the 50% credit bonus.

Full pricing details: **[docs.systemr.ai/billing/pricing](https://docs.systemr.ai/billing/pricing)**

---

### Get started

**1. Register an agent**

```bash
curl -X POST https://agents.systemr.ai/v1/agents/register \
  -H "Content-Type: application/json" \
  -d '{"owner_id": "you", "agent_name": "my-agent", "agent_type": "trading"}'
```

You receive an API key (`sr_agent_...`). Shown once. $5 free credits loaded.

**2. Install the SDK**

```bash
pip install systemr
```

**3. Make your first call**

```python
from systemr import SystemRClient

client = SystemRClient(api_key="sr_agent_...")
gate = client.pre_trade_gate(
    symbol="AAPL", direction="long",
    entry_price="185.50", stop_price="180.00",
    equity="100000",
)
```

**4. Connect a broker** (when ready)

```python
client.connect_broker("alpaca", {
    "api_key": "...",
    "api_secret": "...",
    "paper": True
})
```

Full walkthrough: [docs.systemr.ai/getting-started/quickstart](https://docs.systemr.ai/getting-started/quickstart)

---

### OSR Token

OSR is the compute credit token for the System R platform, built on Solana.

- Burn and Mint Equilibrium: 70% of OSR payments burned, 30% retained
- 1B fixed supply. Mint authority revoked. Freeze authority revoked.
- Presale buyers receive a **permanent 20% discount** on all platform operations
- Pay with OSR for a **50% credit bonus**

Token: [`E2grvu8fyeeuVaxj2DrHVBqv8j21jK3vyJpXG8FJjJNc`](https://solscan.io/token/E2grvu8fyeeuVaxj2DrHVBqv8j21jK3vyJpXG8FJjJNc) &nbsp;&middot;&nbsp; [osrprotocol.com](https://osrprotocol.com)

---

### Repositories

| Repo | What it is |
|:-----|:-----------|
| [`systemr-python`](https://github.com/System-R-AI/systemr-python) | Python SDK — `pip install systemr` |
| [`demo-trading-agent`](https://github.com/System-R-AI/demo-trading-agent) | Reference agent showing System R integration |
| [`sol-systemr`](https://github.com/System-R-AI/sol-systemr) | Solana RWA Intelligence Hub — [sol.systemr.ai](https://sol.systemr.ai) |
| [`systemr-cli`](https://github.com/System-R-AI/systemr-cli) | Terminal client for System R |

---

<p align="center">
  <a href="https://www.systemr.ai">systemr.ai</a> &nbsp;&middot;&nbsp;
  <a href="https://docs.systemr.ai">docs</a> &nbsp;&middot;&nbsp;
  <a href="https://app.systemr.ai">app</a> &nbsp;&middot;&nbsp;
  <a href="https://agents.systemr.ai">api</a> &nbsp;&middot;&nbsp;
  <a href="https://sol.systemr.ai">sol</a> &nbsp;&middot;&nbsp;
  <a href="https://x.com/Systemrai">@Systemrai</a> &nbsp;&middot;&nbsp;
  <a href="https://youtube.com/@systemr_ai">YouTube</a> &nbsp;&middot;&nbsp;
  <a href="mailto:hello@systemr.ai">hello@systemr.ai</a>
</p>

<p align="center"><sub>&copy; 2026 System R AI &nbsp;&middot;&nbsp; Software platform &nbsp;&middot;&nbsp; Not financial advice</sub></p>
