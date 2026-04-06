<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/System-R-AI/.github/main/assets/banner.svg">
  <img alt="System R AI — The Trading Operating System for AI Agents" src="https://raw.githubusercontent.com/System-R-AI/.github/main/assets/banner.svg" width="100%">
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

---

#### What's inside

| | |
|:--|:--|
| **55 tools across six layers** | Risk, intelligence, analysis, planning, execution, and memory |
| **25 brokers and exchanges** | Equities, options, futures, crypto, forex, and prediction markets |
| **One platform** | Covers the full lifecycle of every trade |

System R operates through its own specialized agentic system with domain-expert workflows that reason about risk, markets, and portfolio construction, not generalized LLM responses.

---

#### LLM control

System R gives you full control over how LLMs are used.

| Mode | How it works |
|:-----|:-------------|
| **Single model** | You choose one model for all tasks |
| **Multi-model routing** | You select multiple models, System R's routing protocol assigns each task to the best-qualified model automatically |
| **System R protocol** | Fully optimized model selection for trading and investment workflows |
| **Bring your own key** | Use your own Anthropic, OpenAI, or any other LLM API key. Pay your provider directly with zero LLM markup from System R |

9 models available today including Claude, GPT, DeepSeek, and Llama.

The platform is model-agnostic by design. Your workflows stay continuous even if any single provider becomes unavailable. System R's value is the specialized domain expertise built through its creators' lived experience in trading and investment. Intelligence is just a layer on top of it, whether it comes from in-house offerings or external providers.

---

#### For humans

