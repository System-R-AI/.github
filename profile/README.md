<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/System-R-AI/.github/main/assets/hero.svg">
  <img alt="System R AI — The Trading Operating System for AI Agents" src="https://raw.githubusercontent.com/System-R-AI/.github/main/assets/hero.svg" width="100%">
</picture>

<p align="center">
  <a href="https://docs.systemr.ai">Documentation</a> &nbsp;&middot;&nbsp;
  <a href="https://app.systemr.ai">Web App</a> &nbsp;&middot;&nbsp;
  <a href="https://pypi.org/project/systemr/">Python SDK</a> &nbsp;&middot;&nbsp;
  <a href="https://agents.systemr.ai">API</a> &nbsp;&middot;&nbsp;
  <a href="https://docs.systemr.ai/billing/pricing">Pricing</a>
</p>

---

**System R is the operating system for trading and investment**, for humans and AI agents.

Research. Planning. Execution. Trade management. Journaling. Data analysis. Feedback loop. All with encrypted privacy, a complete audit trail, and cognitive memory that compounds over time.

68 tools across six layers. 25 brokers and exchanges across equities, options, futures, crypto, forex, and prediction markets. One platform that covers the full lifecycle of every trade. System R operates through its own specialized agentic system with domain-expert workflows that reason about risk, markets, and portfolio construction, not generalized LLM responses.

System R handles model selection automatically. A proprietary routing protocol assigns each task to the best-qualified model from a curated stack of 7 LLMs, optimized for trading and investment workflows. No manual model selection, no configuration needed.

The platform is model-agnostic by design. Your workflows stay continuous even if any single provider becomes unavailable. System R's value is the specialized domain layer, anchored in the G-formula: **G = E[R] - σ²/2**, where geometric growth is maximized by increasing expected return while minimizing variance drag. Every tool in the platform exists to answer one question: how does this affect my G? Intelligence is just a layer on top of it.

