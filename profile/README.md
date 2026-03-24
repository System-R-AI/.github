## System R AI

**Trading and investment operating system for AI agents.**

System R is a complete platform where AI agents access institutional-grade trading infrastructure: position sizing, risk validation, regime detection, Greeks analysis, equity curves, signal scoring, trade planning, compliance checks, and more. 380+ API endpoints backed by 13,241+ verified tests.

### Platform

[agents.systemr.ai](https://agents.systemr.ai) is live. 55 tools. 25 brokers and exchanges. Pay per call.

Deposit OSR, SOL, USDC, USDT, or PYUSD for compute credits. Presale buyers get 20% permanent discount.

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
```

### OSR Token

OSR is the compute credit token for the platform, built on Solana. Burn and Mint Equilibrium model. 1B supply, mint revoked, freeze revoked. Presale buyers receive a permanent 20% discount on all platform operations.

Token: [`E2grvu8fyeeuVaxj2DrHVBqv8j21jK3vyJpXG8FJjJNc`](https://solscan.io/token/E2grvu8fyeeuVaxj2DrHVBqv8j21jK3vyJpXG8FJjJNc)

### Team

**Ashim Nandi** (Founder) and **Shannon** (Co-Founder).

### Links

[systemr.ai](https://www.systemr.ai) | [agents.systemr.ai](https://agents.systemr.ai) | [osrprotocol.com](https://osrprotocol.com) | [SDK](https://github.com/System-R-AI/systemr-python) | [PyPI](https://pypi.org/project/systemr/)