Sign up at [systemr.ai](https://app.systemr.ai) and get **$5 free compute credits** to start. Voice chat available.

| Surface | |
|:--------|:--|
| **[Web app](https://app.systemr.ai)** | Browser-based interface at app.systemr.ai |
| **[Desktop CLI](https://github.com/System-R-AI/systemr-cli)** | Terminal client for power users |
| **[Mobile app](https://github.com/System-R-AI/systemr-mobile)** | iOS and Android |

---

#### For AI agents

No signup required. No account needed.

| Method | |
|:-------|:--|
| **[MCP protocol](https://docs.systemr.ai/mcp/overview)** | Any MCP-compatible client discovers all 55 tools natively |
| **[Python SDK](https://pypi.org/project/systemr/)** | `pip install systemr` |
| **[REST API](https://agents.systemr.ai)** | `POST /v1/tools/call` with `X-API-Key` header |
| **Solana wallet (x402)** | Pay per call on-chain, no account needed |

---

#### Fair, transparent pricing

Every tool call, every LLM request, every broker order is a micro-transaction on a **usage-based compute credit** system. No subscriptions, no monthly fees, credits never expire.

| Method | Rate |
|:-------|:-----|
| Card (Stripe) | 1:1 USD |
| USDC / USDT / PYUSD | 1:1 USD (Solana) |
| SOL | Live market rate |
| **[OSR token](https://solscan.io/token/E2grvu8fyeeuVaxj2DrHVBqv8j21jK3vyJpXG8FJjJNc)** | **50% credit bonus** |

---

#### Solana settlement

The OSR token, issued by **OSR Protocol**, is the native compute credit on Solana. System R uses Solana through OSR Protocol as its agentic settlement and payment layer.

Solana's sub-second finality, near-zero transaction costs, native stablecoin infrastructure, and tokenization capabilities make it the natural settlement rail for autonomous agents operating across global markets.

Explore Solana RWA intelligence at **[sol.systemr.ai](https://sol.systemr.ai)**.

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

### 55 tools, six layers

<details>
<summary><strong>Risk</strong> | 12 tools &nbsp; <sub>Position sizing, validation, and controls</sub></summary>
<br>

| Tool | What it does | Cost |
|:-----|:-------------|:-----|
| `calculate_position_size` | G-formula geometric growth optimization | $0.003 |
| `check_trade_risk` | Iron Fist risk validation (position + portfolio + daily limits) | $0.004 |
| `evaluate_performance` | G-metric analysis (score, grade, rolling trend) | $0.10 - $1.00 |
| `analyze_drawdown` | Drawdown periods, depth, recovery time | $0.005 |
| `run_monte_carlo` | 1,000-10,000 simulated equity paths | $0.008 |
| `calculate_kelly` | Kelly criterion (full, half, quarter) | $0.004 |
| `find_variance_killers` | Trades that damage geometric growth | $0.006 |
| `analyze_win_loss` | Win/loss statistics and streaks | $0.004 |
| `run_what_if` | G-improvement scenarios | $0.008 |
| `analyze_confidence` | Confidence intervals on R-multiples | $0.005 |
| `analyze_risk_adjusted` | Sharpe, Sortino, Calmar ratios | $0.005 |
| `calculate_system_r_score` | Composite score 0-100, grade A+ through F | $0.005 |

</details>

<details>
<summary><strong>Intelligence</strong> | 11 tools &nbsp; <sub>Market regime, patterns, and signals</sub></summary>
<br>

| Tool | What it does | Cost |
|:-----|:-------------|:-----|
| `detect_patterns` | Breakouts, pullbacks, MA crossovers, RSI divergences, gaps | $0.008 |
| `detect_structural_break` | Distribution break detection (recent vs historical) | $0.006 |
| `analyze_trend_structure` | Bollinger/ATR expansion, compression, squeeze detection | $0.006 |
| `calculate_indicators` | SMA, EMA, RSI, MACD, Bollinger Bands, ATR | $0.004 |
| `analyze_price_structure` | Support/resistance, swing points, consolidation zones | $0.006 |
| `analyze_correlations` | Multi-symbol correlation matrix | $0.008 |
| `analyze_liquidity` | Volume analysis (normal, thinning, stressed, spike) | $0.004 |
| `analyze_greeks` | Options Greeks portfolio exposure | $0.006 |
| `analyze_iv_surface` | Implied volatility surface structure | $0.008 |
| `analyze_futures_curve` | Term structure (contango, backwardation, flat) | $0.006 |
| `analyze_options_flow` | Options order flow directional signals | $0.006 |

</details>

<details>
<summary><strong>Analysis</strong> | 18 tools &nbsp; <sub>Statistical analysis and diagnostics</sub></summary>
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
<summary><strong>Planning</strong> | 4 tools &nbsp; <sub>Options and futures position building</sub></summary>
<br>

| Tool | What it does | Cost |
|:-----|:-------------|:-----|
| `size_options_position` | 4 modes: equity risk, premium, delta-adjusted, spread | $0.004 |
| `size_futures_position` | 3 modes: margin-based, tick value, notional | $0.004 |
| `build_options_plan` | Complete options plan from thesis (bullish/bearish/neutral/volatile) | $0.008 |
| `build_futures_plan` | Structured futures plan with entry, stop, and target | $0.008 |

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

All broker credentials encrypted per-agent. Decrypted only at moment of execution. $0.015 per order.

</details>

<details>
<summary><strong>Memory</strong> | 8 tools &nbsp; <sub>Learning, biases, and behavioral analysis</sub></summary>
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

#### LLM models (per 1M tokens)

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

**BYOK** (Bring Your Own Key): Connect your own API key. LLM usage billed directly by the provider. System R charges only for tool calls.

#### Real-world cost examples

| Workflow | Cost |
|:---------|:-----|
| Single pre-trade gate | $0.01 |
| Position size + risk check | $0.007 |
| Backtest diagnostic (6 tools) | ~$0.032 |
| Chat session (Sonnet, ~2K tokens) | ~$0.10 |
| 100 pre-trade gates / day | $1.00 |
| Full system assessment (7 tools) | $2.00 |

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
| [`sol-systemr`](https://github.com/System-R-AI/sol-systemr) | Solana RWA Intelligence Hub ([sol.systemr.ai](https://sol.systemr.ai)) |
| [`systemr-cli`](https://github.com/System-R-AI/systemr-cli) | Terminal client for System R |

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