**Humans**: Sign up at [systemr.ai](https://app.systemr.ai) and get **$5 free compute credits** to start. Voice chat available. Use it through the **[web app](https://app.systemr.ai)** — desktop CLI and mobile apps coming soon.

**AI Agents**: No signup required. Connect via **[MCP protocol](https://docs.systemr.ai/mcp/overview)**, **[Python SDK](https://pypi.org/project/systemr/)**, or **[REST API](https://agents.systemr.ai/openapi.json)**. Agents can also pay per call with a Solana wallet using x402, no account needed.

**Fair, transparent pricing.** All 68 tools are completely free. You only pay when an LLM is used. Cost varies by query complexity. No subscriptions, no monthly fees, credits never expire. Fund your account with Stripe, stablecoins (USDC/USDT/PYUSD), SOL, or the **[OSR token](https://solscan.io/token/E2grvu8fyeeuVaxj2DrHVBqv8j21jK3vyJpXG8FJjJNc)** for a 50% credit bonus.

The OSR token, issued by OSR Protocol, is the native compute credit on Solana with a 50% credit bonus on every deposit. System R uses Solana through OSR Protocol as its agentic settlement and payment layer. Solana's sub-second finality, near-zero transaction costs, native stablecoin infrastructure, and tokenization capabilities make it the natural settlement rail for autonomous agents operating across global markets.

Explore Solana RWA intelligence at [sol.systemr.ai](https://sol.systemr.ai).

---

### Security

| | |
|:--|:--|
| **Per-agent encryption** | AES encryption with unique keys derived from agent identity. Credentials, strategies, wallet data, and memories encrypted at rest. Only the owning agent can decrypt. System R operators cannot read agent data. |
| **Complete audit trail** | Every data read, risk check, and decision logged with timestamps. What was read, what passed, what was decided and why. Queryable via API. |
| **Zero-trust architecture** | Platform Guardian monitors all activity. Threat scoring, rate limiting, session binding, request signing. |
| **Agent isolation** | Each agent has separate keys, credits, broker connections, encryption keys, and audit trails. Agent A cannot access Agent B's data. |

---

### How it works

<img src="https://raw.githubusercontent.com/System-R-AI/.github/main/assets/system-r-arch.svg" alt="System R Architecture" width="100%">

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

### 68 tools, six layers — all free

<details>
<summary><strong>Risk</strong> | 12 tools &nbsp; <sub>Position sizing, validation, and controls</sub></summary>
<br>

| Tool | What it does |
|:-----|:-------------|
| `calculate_position_size` | G-formula geometric growth optimization |
| `check_trade_risk` | Iron Fist risk validation (position + portfolio + daily limits) |
| `evaluate_performance` | G-metric analysis (score, grade, rolling trend) |
| `analyze_drawdown` | Drawdown periods, depth, recovery time |
| `run_monte_carlo` | 1,000-10,000 simulated equity paths |
| `calculate_kelly` | Kelly criterion (full, half, quarter) |
| `find_variance_killers` | Trades that damage geometric growth |
| `analyze_win_loss` | Win/loss statistics and streaks |
| `run_what_if` | G-improvement scenarios |
| `analyze_confidence` | Confidence intervals on R-multiples |
| `analyze_risk_adjusted` | Sharpe, Sortino, Calmar ratios |
| `calculate_system_r_score` | Composite score 0-100, grade A+ through F |

</details>

<details>
<summary><strong>Intelligence</strong> | 11 tools &nbsp; <sub>Market regime, patterns, and signals</sub></summary>
<br>

| Tool | What it does |
|:-----|:-------------|
| `detect_patterns` | Breakouts, pullbacks, MA crossovers, RSI divergences, gaps |
| `detect_structural_break` | Distribution break detection (recent vs historical) |
| `analyze_trend_structure` | Bollinger/ATR expansion, compression, squeeze detection |
| `calculate_indicators` | SMA, EMA, RSI, MACD, Bollinger Bands, ATR |
| `analyze_price_structure` | Support/resistance, swing points, consolidation zones |
| `analyze_correlations` | Multi-symbol correlation matrix |
| `analyze_liquidity` | Volume analysis (normal, thinning, stressed, spike) |
| `analyze_greeks` | Options Greeks portfolio exposure |
| `analyze_iv_surface` | Implied volatility surface structure |
| `analyze_futures_curve` | Term structure (contango, backwardation, flat) |
| `analyze_options_flow` | Options order flow directional signals |

</details>

<details>
<summary><strong>Analysis</strong> | 18 tools &nbsp; <sub>Statistical analysis and diagnostics</sub></summary>
<br>

| Tool | What it does |
|:-----|:-------------|
| `analyze_consistency` | Behavioral drift detection |
| `analyze_correlation` | Serial correlation in trade outcomes |
| `analyze_distribution` | Skewness, kurtosis, normality testing |
| `analyze_recovery` | Recovery patterns after drawdowns |
| `segment_trades` | G-metrics by symbol, day, strategy, or regime |
| `analyze_execution_quality` | MAE/MFE analysis |
| `detect_peak_valley` | Peaks and valleys in equity curve |
| `calculate_rolling_g` | Rolling G over sliding windows |
| `calculate_equity_curve` | Equity curve from trade history |
| `score_signal` | Signal quality scoring |
| `analyze_trade_outcome` | Individual trade outcome analysis |
| `calculate_margin` | Margin requirement calculation |
| `evaluate_scanner` | Scanner/screener evaluation |
| `calculate_pnl` | Profit/loss calculation |
| `calculate_expected_value` | Expected value per trade |
| `check_compliance` | Compliance rule validation |
| `detect_regime` | Market regime classification |
| `detect_anomalies` | Trades deviating from your patterns |

</details>

<details>
<summary><strong>Planning</strong> | 4 tools &nbsp; <sub>Options and futures position building</sub></summary>
<br>

| Tool | What it does |
|:-----|:-------------|
| `size_options_position` | 4 modes: equity risk, premium, delta-adjusted, spread |
| `size_futures_position` | 3 modes: margin-based, tick value, notional |
| `build_options_plan` | Complete options plan from thesis (bullish/bearish/neutral/volatile) |
| `build_futures_plan` | Structured futures plan with entry, stop, and target |

</details>

<details>
<summary><strong>Market Data</strong> | 5 tools &nbsp; <sub>Live quotes, news, and screening</sub></summary>
<br>

| Tool | What it does |
|:-----|:-------------|
| `get_stock_quote` | Real-time stock quotes |
| `get_market_movers` | Top gainers, losers, and most active |
| `get_market_overview` | Broad market summary |
| `search_news` | Market news search |
| `scan_market` | Screen instruments by custom criteria |

</details>

<details>
<summary><strong>Execution</strong> | 25 brokers &nbsp; <sub>Trade across every asset class</sub></summary>
<br>

| Category | Brokers |
|:---------|:--------|
| **Equities & Options** | Interactive Brokers, Charles Schwab, Alpaca, Tradier, Tastytrade, TradeStation, E\*TRADE |
| **Crypto** | Binance, Bybit, OKX, Coinbase, Kraken, Deribit, KuCoin, Gate.io, Gemini, Bitfinex, Aster |
| **DeFi** | Hyperliquid, dYdX, Drift |
| **Forex** | OANDA |
| **Prediction Markets** | Polymarket, Kalshi |
| **Paper Trading** | Demo broker (sandbox mode) |

All broker credentials encrypted per-agent. Decrypted only at moment of execution.

</details>

<details>
<summary><strong>Memory</strong> | 8 tools &nbsp; <sub>Learning, biases, and behavioral analysis</sub></summary>
<br>

| Tool | What it does |
|:-----|:-------------|
| `store_memory` | Encrypted memory storage with categories |
| `search_memory` | Semantic similarity search across memories |
| `get_trading_biases` | Detects disposition effect, recency bias, overtrading, loss aversion, anchoring |
| `get_behavioral_fingerprint` | Trading style: risk profile, hold duration, concentration, streaks |
| `predict_trajectory` | Performance forecast over next N trades |
| `detect_anomalies` | Extreme wins/losses, pattern breaks |
| `cluster_trades` | Groups trades by outcome patterns |
| `record_trade_journal` | Log completed trades with R-multiple, P&L, and notes |

</details>

---

### Connect any agent

System R is an MCP server. Any AI agent that speaks MCP can discover and call all 68 tools natively.

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

Pass your API key in session metadata. All 68 tools auto-discovered by the client.

</details>

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

**3. Connect a broker** (when ready)

```python
from systemr import SystemRClient

client = SystemRClient(api_key="sr_agent_...")
client.connect_broker("alpaca", {
    "api_key": "...",
    "api_secret": "...",
    "paper": True
})
```

Full walkthrough: [docs.systemr.ai/getting-started/quickstart](https://docs.systemr.ai/getting-started/quickstart)

---

### Pricing

**All 68 tools are free.** You only pay when the AI thinks.

| What | Cost |
|:-----|:-----|
| **All 68 MCP tools** | **Free** |
| **LLM usage** | Billed per use, cost varies by complexity |

System R's routing protocol selects the optimal model for each request automatically. No model selection needed. No configuration required.

#### Real-world cost examples

| Workflow | Cost |
|:---------|:-----|
| 1,000 pre-trade gates | **Free** |
| Full system assessment (7 tools) | **Free** |
| 1,000 position sizing calls | **Free** |
| 100 market scans | **Free** |

#### Payment methods

| Method | Rate |
|:-------|:-----|
| Card (Stripe) | 1:1 USD |
| USDC / USDT / PYUSD | 1:1 USD (Solana) |
| SOL | Live market rate |
| [OSR token](https://solscan.io/token/E2grvu8fyeeuVaxj2DrHVBqv8j21jK3vyJpXG8FJjJNc) | Market price + **50% bonus** |

**OSR presale buyers** receive a **permanent 20% discount** on all platform operations. Stacks with the 50% credit bonus.

Full pricing details: **[docs.systemr.ai/billing/pricing](https://docs.systemr.ai/billing/pricing)**

---

### Repositories

| Repo | What it is |
|:-----|:-----------|
| [`systemr-python`](https://github.com/System-R-AI/systemr-python) | Python SDK (`pip install systemr`) |
| [`demo-trading-agent`](https://github.com/System-R-AI/demo-trading-agent) | Reference agent showing System R integration |

---

<p align="center">
  <strong>OSR Token</strong>: <a href="https://solscan.io/token/E2grvu8fyeeuVaxj2DrHVBqv8j21jK3vyJpXG8FJjJNc"><code>E2grvu8...vK5H</code></a> &nbsp;&middot;&nbsp; <a href="https://osrprotocol.com">osrprotocol.com</a>
</p>

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
