# EdgeMarket

**Autonomous prediction market intelligence agent.**

EdgeMarket analyzes any Polymarket question, forms an independent probability estimate using evidence-based reasoning, then compares it against current market odds to surface actionable edges.

It is not a news summarizer. It is an edge finder.

---

## What It Does

Give it a market question and the current odds. It returns:

- An independent probability estimate derived from base rates and evidence
- A step-by-step probability derivation showing every adjustment
- Edge calculation (your estimate minus market odds), adjusted for fees
- Signal classification: NO SIGNAL / WEAK / MODERATE / STRONG / CRITICAL
- Position recommendation with bankroll sizing guidance
- Risk flags, correlated markets, and upcoming catalysts

It covers all Polymarket categories — crypto, politics, macroeconomics, sports, geopolitics, and any other binary or categorical outcome.

---

## How To Use It

1. Copy the full system prompt from [prompt.md](./prompt.md)
2. Paste it into any capable LLM (GPT-4o, Claude, Gemini, etc.)
3. Input a market in this format:

```
[Market question] — [current odds]%
```

**Example input:**
```
Will the Fed cut rates at the September 2025 FOMC meeting? — 34%
```

**With additional context:**
```
Will Bitcoin exceed $100k before December 31 2025? — 62%
Context: Recent CPI came in above expectations at 3.4%.
```

**Batch mode:**
```
Analyze these three markets:
1. Will Ethereum ETF net inflows exceed $1B in July 2025? — 41%
2. Will the ECB cut rates in October 2025? — 58%
3. Will Arsenal win the Premier League 2025/26? — 22%
```

---

## Why It Works

Most LLMs default to summarizing headlines and echoing market consensus. EdgeMarket is built to fight that.

The prompt forces:

- Independent estimation before comparing to market odds
- Bayesian-style evidence updates with explicit probability adjustments
- Mandatory regression toward base rates when evidence is thin
- Uncertainty bands instead of false point precision
- Position sizing guidance tied to signal strength and confidence
- Fee-adjusted edge calculation

The result is analysis that resembles a quantitative research desk rather than a chatbot.

---

## Example Output

See [examples/example_1.md](./examples/example_1.md) for a full sample analysis.

---

## Marketplace

EdgeMarket is available as a tokenized prompt product on the Swarms Marketplace.

[View on Swarms →](https://swarms.world/prompt/550411c6-250c-4927-b3a9-c278377983a8)

---

## Author

Built by [@scarrxt](https://x.com/scarrxt)
