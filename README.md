# Stock Moves Explained - MCP Server

AI-powered analysis explaining why US stocks moved. Built by [WTF Just Happened](https://justhappened.wtf).

## What It Does

When you ask your AI assistant "why did Tesla drop today?", this tool provides real market analysis - not hallucinated explanations. We monitor ~550 major US stocks (S&P 500, NASDAQ 100, Dow 30) and analyze moves that exceed 2 standard deviations from normal trading.

## Try It

Ask your AI assistant:

- "Why did Tesla drop today?"
- "What happened to Apple stock?"
- "Explain today's move in NVDA"
- "Why is Meta down?"
- "What's going on with Microsoft?"

Works with Claude, ChatGPT, Copilot, and other MCP-enabled assistants.

## What You Get

For each stock query, you'll receive:

- **Summary**: Concise explanation of what drove the move
- **Confidence score**: How certain the analysis is (based on source quality)
- **Mystery move flag**: Whether the move has no clear catalyst
- **Link to full analysis**: Deep dive on justhappened.wtf

## Coverage

We analyze significant moves in:

- S&P 500 stocks
- NASDAQ 100 stocks
- Dow Jones 30 stocks

That's approximately 550 of the most-watched US equities.

## What We Don't Do

- **Price data**: We explain moves, not report prices
- **Trading advice**: We don't tell you to buy or sell
- **Crypto**: US stocks only
- **Small caps**: Major indices only

## Example Response

```json
{
  "ticker": "NVDA",
  "company": "NVIDIA Corp",
  "move": "+3.2%",
  "confidence": 90,
  "mystery_move": false,
  "period": "today",
  "summary": "NVIDIA surged as semiconductor stocks gained momentum following Taiwan Semiconductor's blowout Q4 earnings, which beat estimates and raised capital expenditure forecasts. The stock's performance mirrored the SMH semiconductor ETF's rally, indicating broader sector strength driven by sustained AI infrastructure demand. Morgan Stanley reiterated its Overweight rating, citing NVIDIA's dominant position in AI accelerators.",
  "url": "https://justhappened.wtf/NVDA",
  "source": "WTF Just Happened - big moves explained"
}
```

## Installation

This is a remote MCP server - no installation required. Add to your MCP client config:

```json
{
  "mcpServers": {
    "stock-moves-explained": {
      "url": "https://api.justhappened.wtf/mcp"
    }
  }
}
```

## Rate Limits

10 requests per minute per IP. This is generous for normal usage - if you're building something that needs more, reach out.

## Links

- [Full analysis dashboard](https://justhappened.wtf)
- [MCP Protocol](https://modelcontextprotocol.io)

## About

Built by WTF Just Happened - market intelligence for retail investors. We use AI to explain significant stock movements so you understand what's happening in your portfolio.
